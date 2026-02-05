# SF32LB56x 低功耗测试报告文档

本仓库包含了 SF32LB56x 系列芯片的低功耗测试报告，提供详细的功耗测试方法和参考结果。

## 📋 项目概述

**SF32LB56x** 是一颗基于 **ArmCortex-M33STAR-MC1** 处理器的大小核架构SoC芯片。本文档包含以下测试内容：

- **BLE 低功耗测试** - 蓝牙低功耗场景的详细测试方法和结果
- **BT 经典蓝牙测试** - 经典蓝牙应用场景的功耗测试数据  
- **CoreMark 性能测试** - 基准性能测试中的功耗性能分析
- **测试环境说明** - 测试所需的硬件环境、软件配置和测试工具

## 🛠 安装工具链

1. 安装 Python 3.x，并确保在命令行中执行`python --version`能显示python版本
2. 在命令行中执行 `pip install -r requirements.txt`，安装编译文档所需的工具包`sifli-docs-toolbox`

## 📖 生成文档

在文档根目录的命令行下执行下面的命令即可生成文档：

```shell
# 生成中文文档
sf-build-docs --lang zh_CN --version latest

# 生成英文文档  
sf-build-docs --lang en --version latest
```

`--lang`配置生成文档的语言，`zh_CN`为中文，`en`为英文，缺省为中文。`--version`配置版本号, 不配置则为`latest`。CI编译时会自动获取标签作为版本号

生成完成后：
- 双击`build/zh_CN/html/index.html`可以打开生成的中文文档
- 双击`build/en/html/index.html`可以打开生成的英文文档

点击[链接](https://docs.sifli.com/projects/rpt5602_sf32lb56x-low-power-measurement-report/latest/zh_CN/index.html)浏览在线文档效果 


## 📁 文档结构

```
source/
├── _static/                 # 静态资源文件
├── _templates/              # 模板文件
├── assets/                  # 共享资源
├── en/                      # 英文文档
│   ├── brief_introduction.md    # 芯片简介
│   ├── ble/                     # BLE 测试相关
│   │   ├── adv.md              # 广播测试
│   │   ├── connect.md          # 连接测试
│   │   ├── result.md           # 测试结果
│   │   └── ...
│   ├── bt/                      # 经典蓝牙测试
│   ├── coremark/                # CoreMark 性能测试
│   │   ├── result.md           # 测试结果汇总
│   │   ├── whileloop.md        # WhileLoop 测试
│   │   └── ...
│   └── test_environment/        # 测试环境说明
└── zh_CN/                   # 中文文档（结构与英文对应）
```

## 🔧 文档配置

### 项目信息
项目配置文件位于：
- `source/en/conf.py` - 英文版配置
- `source/zh_CN/conf.py` - 中文版配置

当前项目名称：
- 英文：`SF32LB56x Low Power Measurement Report`
- 中文：`SF32LB56x 低功耗测试报告`

### 自动部署
文件`.github/workflows/build-docs.yml`为GitHub Actions配置文件，推送代码后会自动触发文档编译和部署。

- 无标签的提交：以`latest`版本编译
- 有标签的提交：以标签名称为版本号编译

### 版本管理
根目录下的`version.json`为版本号列表，可在其中添加需要在版本下拉框中显示的版本号。

## 📞 联系方式

如有疑问或建议，请联系 OpenSiFli 团队。
