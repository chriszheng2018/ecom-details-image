# Brief / Prompt 模式报告（示例）

> 本文件为 `ecom-details-image` Skill 在 **Brief/Prompt 模式（不出图）** 下自动存档的报告示例。
> 实际运行时由 agent 写入 `<CWD>/output/ecom-details-image/<slug>/brief_prompt.md`。

## 1. 匹配模板
- 文件：`01-hero-image.json`
- 场景类型：白底主图 / Hero Image

## 2. Visual Brief
- 产品：轻盈蓬松洗衣凝珠（laundry-detergent-pods）
- 用途：电商主图、搜索结果卡
- 风格：clean household care，高级棚拍、通透感
- 主体占比：35-40%
- 留白：至少 45%

## 3. Final Image Prompt
Premium ecommerce product photography, a single pack of laundry detergent pods centered on a pure white background `#FFFFFF`, the pods translucent with visible multicolored beads inside, soft diffused studio lighting from upper left, subtle soft shadow beneath, product occupies 38% of frame, whitespace at least 45%, top-center 200x100px area left empty for platform price overlay, clean high-end look. NOT cluttered, NOT extra props.

## 4. Negative Constraints
不要添加：道具、手、水印、假 logo、额外文字、装饰元素、渐变背景。

## 5. Assumptions
- 未提供品牌色，默认使用中性高级白 + 深炭灰文字 `#2D2D2D`。
- 比例默认 `1:1`（主图）。

---

## 商品/营销任务追加字段

### Conversion Driver Diagnosis
视觉驱动型（购买决策依赖外观、质感、洁净感）。

### Campaign Style Lock
consistent premium ecommerce visual system across the entire image set; fixed palette of clean off-white background `#F5F1E8`, deep charcoal text `#2D2D2D`, one product-matched accent color `#7A9E7E`, and one soft secondary accent `#D4AF37`; neutral-cool studio lighting; modern geometric sans-serif headline placeholders only; consistent rounded rectangular info labels; consistent thin-line icon style; clean high-end product photography mixed with minimal infographic elements; stable product scale and placement; generous whitespace; no color palette changes, no mixed fonts, no random backgrounds, no inconsistent lighting, no mismatched icon styles.

### Hero Image Sequence
1. 一眼可懂的视觉主张 — `01-hero-image.json` — 白底主图
2. 核心功能或质感特写 — `04-detail-macro.json` — 凝珠微距
3. 使用场景匹配 — `02-lifestyle-scene.json` — 洗衣场景
4. 普通方案 vs 升级方案对比 — `09-before-after.json`
5. 优惠、物流、保障或 CTA 画面 — `05-poster-banner.json`

### PDP Detail Image Sequence
（涉及详情页时填写，此处略）

### Copy Lines
- 主标题：「深层洁净 一颗搞定」
- 副标题：「8倍浓缩 · 柔顺留香」
- CTA：「立即选购」

### Test Priorities
- 主图 CTR vs 场景图 CTR
- 微距特写对质感信任度的影响
