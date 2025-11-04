💳 ATM 模拟器（C语言版）

一个用 C语言 编写的简易 ATM 自动取款机模拟程序，支持存款、取款、查看交易记录、余额查询等功能，并且可以在退出时自动保存交易历史到 CSV 与 JSON 文件，下次启动时自动加载历史记录。

🚀 功能介绍

✅ 核心功能

💰 存款：输入金额（支持小数两位，如 100.50）

💸 取款：自动检测余额是否足够

📜 查看交易记录：带时间戳的详细流水

🧮 查看当前余额

💾 自动保存数据到 transactions.csv 与 transactions.json

🔁 程序启动时自动读取上次的交易记录与余额

🗂️ 数据文件说明

程序运行结束后会在同目录下生成以下两个文件：

文件名	说明
transactions.csv	可用 Excel 打开，查看所有交易流水
transactions.json	结构化数据保存，更适合程序读取

示例（JSON）：

{
  "balance_cents": 12345,
  "transactions": [
    {"type":1,"amount":10000,"balance_after":10000,"timestamp":1700000000},
    {"type":2,"amount":5000,"balance_after":5000,"timestamp":1700003600}
  ]
}

🧩 使用方法
1️⃣ 编译

在 PowerShell 或 CMD 中进入项目目录，例如：

cd "D:\pycharm\ATM simulator"
gcc -std=c11 -Wall -Wextra -O2 -mconsole atm.c -o atm.exe

2️⃣ 运行
.\atm.exe

📖 程序菜单说明
选项	功能
1	存款
2	取款
3	查看交易记录
4	查看余额
0	退出（并自动保存）
🧠 技术要点

全部以“分”为单位存储金额，避免浮点误差

时间戳使用 time() 保存交易时间

自动检测并加载历史记录

JSON 读写不依赖外部库，纯标准 C 实现

🧑‍💻 开发环境

编译器：GCC（MinGW / TDM-GCC 均可）

C 标准：C11

操作系统：Windows（兼容 Linux / macOS）

📦 项目结构
ATM simulator/
│
├── atm.c                 # 主程序
├── transactions.csv      # 存储的交易记录（自动生成）
├── transactions.json     # JSON 格式记录（自动生成）
└── README.md             # 项目说明文件

🧭 后续计划（可选扩展）

🔐 多账户系统 + PIN 登录

🗃️ 账户文件自动管理

🖥️ 图形界面版本（GTK / Win32）

📊 导出交易记录为 Excel (.xlsx)

📜 许可证

本项目采用 MIT License 开源协议，欢迎学习、修改与分发。
