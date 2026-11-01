
# 公共属性

## QObject

## QWidget


# Buttons

## QPushButton

```c++
autodefault_btn = new QPushButton("自动默认按钮autodefault",this);
default_btn = new QPushButton("自动默认按钮default",this);
flat_btn = new QPushButton("扁平化flat",this);
autodefault_btn->setGeometry(0,0,150,40);
autodefault_btn->setAutoDefault(true);
default_btn->setGeometry(0,50,150,40);
default_btn->setDefault(true);
flat_btn->setGeometry(0,100,150,40);
flat_btn->setFlat(true);
```

## QToolButton
```c++
toolBtn1 = new QToolButton(this);

// 设置下拉模式，需要关联菜单
toolBtn1->setPopupMode(QToolButton::DelayedPopup);
// 设置btn 显示模式
toolBtn1->setToolButtonStyle(Qt::ToolButtonIconOnly);
// 3D立体UI
toolBtn1->setAutoRaise(true);
// 箭头方向
toolBtn1->setArrowType(Qt::UpArrow);
```

## QRadioButton

checkable:是否可选中
checked:默认选中
autoExclusive:默认互斥

## QCheckBox

tristate:中间状态，默认值false

## QCommandLinkButton

description: 按钮描述 QString

## QDialogButtonBox
orientation：排布方向 QtEnumPropertyType
standarButtons：按钮方向 DesignerFlagPropertyType  ok|cancel
centerButtons：按钮居中 bool

# Input Widgets

## QComboBox
![](assets/Pasted%20image%2020260227103110.png)

## QFontComboBox
![](assets/Pasted%20image%2020260227141604.png)

## QLineEdit
![](assets/Pasted%20image%2020260227141906.png)

## QTextEdit
![](assets/Pasted%20image%2020260227160323.png)
![](assets/Pasted%20image%2020260227160335.png)
## QFrame
![](assets/Pasted%20image%2020260227143029.png)

## QAbstractScorollArea
![](assets/Pasted%20image%2020260227155412.png)

## QPlainTextEdit
![](assets/Pasted%20image%2020260227161915.png)


## QAbstractSpinBox

![](assets/Pasted%20image%2020260227162329.png)

## QSpinBox
![](assets/Pasted%20image%2020260227162045.png)
## QDoubleSpinBox
![](assets/Pasted%20image%2020260227163112.png)

## QTimeEdit
![](assets/Pasted%20image%2020260227163831.png)![](assets/Pasted%20image%2020260227163840.png)

## QDateEdit
![](assets/Pasted%20image%2020260227164646.png)

## QDateTimeEdit

## QAbstractSlider
![](assets/Pasted%20image%2020260227165029.png)

## QDial
![](assets/Pasted%20image%2020260227165216.png)

## Horizontal Scroll Bar 

![](assets/Pasted%20image%2020260227170509.png)

## Vertical Scroll Bar
![](assets/Pasted%20image%2020260227170518.png)

## Horizontal Slider
![](assets/Pasted%20image%2020260227170557.png)

## Vertical Slider


## QSlider

## QKeySequenceEdit
![](assets/Pasted%20image%2020260228090943.png)
![](assets/Pasted%20image%2020260228090951.png)


# Display Widgets

## QLabel

![](assets/Pasted%20image%2020260228091803.png)
![](assets/Pasted%20image%2020260228091854.png)

## Text Browser
![](assets/Pasted%20image%2020260228092130.png)

## Calendar Widget
![](assets/Pasted%20image%2020260228092417.png)

## QCalendarWidget
![](assets/Pasted%20image%2020260228092540.png)

## QLCDNumber
![](assets/Pasted%20image%2020260228092852.png)

![](assets/Pasted%20image%2020260228092858.png)

## QProgressBar

![](assets/Pasted%20image%2020260228093021.png)

![](assets/Pasted%20image%2020260228093107.png)

![](assets/Pasted%20image%2020260228093457.png)
![](assets/Pasted%20image%2020260228093503.png)


