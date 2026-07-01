<div align="center">

# 💪 Exercises Dataset(中文备份仓库)

**1324 个健身运动的结构化多语言数据集 · 含本地 GIF 动画演示 · 6 种语言步骤说明**

</div>

---

## ⚠️ 重要说明 · 版权与备份声明

> **本仓库仅用于备份运动演示图片(GIF),供个人学习与离线使用,不用于任何商业用途。**

- 原项目 [hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset) 因存在**多方相互冲突的版权主张**,已于 2026-06-30 通过 `git filter-repo` 将全部图片(原 `images/` 与 `videos/` 目录)从仓库及完整历史中移除,只保留数据与代码。
- 原项目数据源自 [ExerciseDB](https://exercisedb.dev/),其官方 CDN(`static.exercisedb.dev`)对部分媒体返回 `401 Unauthorized`(需授权访问)。
- 本仓库中的 **1324 张 GIF 来源于上述清理发生"之前"的社区 fork**(这些独立副本保留了原始媒体),仅作**备份**目的重新归集。
- **所有图片的版权归原始权利人所有,本仓库不主张任何版权。**
- **若您是相关图片的权利人,认为本仓库内容侵犯了您的权益,请[提交 Issue](../../issues) 或联系仓库所有者,我们将在确认后立即清理对应内容。**

---

## 📦 项目简介

本数据集收录 **1324 个健身运动**,每个运动包含:

| 内容 | 说明 |
|---|---|
| 名称 / 类别 / 部位 | 运动名称、身体部位分类 |
| 目标与肌群 | 目标肌群(target)、辅助肌群(secondary muscles) |
| 所需器材 | 哑铃、杠铃、自重等 |
| 多语言步骤说明 | 🇬🇧英 · 🇪🇸西 · 🇮🇹意 · 🇹🇷土 · 🇷🇺俄 · 🇨🇳中 |
| **GIF 动画演示** | 本地 `media/` 目录,完全离线可播放 |

## 🆚 本仓库与原仓库的区别

| 项目 | 原仓库(`hasaneyldrm`) | 本仓库(`Johnson-Jia`) |
|---|---|---|
| 演示图片 | ❌ 已移除(版权争议) | ✅ **1324 张 GIF 已备份** |
| 数据 / 页面 | ✅ | ✅(一致) |
| 离线浏览 | 无图 | **全图,完全离线** |
| 与原项目关系 | — | 独立仓库(非 fork),保留 upstream 引用 |

## 📂 目录结构

```
exercises-dataset/
├── data/
│   └── exercises.json    # 1324 条运动数据(含 6 语言说明)
├── media/                # 1324 张 GIF 动画(本仓库备份)
│   └── {media_id}.gif
├── index.html            # 交互式浏览器(双击即可离线打开)
├── setup.html            # 开发者向导(建库 SQL + API 集成示例)
└── README.md
```

## 🚀 使用方式

**直接双击 `index.html`**,即可在浏览器中离线浏览全部 1324 个运动:

- 实时搜索 / 按类别、器材、目标肌群筛选
- 无限滚动卡片网格
- 点击卡片查看详情与 6 语言步骤说明
- 所有动图均从本地 `media/` 加载,**无需联网**

## 🗂️ 数据结构

`data/exercises.json` 是一个 JSON 数组,每条记录主要字段:

| 字段 | 类型 | 说明 |
|---|---|---|
| `id` | string | 编号(如 `"0001"`) |
| `name` | string | 运动名称 |
| `category` / `body_part` | string | 身体部位 |
| `equipment` | string | 所需器材 |
| `target` | string | 主要目标肌群 |
| `muscle_group` | string | 主要协同肌群 |
| `secondary_muscles` | array | 辅助肌群 |
| `instructions` | object | `{en, es, it, tr, ru, zh}` 六语言步骤说明 |
| `media_id` | string | ExerciseDB 媒体引用 ID |
| `image` / `gif_url` | string | 本地 GIF 路径 `media/{media_id}.gif` |
| `created_at` | string | 记录创建时间(ISO 8601) |

## 📊 统计(共 1324 个运动)

**按身体部位**

| 部位 | 数量 | 部位 | 数量 |
|---|---|---|---|
| 上臂 | 292 | 胸 | 163 |
| 大腿 | 227 | 肩 | 143 |
| 背 | 203 | 小腿 | 59 |
| 腰 | 169 | 前臂 | 37 |
| 有氧 | 29 | 颈部 | 2 |

**按器材**:自重 325 · 哑铃 294 · 绳索 157 · 杠铃 154 · 杠杆机 81 · 弹力带 54 · 史密斯机 48 · 壶铃 41 · 负重 36 · 瑞士球 28 · EZ 杠 23 · 其它 83

> 约 25% 的运动不需要任何器械,适合居家训练场景。

## 🙏 数据来源与致谢

- 数据与代码源自 [hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset)
- 原始运动数据源自 [ExerciseDB](https://exercisedb.dev/)
- 多语言翻译由原项目的社区贡献者完成
- 本仓库的 GIF 备份来自清理前的社区 fork

## 📄 License

- 数据与代码沿用原项目许可,使用前请审阅 [ExerciseDB 的条款](https://exercisedb.dev/)
- **图片(GIF)版权归原作者所有,本仓库仅作备份,不用于商业用途**
- 若您是权利人,请通过 [Issues](../../issues) 联系清理
