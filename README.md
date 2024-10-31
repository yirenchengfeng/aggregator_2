## 项目简介
```
aggregator/
├── .github/
│   └── workflows/
│       └── collect.yaml          # GitHub Actions 工作流配置文件，用于自动化代理收集
│       └── test.yaml             # GitHub Actions 工作流配置文件，用于自动化测试
├── clash/
│   ├── config.yaml               # Clash 全局配置文件
│   ├── rules.yaml                # Clash 分流规则配置
│   ├── providers/                # Clash 代理提供者目录
│   │   ├── provider1.yaml        # 代理提供者1的配置
│   │   └── provider2.yaml        # 代理提供者2的配置
│   └── scripts/
│       └── update_config.py      # 更新 Clash 配置的脚本
│       └── merge_rules.py        # 合并多个规则文件的脚本
├── cmd/
│   ├── __init__.py               # 初始化 cmd 包
│   ├── cli.py                    # 命令行接口主程序
│   ├── commands/                 # 子命令目录
│   │   ├── __init__.py           # 初始化 commands 包
│   │   ├── collect.py            # 收集代理的命令
│   │   ├── convert.py            # 转换代理格式的命令
│   │   ├── update.py             # 更新订阅的命令
│   │   ├── test.py               # 测试代理的命令
│   │   └── clean.py              # 清理无效代理的命令
│   └── utils.py                  # 命令行工具辅助函数
├── subconverter/
│   ├── __init__.py               # 初始化 subconverter 包
│   ├── converter.py              # 代理格式转换核心逻辑
│   ├── parsers/                  # 解析器目录
│   │   ├── __init__.py           # 初始化 parsers 包
│   │   ├── clash.py              # Clash 格式解析器
│   │   ├── v2ray.py              # V2Ray 格式解析器
│   │   ├── ss.py                 # Shadowsocks 格式解析器
│   │   ├── ssr.py                # ShadowsocksR 格式解析器
│   │   ├── trojan.py             # Trojan 格式解析器
│   │   └── base.py               # 基础解析器类
│   ├── generators/               # 生成器目录
│   │   ├── __init__.py           # 初始化 generators 包
│   │   ├── clash.py              # Clash 配置生成器
│   │   ├── v2ray.py              # V2Ray 配置生成器
│   │   ├── ss.py                 # Shadowsocks 配置生成器
│   │   ├── ssr.py                # ShadowsocksR 配置生成器
│   │   ├── trojan.py             # Trojan 配置生成器
│   │   └── base.py               # 基础生成器类
│   ├── emoji.py                  # 表情符号处理模块
│   └── utils.py                  # 转换器通用工具函数
├── subscribe/
│   ├── __init__.py               # 初始化 subscribe 包
│   ├── manager.py                # 订阅管理主程序
│   ├── validator.py              # 订阅链接验证模块
│   ├── updater.py                # 订阅更新模块
│   ├── storage.py                # 订阅存储管理模块
│   └── models/                   # 订阅数据模型目录
│       ├── __init__.py           # 初始化 models 包
│       └── subscription.py       # 订阅数据模型定义
├── tools/
│   ├── __init__.py               # 初始化 tools 包
│   ├── crawler.py                # 代理爬取工具
│   ├── formatter.py              # 数据格式化工具
│   ├── speed_test.py             # 代理速度测试工具
│   ├── geo_ip.py                 # IP 地理位置查询工具
│   ├── encryption.py             # 加密解密工具
│   └── network.py                # 网络工具函数
├── tests/
│   ├── __init__.py               # 初始化 tests 包
│   ├── test_converter.py         # 测试代理转换功能
│   ├── test_subscribe.py         # 测试订阅管理功能
│   ├── test_crawler.py           # 测试爬虫功能
│   ├── test_speed.py             # 测试速度测试功能
│   └── test_utils.py             # 测试通用工具函数
├── config/
│   ├── __init__.py               # 初始化 config 包
│   ├── settings.py               # 全局设置文件
│   ├── logging.py                # 日志配置文件
│   └── constants.py              # 常量定义文件
├── docs/
│   ├── installation.md           # 安装说明文档
│   ├── usage.md                  # 使用说明文档
│   ├── api.md                    # API 文档
│   └── contributing.md           # 贡献指南
├── scripts/
│   ├── install.sh                # 安装脚本
│   ├── update.sh                 # 更新脚本
│   └── clean.sh                  # 清理脚本
├── .dockerignore                 # Docker 忽略文件配置
├── .gitignore                    # Git 忽略文件配置
├── Dockerfile                    # Docker 构建文件
├── docker-compose.yml            # Docker Compose 配置文件
├── LICENSE                       # 项目许可证文件
├── README.md                     # 项目说明文档
├── requirements.txt              # Python 依赖包列表
├── setup.py                      # 项目安装和分发配置
├── clash.ico                     # 应用程序图标
└── main.py                       # 项目主入口文件
```

## 节点存储位置
```
https://gist.github.com/PangTouY00/2efa3f1165304204299a6e091eee070f
```

## V2ray订阅
```
https://gist.githubusercontent.com/PangTouY00/2efa3f1165304204299a6e091eee070f/raw/ecde221dcb6b24d11f48b0eacf5cce43abf95ff6/v2ray.txt
```

## clash订阅
```
https://gist.githubusercontent.com/PangTouY00/2efa3f1165304204299a6e091eee070f/raw/ecde221dcb6b24d11f48b0eacf5cce43abf95ff6/clash.yaml
```

## 功能
打造免费代理池，爬一切可爬节点
> 拥有灵活的插件系统，如果目标网站特殊，现有功能未能覆盖，可针对性地通过插件实现

> 欢迎 Star 及 PR。对于质量较高且普适的爬取目标，亦可在 Issues 中列出，将在评估后选择性添加

## 使用方法
> 略，自行探索。我才不会告诉你入口是 `collect.py` 和 `process.py`

## 免责申明
+ 本项目仅用作学习爬虫技术，请勿滥用，不要通过此工具做任何违法乱纪或有损国家利益之事
+ 禁止使用该项目进行任何盈利活动，对一切非法使用所产生的后果，本人概不负责