## Horizontal Line

![](assets/Pasted%20image%2020260228095906.png)

## Vertical Line


# Layout


## layout
![](assets/Pasted%20image%2020260228100516.png)

## Vertical Layout
![](assets/Pasted%20image%2020260228100113.png)


## Horizontal Layout
![](assets/Pasted%20image%2020260228143635.png)

## Grid Layout
![](assets/Pasted%20image%2020260228143714.png)

## Form Layout
![](assets/Pasted%20image%2020260228143902.png)


## Horizontal Spacer

![](assets/Pasted%20image%2020260228144112.png)

## Vertical Spacer


# Containers


## QGroupBox
![](assets/Pasted%20image%2020260228144327.png)

![](assets/Pasted%20image%2020260228145133.png)

## Scroll Area
![](assets/Pasted%20image%2020260228145441.png)

## QToolBox
![](assets/Pasted%20image%2020260228150001.png)

![](assets/Pasted%20image%2020260228150748.png)


## QTabWidget
![](assets/Pasted%20image%2020260228151421.png)

![](assets/Pasted%20image%2020260228151543.png)
![](assets/Pasted%20image%2020260228151616.png)

## QStackWidget
![](assets/Pasted%20image%2020260228160400.png)

## QDockWidget
![](assets/Pasted%20image%2020260228161210.png)

# Item Views

## List View
![](assets/Pasted%20image%2020260228161612.png)

```c++
    // 实例化model模型
    QStandardItemModel *model = new QStandardItemModel();

    // 给model模型添加元素 (行列索引)
    model->setItem(
        0,  // row
        0, // column
        new QStandardItem(QString::fromStdString("你好"))
        );

    // 将model对象绑定 listview 表项视图控件
    ui->listView->setModel(model);
```

![](assets/Pasted%20image%2020260304152439.png)
![](assets/Pasted%20image%2020260304152646.png)
![](assets/Pasted%20image%2020260304153333.png)

##  QListView
![](assets/Pasted%20image%2020260304153816.png)
![](assets/Pasted%20image%2020260304153950.png)

## Tree View
```c++
// 模拟treeview数据
std::list<std::map<std::string, std::any>> cities = {
    {
        {"name", std::string("上海市")},
        {"children", std::list<std::map<std::string, std::string>>{
            {{"name", std::string("徐汇区")}},
            {{"name", std::string("浦东区")}}
        }}
    },
    {
        {"name", std::string("上海市")},
        {"children", std::list<std::map<std::string, std::string>>{
                {{"name", std::string("徐汇区")}},
                {{"name", std::string("浦东区")}}
        }}
    },
};


void MyListItem::loadTreeView()
{
    // 给treeview加载数据
    QStandardItemModel *model = new QStandardItemModel();
    // 循环数据中的一级节点
    for(std::map<std::string, std::any> parent : cities)
    {
        // 根据当前遍历到的节点，创建item
        QStandardItem *parentItem = new QStandardItem(QString::fromStdString(std::any_cast<std::string>(parent["name"])));
        // 将当前创建的item添加到model中的根节点上
        model->invisibleRootItem()->appendRow(parentItem);
        // 判断当前节点是否是children 结束之前找到了
        if(parent.find("children") != parent.end())
        {
            // 获取当前children的子节点
            std::list<std::map<std::string, std::string>> children = std::any_cast<std::list<std::map<std::string, std::string>>>(parent["children"]);
            // 循环子节点
            for(std::map<std::string, std::string> child : children)
            {
                // 创建item
                QStandardItem *childItem = new QStandardItem(QString::fromStdString(child["name"]));
                // 将子节点item添加到parent
                parentItem->appendRow(childItem);
            }

        }
    }

    // 给treeview绑定model模型
    ui->treeView->setModel(model);
}
```

![](assets/Pasted%20image%2020260309090119.png)

## Table View
![](assets/Pasted%20image%2020260309090351.png)

