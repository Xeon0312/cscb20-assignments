# 🎓 Python Flask - Student Management System

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

**基于 Flask 的学生成绩管理系统**

</div>

---

## 📖 项目简介

这是一个基于 **Flask** 框架开发的学生成绩管理系统，实现了用户认证、成绩管理、权限控制等核心功能。

系统使用 **SQLite** 数据库存储数据，支持管理员和普通用户两种角色，提供完整的成绩增删改查功能。

## ✨ 功能特性

### 🔐 用户认证
- 用户登录/登出
- Session 管理
- 角色权限控制（管理员/普通用户）

### 📊 成绩管理
- 查看学生成绩列表
- 编辑学生成绩
- 按用户名查询
- 成绩数据持久化

### 👥 权限系统
- **管理员**：可以编辑所有学生成绩
- **普通用户**：只能查看自己的成绩

## 🛠️ 技术栈

| 技术 | 用途 |
|------|------|
| Python 3 | 后端开发语言 |
| Flask | Web框架 |
| Flask-SQLAlchemy | ORM数据库操作 |
| SQLite | 轻量级数据库 |
| HTML/CSS | 前端界面 |
| Jinja2 | 模板引擎 |

## 📁 项目结构

```
python_flask_a3/
├── app.py                 # 主应用文件
├── assignment3.db         # SQLite数据库
├── logindatabase.db.sql   # 数据库SQL脚本
├── requirment.txt         # 依赖包列表
├── templates/             # HTML模板
│   ├── home.html
│   ├── login.html
│   └── editmarks.html
└── static/                # 静态资源
    ├── css/
    └── js/
```

## 🚀 快速开始

### 前置要求

- Python 3.6+
- pip

### 安装步骤

```bash
# 克隆仓库
git clone https://github.com/Xeon0312/python_flask_a3.git

# 进入项目目录
cd python_flask_a3

# 安装依赖
pip install -r requirment.txt

# 运行应用
python app.py

# 访问 http://localhost:5000
```

## 📋 依赖包

```
Flask
Flask-SQLAlchemy
markupsafe
```

## 🎯 核心功能

### 路由说明

| 路由 | 方法 | 功能 |
|------|------|------|
| `/` | GET | 首页，显示用户信息 |
| `/login` | GET, POST | 用户登录 |
| `/logout` | GET | 用户登出 |
| `/editmarks/<studentname>` | GET, POST | 编辑学生成绩 |

### 数据库结构

```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    username VARCHAR(50),
    password VARCHAR(50),
    role VARCHAR(20),
    marks INTEGER
);
```

## 🔒 安全说明

> ⚠️ **注意**：本项目为学习用途，存在以下安全问题，请勿用于生产环境：
> - SQL注入风险（使用了字符串格式化）
> - 密码明文存储
> - 简单的Session管理

## 📝 学习要点

- Flask 基础路由和视图
- Flask-SQLAlchemy ORM使用
- Session 管理和用户认证
- Jinja2 模板渲染
- SQLite 数据库操作
- 表单处理和POST请求

## 🤝 课程信息

- **课程**：CSC B20 / 相关Web开发课程
- **作业**：Assignment 3
- **主题**：Web应用开发 - Flask框架

## 📄 许可证

本项目为课程作业，仅供学习参考使用。

---

<div align="center">

**Made with ❤️ using Flask**

</div>
