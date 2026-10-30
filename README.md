# 国产 AI 产品计费逻辑（参照飞书）

## 简体中文

一个帮助读懂国产 AI 计费规则、比较版本变化、判断企业影响的 Skill。用飞书案例说明四层地图：**收什么 → 怎么算 → 定多贵 → 怎么实施**。先定位变化，再解释可能原因，避免把所有账单增加都叫涨价。

使用示例：

> 使用 $ai-pricing-logic 分析这两版计费规则。把每条规则放到四层框架中，说明改了哪里、哪些没改、可能为什么、影响谁，以及企业能怎么省钱。请用通俗语言和逻辑图表达。

将本目录作为 `ai-pricing-logic` 技能目录放入支持 SKILL.md 的环境。在 Codex 中可放入个人技能目录并重新加载技能。入口：[SKILL.md](SKILL.md)；[三语逻辑图](references/framework.md)；[日期化飞书例子](references/feishu-case.md)。正文包含中、英、日三语，默认按用户语言回答，亦可要求三语输出。

技能区分事实、推断和未知；保留固定费、实际用量、持续资源和优惠过渡的差异。省钱重点是固定规则用程序、减少重复调用、管理闲置资源，并以业务成功总成本衡量，而非单纯压低点数。分析不自动执行采购、改套餐或停用生产服务。

飞书只是案例。本 Skill 非飞书或字节官方作品；历史例子不代表现行报价，未发布用户私有正文和个人笔记。

## English

**Pricing Logic of Chinese AI Products (Using Feishu as a Reference)**

A skill for reading AI billing policies, comparing versions and assessing enterprise impact. Its four-layer map is **charge scope → meter → rate → application and transition**. Locate each change before explaining possible rationale; not every higher bill is a unit-price increase.

Example:

> Use $ai-pricing-logic to compare these billing versions. Map every clause to the four layers, explain changes and retained rules, plausible reasons, affected users and cost-saving actions. Use plain language and a diagram.

Place this folder as `ai-pricing-logic` in an environment supporting SKILL.md. For Codex, use the personal skills directory and reload skills. Entry: [SKILL.md](SKILL.md); [trilingual diagrams](references/framework.md); [dated examples](references/feishu-case.md). Chinese, English and Japanese instructions are included; output follows the user's language unless multilingual delivery is requested.

The skill separates evidence, inference and unknowns; distinguishes fixed charges, actual usage, reserved resources and rollout offers. It favors deterministic code for fixed rules, fewer duplicate calls and idle resources, and total cost per successful outcome. It does not authorize purchases, plan changes or production shutdowns.

Feishu is an illustrative case. This is not an official Feishu/ByteDance product, current price list or distribution of private source text and personal notes.

## 日本語

**中国AI製品の料金設計（飛書を参考に）**

AI料金文書、版の違い、企業への影響を読むための Skill。**課金対象 → 計量方法 → 単価 → 適用と移行**の四層で変更箇所を特定し、理由の仮説を説明する。請求増をすべて単価値上げと呼ばない。

使用例：

> $ai-pricing-logic を使い、この二つの料金規則を比較してください。各条項を四層に置き、変更・据置き、考えられる理由、影響対象、節約策を平易な言葉と図で示してください。

このフォルダを `ai-pricing-logic` として SKILL.md 対応環境に配置する。Codexでは個人スキルディレクトリに置き、スキルを再読み込みする。[SKILL.md](SKILL.md)、[三言語の図](references/framework.md)、[日付付き事例](references/feishu-case.md)を参照。中国語・英語・日本語を含み、通常は利用者の言語で回答する。

根拠・推測・不明点を分離し、固定料金、実消費、継続資源、導入特典を区別する。固定処理は通常コード、重複呼出しと遊休資源を削減し、成功一件当たりの総費用で評価する。購入、プラン変更、本番停止を自動承認しない。

飛書は参考事例であり、公式製品ではない。過去の事例は現行価格ではなく、非公開原文や個人ノートを配布しない。

---

Created with the [Codex skill-creator](https://github.com/openai/skills/tree/main/skills/.system/skill-creator) workflow. Framework developed from the author's Feishu billing analysis; not an official vendor methodology.