```c++
void MyListItem::loadTableView()
{
    // 1. 创建 Model 并设置父对象（防止内存泄漏）
    QStandardItemModel *model = new QStandardItemModel(this);

    // 2. 设置表头
    QStringList headers = {"姓名", "年龄", "城市", "职业"};
    model->setHorizontalHeaderLabels(headers);

    // 3. 模拟一些数据源 (通常这部分数据来自数据库或 API)
    struct Person {
        QString name;
        int age;
        QString city;
        QString job;
    };

    QList<Person> dataList = {
        {"张三", 25, "上海", "工程师"},
        {"李四", 30, "北京", "设计师"},
        {"王五", 28, "广州", "产品经理"}
    };

    // 4. 填充数据到 Model
    for (int i = 0; i < dataList.size(); ++i) {
        const auto& person = dataList[i];

        // 创建每一列的 Item
        QStandardItem *nameItem = new QStandardItem(person.name);
        QStandardItem *ageItem  = new QStandardItem(QString::number(person.age));
        QStandardItem *cityItem = new QStandardItem(person.city);
        QStandardItem *jobItem  = new QStandardItem(person.job);

        // 将这一行的 Item 组合成一个列表，然后添加到 model
        QList<QStandardItem*> row;
        row << nameItem << ageItem << cityItem << jobItem;

        model->appendRow(row);
    }

    // 5. 绑定 Model 到 View
    ui->tableView->setModel(model);

    // 6. 额外的小技巧：自适应列宽
    ui->tableView->horizontalHeader()->setSectionResizeMode(QHeaderView::Stretch);
}
```

![](assets/Pasted%20image%2020260309090959.png)


## Column View

![](assets/Pasted%20image%2020260309091233.png)

![](assets/Pasted%20image%2020260309091548.png)


## Undo View

操作记录视图

![](assets/Pasted%20image%2020260309091607.png)

![](assets/Pasted%20image%2020260309092123.png)


# 信号和槽

```c++
connect(btn, &QPushButton::clicked, this, &MainWindow::pushButtonClicked);
```

# 对话框

## 非模态对话框
![](assets/Pasted%20image%2020260309103918.png)

## 窗口级别模态对话框
![](assets/Pasted%20image%2020260309103947.png)

## 应用级别模态对话框
![](assets/Pasted%20image%2020260309104122.png)

## QMessageBox

![](assets/Pasted%20image%2020260309104411.png)

## QInputDialog

![](assets/Pasted%20image%2020260309104444.png)

## QColorDialog

## QFontDialog

## QFileDialog

# 菜单栏

![](assets/Pasted%20image%2020260309104625.png)

## MenuBar
![](assets/Pasted%20image%2020260309110204.png)

```c++
    // 菜单栏
    QMenuBar *mBar = new QMenuBar();
    this->setMenuBar(mBar);

    QMenu *fileMenu = mBar->addMenu("文本");

    fileMenu->addAction("点击测试", this, []() {
        qDebug() << "菜单被点击了！";
    });

    fileMenu->addAction("第二个选项", this, []() {
        qDebug() << "这是第二个选项的内容";
    });
```

## Tool Bar Area

![](assets/Pasted%20image%2020260309110649.png)

## Status Bar
![](assets/Pasted%20image%2020260309110823.png)

# QPainter

重写重绘事件

## 绘制文字

```c++
public:
    // 重写重绘事件
    void paintEvent(QPaintEvent* event);

void MyPaintEvent::paintEvent(QPaintEvent *evevt)
{
    QPen pen;
    pen.setColor(QColor(100,100,150));

    QFont font;
    font.setFamily("Microsoft YaHei");
    font.setPointSize(48);

    // 创建画家
    QPainter painter(this); // 画在当前窗体
    painter.setPen(pen);
    painter.setFont(font);
    painter.drawText(50,90, "测试");
}
```

## 绘制直线
![](assets/Pasted%20image%2020260309112530.png)

