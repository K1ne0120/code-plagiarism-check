
---

# C代码树构建与重复率计算系统 / C Code Tree Construction and Similarity Calculation System

[English Version](#en) | [中文版本](#cn)

---

<a id="cn" name="中文版本"></a>

## 📝 项目简介

这是一个基于 Python 开发的 GUI 工具，旨在对 C 语言代码进行结构化分析。该系统能够将 C 源代码解析为树状结构（Abstract Syntax Tree 的简化版），支持代码预处理、语法检测（括号匹配）、可视化展示以及两份代码间的重复率（相似度）计算。

### ✨ 核心功能

* **代码树构建**：解析 `main` 函数体，识别 `if`、`for`、`while`、`switch` 等控制流语句并构建层级树结构。
* **重复率计算**：通过比较两棵代码树的结构，计算代码间的相似度，适用于简单的代码查重。
* **代码预处理**：自动移除注释（单行及多行），并将非关键字标识符统一替换为 `var` 以进行结构化对比。
* **语法检测**：实时检测代码中的小括号 `()` 和中括号 `[]` 是否匹配，并精确定位错误行号。
* **可视化展示**：集成 Graphviz 库，将复杂的代码逻辑以直观的图形化树状结构展示。
* **自动备份**：程序启动时会自动将当前的 Python 脚本备份至 `code_backups` 文件夹。

### 📂 文件结构

| 文件名 | 描述 |
| --- | --- |
| `main.py` | 程序入口，负责启动备份逻辑及 GUI 应用。 |
| `CodeTree.py` | 核心逻辑类，包含代码预处理、树构建算法、表达式解析及括号检测。 |
| `CodeTreeApp.py` | 基于 `tkinter` 的图形界面实现，包含操作面板、输出日志及图像显示。 |
| `util.py` | 工具模块，提供带时间戳的脚本自动备份功能。 |
| `test.py` | 测试脚本，用于验证代码解析逻辑的正确性。 |

### 🛠️ 环境要求

* **Python 版本**: 3.x
* **第三方库**:
* `graphviz`: 用于生成代码树图像。
* `anytree`: 用于管理和操作树形数据结构。


* **外部依赖**: 需在系统中安装 [Graphviz 软件](https://www.google.com/search?q=https://graphviz.org/download/) 并配置环境变量。

### 🚀 快速开始

1. 安装依赖库：
```bash
pip install -r requirements.txt
```


2. 运行主程序：
```bash
python main.py
```


3. 在操作面板中选择“输入代码”或使用“示例代码演示”查看效果。

---

<a id="en" name="english-version"></a>

## 📝 Project Overview

This is a Python-based GUI tool designed for the structural analysis of C language code. The system parses C source code into a tree-like structure (a simplified AST), supporting code preprocessing, syntax detection (bracket matching), visual representation, and similarity (repetition rate) calculation between two code samples.

### ✨ Key Features

* **Code Tree Construction**: Parses the `main` function body to identify control flow statements like `if`, `for`, `while`, and `switch` to build a hierarchical tree.
* **Similarity Calculation**: Compares the structures of two code trees to calculate similarity, useful for basic code plagiarism detection.
* **Code Preprocessing**: Automatically removes single-line and multi-line comments and normalizes identifiers (non-keywords) to `var` for structural comparison.
* **Syntax Detection**: Real-time detection of mismatched parentheses `()` and square brackets `[]`, providing precise error line numbers.
* **Visualization**: Integrates with Graphviz to display complex code logic as an intuitive graphical tree.
* **Automatic Backup**: Automatically backs up current Python scripts to a `code_backups` folder upon program execution.

### 📂 File Structure

| File | Description |
| --- | --- |
| `main.py` | Entry point of the application; handles backup logic and starts the GUI. |
| `CodeTree.py` | Core logic class containing code preprocessing, tree-building algorithms, and bracket detection. |
| `CodeTreeApp.py` | GUI implementation using `tkinter`, featuring an operation panel, logs, and image displays. |
| `util.py` | Utility module providing timestamped script backup functionality. |
| `test.py` | Test script for validating code parsing logic. |

### 🛠️ Requirements

* **Python Version**: 3.x
* **Libraries**:
* `graphviz`: For generating code tree images.
* `anytree`: For managing tree data structures.


* **External Dependency**: Must have [Graphviz software](https://www.google.com/search?q=https://graphviz.org/download/) installed and configured in your system's PATH.

### 🚀 Quick Start

1. Install dependencies:
```bash
pip install -r requirements.txt
```


2. Run the application:
```bash
python main.py
```


3. Use the "Input Code" buttons or "Demo Example" in the panel to start analyzing code.