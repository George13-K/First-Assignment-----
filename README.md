# 小小烧鱼通讯录小程序

一个简洁的微信小程序，用于管理联系人信息，支持联系人添加、编辑、删除、搜索及头像、背景设置等功能。

## 项目概述
小小烧鱼通讯录是一款基于微信小程序的通讯录管理工具，通过云数据库存储联系人信息，支持基本的通讯录操作。用户可以新增联系人、设置头像、编辑或删除联系人。

## 功能特性
- **联系人管理**：添加、编辑、删除联系人。
- **头像和背景设置**：支持选择头像和背景图片。
- **快速搜索**：搜索栏实时筛选联系人。
- **字母分组与快捷滚动**：首字母分组及字母索引。
- **微信授权登录**：支持微信授权获取用户头像和昵称。
  
## 安装与使用

### 在微信开发者工具中导入项目
1. 打开微信开发者工具，选择“导入项目”。
2. 设置 AppID 和云开发环境 ID。

### 启动云开发
1. 启用云开发服务，并在数据库中创建 `contacts` 集合，用于存储联系人信息。

### 配置云数据库集合
1. 创建 `contacts` 集合，包含字段：`name`、`phone`、`email`、`address`、`avatar`、`background`、`remark`。

### 运行项目
1. 在微信开发者工具中，点击“预览”按钮即可运行项目。

## 注意事项
- 在 `project.config.json` 中配置 `cloudfunctionRoot` 和 `packNpmManually`，以确保云函数路径正确。
- 如需扩展功能，请在云开发控制台中添加相应的数据库字段或云函数。

## 贡献指南
欢迎提交 Pull Requests！如需修复 Bug 或新增功能，请在 issues 中提出，感谢您的贡献！


## 文件结构
```plaintext
|-- miniprogram/
|   |-- pages/
|   |   |-- index/                   # 主页面 - 展示联系人列表
|   |   |-- addContact/              # 添加联系人页面
|   |   |-- card/                    # 联系人详情卡片页面
|   |-- utils/
|       |-- cloudfunctions.js        # 云函数调用
|-- cloudfunctions/                  # 云函数代码目录
|   |-- addContact/                  # 添加联系人云函数
|   |-- deleteContact/               # 删除联系人云函数
|-- project.config.json              # 项目配置文件
|-- README.md                        # 项目说明文件