## 绘制矩形

![](assets/Pasted%20image%2020260309112606.png)

## 绘制圆

![](assets/Pasted%20image%2020260309112641.png)

## 绘制多边形

![](assets/Pasted%20image%2020260309112703.png)

## 绘制图片
![](assets/Pasted%20image%2020260309112809.png)

## QPixmap

适合画图标

![](assets/Pasted%20image%2020260309113110.png)

## QImage

主要用于对现有的图片进行像素级别的修改

![](assets/Pasted%20image%2020260309113234.png)

## QPicture

主要对QPainter的操作进行存档

![](assets/Pasted%20image%2020260309113330.png)

![](assets/Pasted%20image%2020260309113420.png)


# 图表

QChart

```yaml
find_package(Qt6 COMPONENTS Charts REQUIRED)

target_link_libraries(project1 PRIVATE Qt${QT_VERSION_MAJOR}::Widgets Qt6::Charts)
```

**导包**

```c++
#include <QtCharts>

QT_BEGIN_NAMESPACE
class QChartView
class QChart
QT_END_NAMESPACE
```

将Graphics View提升为QChartView

## QValueAxis

![](assets/Pasted%20image%2020260309134447.png)
![](assets/Pasted%20image%2020260309134514.png)
![](assets/Pasted%20image%2020260309134547.png)
![](assets/Pasted%20image%2020260309134559.png)

![](assets/Pasted%20image%2020260309134610.png)

## QScatterSeries
散点序列

![](assets/Pasted%20image%2020260309145021.png)
![](assets/Pasted%20image%2020260309145102.png)


```c++
// 图2 散点图
QScatterSeries *scatterSeries = new QScatterSeries();
scatterSeries->setName("散点图");
scatterSeries->setMarkerShape(QScatterSeries::MarkerShapeStar);
scatterSeries->setMarkerSize(10);

scatterSeries->append(1, 2);
scatterSeries->append(3, 5);
scatterSeries->append(7, 8);
scatterSeries->append(12, 6);

QChart * scatterChart = new QChart();
scatterChart->addSeries(scatterSeries);
scatterChart->setTitle("散点图坐标");

QValueAxis *axisX = new QValueAxis();
axisX->setRange(0, 20);          // 设置范围 0 到 20
axisX->setTickCount(11);         // 设置刻度线数量
axisX->setLabelFormat("%d");     // 设置标签格式（整数）
axisX->setTitleText("时间 (s)");  // 设置 X 轴标题

QValueAxis *axisY = new QValueAxis();
axisY->setRange(0, 15);          // 设置范围 0 到 15
axisY->setTickCount(6);          // 设置刻度线数量
axisY->setTitleText("电压 (V)");  // 设置 Y 轴标题

// 注意：必须先 addAxis 再 attachSeries
scatterChart->addAxis(axisX, Qt::AlignBottom);
scatterChart->addAxis(axisY, Qt::AlignLeft);
scatterSeries->attachAxis(axisX);
scatterSeries->attachAxis(axisY);

QChartView *scatterView = new QChartView(scatterChart);
scatterView->setRenderHint(QPainter::Antialiasing);

gridLayout->addWidget(scatterView, 0, 1);

gridLayout->addWidget(new QLabel("第一行-第三列 (0,2)", this), 0, 2);

```

## QLineSeries & QSplineSeries
![](assets/Pasted%20image%2020260309151515.png)
![](assets/Pasted%20image%2020260309151628.png)
![](assets/Pasted%20image%2020260309151646.png)
![](assets/Pasted%20image%2020260309151708.png)

```c++
    // 图1 折线图
    QWidget *centralWidget = new QWidget(this);
    QGridLayout *gridLayout = new QGridLayout(centralWidget);
    this->setCentralWidget(centralWidget); // 挂载在中心区域

    QLineSeries *series = new QLineSeries();
    series->append(0, 5);
    series->append(2, 10);

    QChart *chart = new QChart();
    chart->addSeries(series);
    chart->createDefaultAxes();
    chart->legend()->hide();

    QChartView *chartView = new QChartView(chart); // 创建视图，并填充chart
    chartView->setRenderHint(QPainter::Antialiasing); //抗锯齿
```

