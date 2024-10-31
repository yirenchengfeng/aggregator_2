```
aggregator/
├── .github/
│   └── workflows/
│       └── collect.yaml  # GitHub Actions 工作流配置文件
├── clash/
│   ├── config.yaml       # Clash 配置文件
│   └── rules.yaml        # Clash 规则配置
├── cmd/
│   ├── __init__.py       # 初始化 cmd 包
│   ├── cli.py            # 命令行接口主程序
│   └── utils.py          # 命令行工具辅助函数
├── subconverter/
│   ├── __init__.py       # 初始化 subconverter 包
│   ├── converter.py      # 代理格式转换核心逻辑
│   └── emoji.py          # 表情符号处理模块
├── subscribe/
│   ├── __init__.py       # 初始化 subscribe 包
│   ├── manager.py        # 订阅管理主程序
│   └── validator.py      # 订阅链接验证模块
├── tools/
│   ├── __init__.py       # 初始化 tools 包
│   ├── crawler.py        # 代理爬取工具
│   └── formatter.py      # 数据格式化工具
├── .dockerignore         # Docker 忽略文件配置
├── .gitignore            # Git 忽略文件配置
├── Dockerfile            # Docker 构建文件
├── LICENSE               # 项目许可证文件
├── README.md             # 项目说明文档
├── requirements.txt      # Python 依赖包列表
├── clash.ico             # 应用程序图标
└── main.py               # 项目主入口文件
```

## https://gist.github.com/PangTouY00/2efa3f1165304204299a6e091eee070f

## https://gist.githubusercontent.com/PangTouY00/2efa3f1165304204299a6e091eee070f/raw/ecde221dcb6b24d11f48b0eacf5cce43abf95ff6/v2ray.txt

## 功能
打造免费代理池，爬一切可爬节点
> 拥有灵活的插件系统，如果目标网站特殊，现有功能未能覆盖，可针对性地通过插件实现

> 欢迎 Star 及 PR。对于质量较高且普适的爬取目标，亦可在 Issues 中列出，将在评估后选择性添加

## 使用方法
> 略，自行探索。我才不会告诉你入口是 `collect.py` 和 `process.py`

## 免责申明
+ 本项目仅用作学习爬虫技术，请勿滥用，不要通过此工具做任何违法乱纪或有损国家利益之事
+ 禁止使用该项目进行任何盈利活动，对一切非法使用所产生的后果，本人概不负责
