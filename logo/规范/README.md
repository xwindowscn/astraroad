# 这是 Astraroad 官方标志（Official）

**生效日期：2026-11-07 ｜ 编号：D-202611-007 ｜ 版本 v1.0**

本目录（`_official/`）内的文件是 **Astraroad 唯一现行标志资产**。
`品牌资产库/astraroad-logo-20261106/新四向/` 下的其他所有目录（11 四向汇流、12 四方路网、
13 四瓣环、14 四人环、15 圆角四向、16 双色四向、17 四向星芒、19 四弧内收、
11S–19S 方形族、破格-20A-20B-20C 等）以及 `新四向/` 根目录下的对比板，
**全部是历史探索稿，不得再用于任何交付、印刷或上线**。

## 先读哪份

| 要做什么 | 看哪份 |
|---|---|
| 判断「这个用法对不对」 | `品牌规范.md`（§2 变体、§3 最小尺寸、§4 留白、§6 错误用法） |
| 拿文件去用 | `png/` 选尺寸，或直接用 SVG |
| 看整体长什么样 | `预览-全家福.png` |
| 查是谁改的、能不能复现 | `自检记录.md`、`_build/` |
| 看上线效果 | `验收截图/` |

## 一分钟取用

| 场景 | 取这个 |
|---|---|
| 网页头部（深底） | `astraroad-horizontal-on-dark.svg` |
| 网页居中大标（深底） | `astraroad-vertical-on-dark.svg` |
| 白纸文件、PPT 浅色母版 | `astraroad-horizontal.svg` |
| 单色印刷 / 打标 / 传真 | `astraroad-horizontal-mono.svg` |
| 深色照片上 | `astraroad-horizontal-mono-white.svg` |
| 方形图标 / App 图标 | `astraroad-icon.svg`（≥20px）或 `astraroad-icon-micro16.svg`（16px） |
| 浏览器页签 | `favicon.ico` |
| iOS 主屏 | `apple-touch-icon-180.png` |

三条不能破的线：**不拉伸、不加描边、留白 ≥ 图标高 ÷ 4**。
16px 档只能用 `icon-micro16`——标准形在 16px 中心孔只剩 1px，四块会糊成一团（实证见 `验收截图/06-…png`）。

## 重新生成

```bash
cd /Users/john/Desktop/AIfolder/公司事务/设计部
/usr/bin/python3 工具/build_astraroad_official.py svg                 # SVG + 作业表
~/.venvs/webscrape/bin/python3 工具/render_svg_batch.py \
    品牌资产库/astraroad-logo-20261106/新四向/18-四向航道/_official/_build/manifest.json
/usr/bin/python3 工具/build_astraroad_official.py final               # favicon.ico + 文件清单
/usr/bin/python3 工具/check_astraroad_assets.py                        # 门禁，须 ALL PASS
```

图形取自 `../icon.svg`、`../icon-micro16.svg`（业主定稿，只读）；构建时脚本会复算并与
锁定文件逐字比对，不一致直接报错。

> 对外正式使用（印刷、商标申请、对外发布）前须经决策人确认；商标申请前另需法务部做近似检索。