```c++
    // 曲线图
    QSplineSeries *splineSeries = new QSplineSeries();
    splineSeries->setName("平滑曲线 (ESP32)");

    // 添加一些波动较大的点，观察平滑效果
    splineSeries->append(0, 1);
    splineSeries->append(2, 4);
    splineSeries->append(3, 3);
    splineSeries->append(5, 8);
    splineSeries->append(7, 2);
    splineSeries->append(10, 5);

    // 2. 创建图表
    QChart *splineChart = new QChart();
    splineChart->addSeries(splineSeries);
    splineChart->setTitle("实时平滑曲线");
    splineChart->createDefaultAxes(); // 暂时先用默认轴
    splineChart->legend()->setVisible(true); // 显示图例
    splineChart->legend()->setAlignment(Qt::AlignBottom);

    // 3. 创建视图
    QChartView *splineView = new QChartView(splineChart);
    splineView->setRenderHint(QPainter::Antialiasing); // 曲线图必须开启抗锯齿，否则会有锯齿感

```


## QBarSeries
QBarSeries 普通柱状序列
QStackedBarSeries 堆叠柱状序列
QPercentBarSeries 百分比柱状序列

```c++
    QBarSet *set = new QBarSet("数据1");
    *set << 1 << 2 << 3 << 4 << 5; // 标准流操作符添加数据

    QBarSeries *barSeries = new QBarSeries();
    barSeries->append(set);

    QChart *barChart = new QChart();
    barChart->addSeries(barSeries);
    barChart->createDefaultAxes();
    barChart->setTitle("柱状图对比");

    QChartView *barView = new QChartView(barChart);
    gridLayout->addWidget(barView, 1, 0);
```

## QPieSeries
```c++
    QPieSeries *pieSeries = new QPieSeries();
    pieSeries->append("分类A", 30);
    pieSeries->append("分类B", 70);

    // 获取第一个切片并设置突出显示
    QPieSlice *slice = pieSeries->slices().at(0);
    slice->setExploded();
    slice->setLabelVisible();

    QChart *pieChart = new QChart();
    pieChart->addSeries(pieSeries);
    pieChart->setTitle("饼图占比");

    QChartView *pieView = new QChartView(pieChart);
    gridLayout->addWidget(pieView, 1, 1);
```

## QPolarChart
极坐标
![](assets/Pasted%20image%2020260309152346.png)

```c++
    // --- (1, 2) 极坐标图 QPolarChart ---
    // 注意：极坐标必须用 QPolarChart 而不是 QChart
    QPolarChart *polarChart = new QPolarChart();
    polarChart->setTitle("极坐标图");

    QLineSeries *polarSeries = new QLineSeries();
    polarSeries->append(0, 5);
    polarSeries->append(90, 10);
    polarSeries->append(180, 5);
    polarSeries->append(270, 10);
    polarSeries->append(360, 5);
    polarChart->addSeries(polarSeries);

    // 极坐标必须手动创建并添加坐标轴
    QValueAxis *axisAng = new QValueAxis(); // 角度轴
    axisAng->setRange(0, 360);
    polarChart->addAxis(axisAng, QPolarChart::PolarOrientationAngular);

    QValueAxis *axisRad = new QValueAxis(); // 径向轴
    axisRad->setRange(0, 15);
    polarChart->addAxis(axisRad, QPolarChart::PolarOrientationRadial);

    polarSeries->attachAxis(axisAng);
    polarSeries->attachAxis(axisRad);

    QChartView *polarView = new QChartView(polarChart);
```

# 动画

![](assets/Pasted%20image%2020260309152756.png)

```c++
chart->setAnimationOptions(QChart::AllAnimations);
```

1
