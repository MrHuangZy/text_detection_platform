# 🛡️ 基于BERT的言论挖掘与检测系统

本项目是一款集攻击性言论识别、评论挖掘、数据可视化、用户行为分析于一体的中文文本检测平台。系统基于 BERT 模型构建语义分类器，结合 PyQt5 构建本地化图形界面，支持从社交平台抓取数据、分析评论健康性，并具备较强的工程可部署性。

---

## 🚀 项目特性

- 🤖 **语义检测能力强**：采用 BERT 模型深度微调，精准识别攻击性言论
- 💻 **图形界面本地运行**：基于 PyQt5 开发，无需 Web 环境，运行即用
- 🔍 **数据自动采集**：支持社交平台评论爬取，语料更新便捷
- 📊 **多维度可视化**：统计攻击性言论比例、检测趋势、用户健康评分等
- 🧩 **模块化架构设计**：代码结构清晰，便于扩展、维护与打包部署

---

## 🗂️ 项目结构

text_detection_platform/
 ├── main.py                # 程序入口（登录界面）
 ├── home.py                # 主窗口导航
 ├── register.py            # 用户注册界面
 ├── login_backend.py       # 登录逻辑处理
 ├── module_detection.py    # 攻击性言论检测模块（基于 BERT）
 ├── module_user.py         # 用户行为与评分计算模块
 ├── module_health.py       # 用户健康评估模块
 ├── module_visual.py       # 可视化模块（使用 matplotlib）
 ├── module_crawl.py        # 评论数据抓取模块（requests）
 ├── captcha_util.py        # 验证码生成与验证工具
 ├── config.ini             # 系统配置文件
 ├── db_config.ini          # 数据库配置
 ├── simhei.ttf             # 中文字体文件
 ├── captcha.png            # 登录页面验证码图
 ├── roberta-base-cold/     # 微调后的 BERT 模型文件夹
 ├── main.spec              # PyInstaller 打包配置文件
 └── test.py                # 测试脚本

---

## 💻 环境依赖

建议使用 Python 3.8+ 环境，推荐使用虚拟环境（如 Anaconda 或 venv）管理依赖。

安装依赖：

```bash
pip install -r requirements.txt
```

## 📈 功能模块说明

| 模块名称           | 功能描述                                     |
| ------------------ | -------------------------------------------- |
| `module_detection` | 使用 PyTorch 加载 BERT 模型，识别攻击性文本  |
| `module_user`      | 统计用户评论行为，生成“网络健康评分”         |
| `module_health`    | 综合评估评论频率、攻击性比例等，生成风险等级 |
| `module_crawl`     | 基于关键词抓取社交平台评论，实现数据自动更新 |
| `module_visual`    | 绘制饼图、折线图等统计结果，提升数据可解释性 |



------

## 📊 示例界面

<img src=".\image-20250731111856789.png" alt="image-20250731111856789" style="zoom:150%;" />

<img src=".\image-20250731111931858.png" alt="image-20250731111931858" style="zoom:150%;" />

<img src=".\image-20250731111936417.png" alt="image-20250731111936417" style="zoom:120%;" />

<img src=".\image-20250731111940047.png" alt="image-20250731111940047" style="zoom:120%;" />

<img src=".\image-20250731111944313.png" alt="image-20250731111944313" style="zoom:130%;" />
