
---

# 🏧 ATM Simulator (C)

[![Language](https://img.shields.io/badge/language-C-blue.svg)](https://en.wikipedia.org/wiki/C_%28programming_language%29)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-lightgrey.svg)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
![Status](https://img.shields.io/badge/status-stable-success.svg)
[![Last Commit](https://img.shields.io/github/last-commit/HUTcl2024/ATM-simulator.svg)](https://github.com/HUTcl2024/ATM-simulator/commits/main)

> 🏦 轻量级 **C 语言** ATM 模拟器。支持存款、取款、交易记录与自动持久化。
> Ideal for beginners to practice **file I/O**, **structs**, and **time functions**.

---

## ✨ 功能特性 | Features

| 功能                     | 说明                                             |
| ---------------------- | ---------------------------------------------- |
| 💰 存款 / Deposit        | 输入金额（支持两位小数，如 `100.50`）                        |
| 💸 取款 / Withdraw       | 自动检测余额是否足够                                     |
| 📜 交易记录 / Transactions | 显示所有交易（含时间戳与余额）                                |
| 🧮 查看余额 / Balance      | 显示当前账户余额                                       |
| 💾 数据持久化 / Persistence | 自动保存至 `transactions.csv` 与 `transactions.json` |
| 🔁 自动加载 / Auto Load    | 启动时自动恢复上次交易记录与余额                               |

---

## 🧰 使用方法 | How to Use

### 编译（Windows / MinGW 示例）

```bash
cd "D:\pycharm\ATM simulator"
gcc -std=c11 -Wall -Wextra -O2 -mconsole atm.c -o atm.exe
```

### 运行

```bash
.\atm.exe
```

启动后会看到菜单：

```text
==============================
          ATM MENU
==============================
1) Deposit
2) Withdraw
3) View transactions
4) View balance
0) Exit
Select an option:
```

---

## 🗂️ 数据文件 | Data Files

运行后会生成：

| 文件名                 | 描述                  |
| ------------------- | ------------------- |
| `transactions.csv`  | 可用 Excel 打开查看所有交易流水 |
| `transactions.json` | 程序启动时读取以恢复历史记录与余额   |

---

## 📦 项目结构 | Project Structure

```bash
ATM-simulator/
├── atm.c                 # 主程序源代码
├── transactions.csv      # 交易记录（自动生成）
├── transactions.json     # 历史记录（自动生成）
├── README.md             # 项目说明
└── .vscode/              # VS Code 配置（可选）
```

---


本项目基于 **MIT License** 开源。欢迎学习、修改与分发。
如果觉得有用，欢迎点个 ⭐️ Star！

---

