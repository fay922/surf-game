# 🏄 Surf（Let's Surf）

Microsoft Edge 浏览器断网小游戏 **Surf**（`edge://surf`）的独立运行版本。

原版游戏由 Microsoft 开发。本仓库中的文件提取自 Microsoft Edge 并做了少量修改，使其可以脱离 Edge 浏览器独立运行，修改部分参考了 [jackbuehner/MicrosoftEdge-Surf](https://github.com/jackbuehner/MicrosoftEdge-Surf)。

<p align="center">
  <a href="https://fay922.github.io/surf-game/"><strong>▶ 在线试玩</strong></a>
  ·
  <a href="#features">功能</a>
  ·
  <a href="#controls">操作</a>
  ·
  <a href="#license">许可</a>
</p>

## 在线试玩

**https://fay922.github.io/surf-game/**

（部署于 GitHub Pages，`main` 分支根目录）

## 功能<a id="features"></a>

- **无尽模式（Endless）**：尽可能冲得更远，躲避障碍与海怪
- **计时赛（Time Trials）**：以最快速度到达终点，收集金币可缩短时间，赛道固定，可反复挑战最短路线
- **穿门模式（Zig Zag）**：连续穿过尽可能多的浮标门，漏门会中断连击，但可继续玩到生命耗尽
- **最高分记录**：每个模式独立记录最高分，刷新纪录时会有提示，可随时重置统计
- **降速模式**：放慢游戏节奏，便于上手或练习
- **双主题**：夏日冲浪主题 / 冬季滑雪主题
- **多输入支持**：键盘、鼠标、触屏、手柄
- **彩蛋**：隐藏了多个小惊喜

## 操作说明<a id="controls"></a>

| 输入 | 动作 |
| --- | --- |
| ↑ / `W` | 上浮 |
| ↓ / `S` | 下潜 |
| ← / → 或 `A` / `D` | 左右转向 |
| `F` / 右键 / 双击 | 使用加速 |
| 空格 / 回车 | 开始 / 暂停 |
| `Esc` | 设置菜单 |
| 触屏 | 滑动 / 点按转向，双击加速 |

> 具体操作可在游戏内 **How to play** 菜单查看。

## 游戏模式<a id="modes"></a>

| 模式 | 目标 | 计分 |
| --- | --- | --- |
| Endless | 冲得越远越好 | 距离（米） |
| Time Trials | 最快到达终点 | 用时 − 2 × 金币数 |
| Zig Zag | 连续穿门 | 连续穿过门数 |

## 项目结构

```
surf-game/
├── index.html              # 入口页面
├── manifest.json           # PWA 清单
├── browserconfig.xml       # 浏览器磁贴配置
├── LICENSE                 # BSD-3-Clause
├── README.md
└── resources/
    ├── css/                # 界面样式
    ├── icons/              # 站点图标
    ├── js/                 # 游戏脚本（含 surf.bundle.js）
    ├── surf/               # 冲浪主题美术资源
    └── ski/                # 滑雪主题美术资源
```

## 本地运行

无需构建，任意静态服务器均可：

```bash
# 方式一：Python
python -m http.server 8000
# 访问 http://localhost:8000

# 方式二：Node
npx serve .
```

也可以直接用浏览器打开 `index.html`（部分浏览器对 `file://` 有安全限制，建议用本地服务器）。

## 部署到 GitHub Pages

1. Fork / 推送本仓库到 GitHub
2. 进入仓库 **Settings → Pages**
3. **Source** 选择 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`
4. 保存后等待构建，访问 `https://<你的用户名>.github.io/surf-game/`

## 版权与许可<a id="license"></a>

- 游戏代码与美术资源 © **Microsoft Corporation**，保留所有权利。
- 源码文件头声明其使用 **BSD 风格许可** 授权，详见 [LICENSE](./LICENSE)（BSD 3-Clause）。
- 原版游戏中的 **Credits**（游戏菜单内）列有完整致谢名单。

## 免责声明

本仓库为粉丝向的独立运行部署，**与 Microsoft 无关联，亦未获得其官方认可**。游戏名称、图标与美术资源可能受 Microsoft 商标与版权保护。本项目仅供学习与个人娱乐使用，请勿用于商业用途。若权利人提出要求，本仓库将立即下架。

## 致谢

- **Microsoft** — 原版游戏《Let's Surf》
- **jackbuehner/MicrosoftEdge-Surf** — 独立化改造与移动端适配参考

## 贡献

欢迎通过 Issue / Pull Request 提交问题与改进。提交前请确认修改不破坏原有功能。
