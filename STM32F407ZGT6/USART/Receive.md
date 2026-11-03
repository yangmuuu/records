| 接收方式 | HAL 函数 | 变长接收 | 是否阻塞 |
| --- | --- | --- | --- |
| 普通轮询接收 | HAL\_UART\_Receive() | 否，按指定长度 | 是 |
| 普通中断接收 | HAL\_UART\_Receive\_IT() | 否，按指定长度 | 否 |
| 普通 DMA 接收 | HAL\_UART\_Receive\_DMA() | 否，按指定长度 | 否 |
| 空闲轮询接收 | HAL_UARTEx_ReceiveToIdle() | 是 | 是 |
| 空闲中断接收 | HAL\_UARTEx\_ReceiveToIdle\_IT() | 是 | 否 |
| 空闲 DMA 接收 | HAL\_UARTEx\_ReceiveToIdle\_DMA() | 是 | 否 |

## 普通轮询接收 HAL_UART_Receive

```c
  /* USER CODE BEGIN 2 */
  // buffer缓冲区
  uint8_t buffer[100];
  // 回复消息 这里是5字节
  uint8_t msg[] = "ok\r\n";
  /* USER CODE END 2 */

  /* Infinite loop */
  /* USER CODE BEGIN WHILE */
  while (1)
  {
      // Receive每次都会从buffer[0]开始，所以不会移除
      if (HAL_UART_Receive(&huart1, buffer, 10, HAL_MAX_DELAY) == HAL_OK)
      {
          // sizeof() - 1，不发送末尾的\0
          HAL_UART_Transmit(&huart1, msg, sizeof(msg) - 1, HAL_MAX_DELAY);
      }
      /* USER CODE END WHILE */

      /* USER CODE BEGIN 3 */
  }
```


## 空闲轮询接收 HAL_UARTEx_ReceiveToIdle()

```c
  /* USER CODE BEGIN 2 */
  // buffer缓冲区
  uint8_t buffer[100];
  // 实际接收的字符数
  uint16_t rx_len = 0;
  /* USER CODE END 2 */

  /* Infinite loop */
  /* USER CODE BEGIN WHILE */
  while (1)
  {
    // 最多写buffer长度的字节，rx_len为实际接收长度
    if(HAL_UARTEx_ReceiveToIdle(&huart1, buffer, sizeof(buffer), &rx_len, HAL_MAX_DELAY) == HAL_OK)
    {
      HAL_UART_Transmit(&huart1, buffer, rx_len, HAL_MAX_DELAY);
    }
    /* USER CODE END WHILE */

    /* USER CODE BEGIN 3 */
  }
```


## 普通中断接收 HAL_UART_Receive_IT()

开启cubemax中的uart1的nvic


