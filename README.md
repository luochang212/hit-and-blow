# hit-and-blow

<!-- *Hit and Blow* is a game of Clubhouse Games: 51 Worldwide Classics. -->
Switch游戏 - 猜颜色 自动解算器。

猜颜色是《世界游戏大全51》中的一款小游戏。本仓库复现了该游戏的玩法，并添加了“自动解算”功能。

## Functions

已支持四种模式：

- 游戏模式 (`game.py`)：复现基本功能，可在命令行体验游戏玩法
- 自动解算 (`auto_play.py`)：计算答案的可行域，使用寻优策略逐步逼近答案
- 实验模式 (`experiment.py`)：多次重复自动解算过程，用于统计寻优策略的性能
- 作弊模式 (`hacker.py`)：和朋友联机时获得指引，快人一步得出答案 ( `д´)

## Usage

可通过两种方式运行代码：

1）通过 [pypi](https://pypi.org/project/switch-hacker/) 下载运行

```python
import switch_hacker

g = switch_hacker.game.Game()
g.main()
```

2）本地运行：以作弊模式为例

1. 在 `src` 目录下新建 `hack.py` 文件
2. 将以下代码贴入文件中保存
3. 在命令行中执行 `python hack.py`

```python
# hack.py
import switch_hacker

hk = switch_hacker.hacker.Hacker()
hk.main()
```

## Tree

文件结构

```
├── README.md
├── pyproject.toml
└── src
    ├── switch_hacker
    │   ├── __init__.py
    │   ├── base.py: 通用函数集合
    │   ├── game.py: 命令行游戏
    │   ├── auto_play.py: 自动解算器
    │   ├── experiment.py: 实验统计模块
    │   ├── hacker.py: 作弊模块
    │   └── strategy.py: 寻优策略
    └── test
        └── example.py: 示例代码
```

## Log

- [x] 命令行游戏
- [x] 自动解算器
- [x] 实验统计模块
- [x] 作弊模块
- [ ] 强化学习

<!-- ## Appendix

游戏的命令行实现：

![游戏的命令行实现.gif](./img/demo.gif) -->
