# ESP32 Smart Environment Monitor

## 项目简介
这是一个基于 ESP32 的智能环境监测与异常告警系统项目。

## 项目目标
本项目将逐步实现以下功能：
- 环境数据采集
- OLED 显示
- 串口日志输出
- 超阈值告警
- 简单异常检测
- 模块化代码设计

## 当前阶段
Week 1 - 项目初始化与开发环境搭建

## 项目目录结构
```text
esp32-smart-env-monitor/
├── README.md
├── docs/
├── src/
├── diagrams/
└── screenshots/



# ESP32 智能环境监测器

## 项目简介
这是一个基于 ESP32 的智能环境监测与异常告警系统学习项目。
项目目标是逐步实现环境数据采集、状态显示、异常判断和告警输出。

## 当前进度
第 1 周已完成：
- GitHub 仓库初始化
- 项目目录结构创建
- Wokwi 上的 ESP32 LED 闪烁实验
- 串口打印实验

## 本周完成内容
- 创建 GitHub 仓库
- 搭建项目基础目录
- 完成 LED 每 500ms 闪烁
- 完成串口输出 `LED ON` 和 `LED OFF`
- 初步理解 `setup()` 和 `loop()` 的运行逻辑
- 初步理解 GPIO 输出与串口调试

## 示例代码

```cpp
const int LED_PIN = 2;

void setup() {
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(115200);
  Serial.println("System start");
}

void loop() {
  digitalWrite(LED_PIN, HIGH);
  Serial.println("LED ON");
  delay(500);

  digitalWrite(LED_PIN, LOW);
  Serial.println("LED OFF");
  delay(500);
}
