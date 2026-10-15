# 项目备忘录（示例）

> 本文件为 `ecom-details-image` Skill 自动存档的 `<slug>` 项目备忘录示例。
> 实际运行时由 agent 写入 `<CWD>/output/ecom-details-image/<slug>/prompt_memo-<slug>.md`（`<slug>` 为产品短名，如 `prompt_memo-洗衣凝珠.md`）。
> 该文件由 **核心流程第 11 步「生成项目备忘录」** 统一写出，**Brief/Prompt 与 Generate 两种模式都会执行该步**，在出图之后写出完整内容（含逐图生成记录）；文件已存在时合并/原地更新，多次调整仅保留最后生效。

---

## 一、Brief/Prompt 模式报告（不出图）

> 以下为 Brief/Prompt 模式返回的字段，也是 Generate 模式返回内容的子集。

### 1. 匹配模板
- 文件：`01-hero-image.json`
- 场景类型：白底主图 / Hero Image

### 2. Visual Brief
- 产品：轻盈蓬松洗衣凝珠（laundry-detergent-pods）
- 用途：电商主图、搜索结果卡
- 风格：clean household care，高级棚拍、通透感
- 主体占比：35-40%
- 留白：至少 45%

### 3. Final Prompt
Premium ecommerce product photography, a single pack of laundry detergent pods centered on a pure white background `#FFFFFF`, the pods translucent with visible multicolored beads inside, soft diffused studio lighting from upper left, subtle soft shadow beneath, product occupies 38% of frame, whitespace at least 45%, top-center 200x100px area left empty for platform price overlay, clean high-end look. NOT cluttered, NOT extra props.

### 4. Negative Constraints
不要添加：道具、手、水印、假 logo、额外文字、装饰元素、渐变背景。

### 5. Assumptions
- 未提供品牌色，默认使用中性高级白 + 深炭灰文字 `#2D2D2D`。
- 比例默认 `1:1`（主图）。

### 商品/营销任务追加字段

- **Conversion Driver Diagnosis**：视觉驱动型（购买决策依赖外观、质感、洁净感）。
- **Campaign Style Lock**：consistent premium ecommerce visual system across the entire image set; fixed palette of clean off-white background `#F5F1E8`, deep charcoal text `#2D2D2D`, one product-matched accent color `#7A9E7E`, and one soft secondary accent `#D4AF37`; neutral-cool studio lighting; modern geometric sans-serif headline placeholders only; consistent rounded rectangular info labels; consistent thin-line icon style; clean high-end product photography mixed with minimal infographic elements; stable product scale and placement; generous whitespace; no color palette changes, no mixed fonts, no random backgrounds, no inconsistent lighting, no mismatched icon styles.
- **Image Pack Plan（图片包计划）**：含 Hero Image Sequence 与 PDP Detail Image Sequence：
  - Hero Image Sequence：1. 一眼可懂的视觉主张 — `01-hero-image.json` — 白底主图；2. 核心功能或质感特写 — `04-detail-macro.json` — 凝珠微距；3. 使用场景匹配 — `02-lifestyle-scene.json` — 洗衣场景；4. 普通方案 vs 升级方案对比 — `09-before-after.json`；5. 优惠、物流、保障或 CTA 画面 — `05-poster-banner.json`。
  - PDP Detail Image Sequence：（涉及详情页时填写，此处略）
- **Copy Lines**：主标题「深层洁净 一颗搞定」、副标题「8倍浓缩 · 柔顺留香」、CTA「立即选购」。
- **Test Priorities**：主图 CTR vs 场景图 CTR；微距特写对质感信任度的影响。

---

## 二、Generate 模式示例（含逐图生成记录）

> 在 Brief/Prompt 全部字段基础上，追加以下生成相关内容（此处仅展示生成追加项，基础字段同上「一」）。

### 6. 选用通道 / 引擎
- 通道 B（apiz，默认）；未点名引擎、无参考图，走默认通道。

### 7. Generated Files
- `GPT-001.png` — 白底主图（01-hero-image.json）
- `GPT-002.png` — 凝珠微距（04-detail-macro.json）
- 落盘：`<CWD>/output/ecom-details-image/洗衣凝珠/prompt_memo-洗衣凝珠.md` 同级目录，全部带 `GPT-` 前缀。

### 8. 逐图生成记录
> 逐图生成记录统一并入本备忘录，与图片产物不再同目录 1:1 落盘，避免与备忘录内容重复。对同一图的多次调整/重生成**原地更新、覆盖旧值，仅保留最后生效内容**。

#### GPT-001.png（当前生效）
- 通道: B (apiz)
- 模型: apiz/gpt-image-2.5-flare
- 比例/尺寸: 1:1
- 质量档: fine
- 种子: n/a
- 参考图: 无
- 时间戳: 2026-10-14T08:30:00Z
- 提交前审核: 已确认提交

**Final Prompt**
Premium ecommerce product photography, a single pack of laundry detergent pods centered on a pure white background `#FFFFFF`, the pods translucent with visible multicolored beads inside, soft diffused studio lighting from upper left, subtle soft shadow beneath, product occupies 38% of frame, whitespace at least 45%, top-center 200x100px area left empty for platform price overlay, clean high-end look. NOT cluttered, NOT extra props.

**Negative Constraints**
不要添加：道具、手、水印、假 logo、额外文字、装饰元素、渐变背景。

#### GPT-002.png（当前生效）
- 通道: B (apiz)
- 模型: apiz/gpt-image-2.5-flare
- 比例/尺寸: 1:1
- 质量档: fine
- 种子: n/a
- 参考图: 无
- 时间戳: 2026-10-14T08:31:20Z
- 提交前审核: 已确认提交

**Final Prompt**
Extreme macro photography of a single laundry detergent pod, translucent shell with visible multicolored beads, captured on pure white background `#FFFFFF`, shallow depth of field, crisp detail on bead texture, soft studio light, premium clean look. NOT cluttered.

**Negative Constraints**
不要添加：道具、手、水印、假 logo、额外文字、渐变背景。

### 9. Assumptions / Notes
- 本次走通道 B（apiz），消耗 apiz 账户积分；出图前已报 Image Pack Plan 给用户确认。
- 依赖均可用，无缺失提示。

---

> 多轮调整示例：若后续对 `GPT-001` 重新生成（如换角度），**原地更新上方「GPT-001.png（当前生效）」记录块**（覆盖 Final Prompt / 时间戳等），不新增 `v2` 历史块；仅保留最后生效内容。
