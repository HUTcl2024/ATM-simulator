# 💳 ATM Simulator（C语言版）

[![Language](https://img.shields.io/badge/language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-lightgrey.svg)](#)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-stable-success.svg)](#)
[![Last Commit](https://img.shields.io/github/last-commit/HUTcl2024/ATM-simulator.svg)](https://github.com/HUTcl2024/ATM-simulator/commits/main)

> 🏧 一款使用 **C语言** 编写的轻量级 **ATM 模拟器**，支持存款、取款、查看流水与自动保存历史记录。  
> 适合 C 语言初学者学习文件读写、结构体与时间函数的综合应用。

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 💰 存款 | 输入金额（支持两位小数，如 `100.50`） |
| 💸 取款 | 自动检测余额是否足够 |
| 📜 交易记录 | 查看所有交易记录（含时间戳与余额） |
| 🧮 查看余额 | 显示当前账户余额 |
| 💾 数据持久化 | 自动保存至 `transactions.csv` 与 `transactions.json` |
| 🔁 自动加载 | 启动时自动恢复上次交易记录与余额 |

---

## 🗂️ 数据文件示例

程序运行后会自动生成以下两个文件：

| 文件名 | 描述 |
|--------|------|
| `transactions.csv` | 可用 Excel 打开，查看所有交易流水 |
| `transactions.json` | 程序自动读取的历史数据文件 |

### 📘 JSON 示例
```json
{
  "balance_cents": 12345,
  "transactions": [
    {"type":1,"amount":10000,"balance_after":10000,"timestamp":1700000000},
    {"type":2,"amount":5000,"balance_after":5000,"timestamp":1700003600}
  ]
}
🧠 技术亮点
⚙️ 使用结构体保存交易记录

📆 时间戳由 time() 自动生成

💾 纯标准 C 实现 JSON 与 CSV 文件读写

🪙 金额以“分”为单位存储，避免浮点误差

🚫 无第三方依赖，跨平台兼容（Windows / Linux / macOS）

🧰 使用方法
🧩 编译
在 PowerShell / CMD 中执行：

bash
复制代码
cd "D:\pycharm\ATM simulator"
gcc -std=c11 -Wall -Wextra -O2 -mconsole atm.c -o atm.exe
▶️ 运行
bash
复制代码
.\atm.exe
📋 菜单示例
markdown
复制代码
==============================
          ATM MENU
==============================
1) Deposit
2) Withdraw
3) View transactions
4) View balance
0) Exit
Select an option:
🖼️ 示例截图
（你可以替换为自己的截图 👇）

启动界面	查看交易记录

📦 项目结构
bash
复制代码
ATM-simulator/
│
├── atm.c                 # 主程序源代码
├── transactions.csv      # 交易记录（自动生成）
├── transactions.json     # 历史记录（自动生成）
├── README.md             # 项目说明文件
└── .vscode/              # VS Code 配置（可选）
📖 后续计划
 多账户支持 + 登录 PIN

 导出为 .xlsx（Excel 文件）

 图形化界面（GTK / Qt）

 网络同步版本

📜 开源许可
本项目采用 MIT License 开源协议，欢迎学习、修改与分发。

💡 若你喜欢本项目，请点亮右上角的 ⭐Star 支持一下！

👤 作者信息
作者：陈雷（@HUTcl2024）
项目地址：https://github.com/HUTcl2024/ATM-simulator
