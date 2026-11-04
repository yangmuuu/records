| 发送方式 | HAL 函数 | 是否阻塞 | 完成回调 |
| --- | --- | --- | --- |
| 普通轮询发送 | HAL\_UART\_Transmit() | 是 | 无 |
| 普通中断发送 | HAL\_UART\_Transmit\_IT() | 否 | HAL\_UART\_TxCpltCallback() |
| 普通 DMA 发送 | HAL\_UART\_Transmit\_DMA() | 否 | HAL\_UART\_TxCpltCallback() |
