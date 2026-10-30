# 国产 AI 产品计费逻辑（参照飞书）

## 简体中文

一个帮助读懂国产 AI 收费结构与设计逻辑的 Skill。它用四层地图拆解规则：**收什么 → 怎么算 → 定多贵 → 怎么实施**，并从成本、客户价值、竞争替代、理解难度和实施复杂度判断设计是否合理。飞书仅作为产品案例参照。

使用示例：

> 使用 $ai-pricing-logic 分析这份计费规则。把每项收费放入四层框架，说明为什么采用这种计价方式、结构是否合理、适用边界和待核实事项。请用通俗语言和逻辑图表达。

将本目录作为 `ai-pricing-logic` 技能目录放入支持 SKILL.md 的环境。在 Codex 中可放入个人技能目录并重新加载技能。入口：[SKILL.md](SKILL.md)；[三语逻辑图](references/framework.md)。正文包含中、英、日三语，默认按用户语言回答，也可要求三语输出。

本 Skill 区分事实、推断和未知，并将收费对象、计量单位、单价和适用条件分开分析。它不是飞书或字节官方作品，飞书案例也不代表所有产品都采用相同方法。

## English

**Pricing Logic of Chinese AI Products (Using Feishu as a Reference)**

A skill for interpreting Chinese AI pricing structures and design logic. Its four-layer map is **charge scope → meter → rate → application**. It evaluates each layer through cost coverage, customer value, competition and alternatives, clarity, and implementation complexity. Feishu is used only as a product reference.

Example:

> Use $ai-pricing-logic to analyze this pricing policy. Map every charge to the four layers, explain why the metering design may have been chosen, assess whether the structure is coherent, and state its boundaries and unknowns. Use plain language and a diagram.

Place this folder as `ai-pricing-logic` in an environment supporting SKILL.md. For Codex, use the personal skills directory and reload skills. Entry: [SKILL.md](SKILL.md); [trilingual diagrams](references/framework.md). Chinese, English and Japanese instructions are included; output follows the user's language unless multilingual delivery is requested.

The skill separates facts, inference and unknowns, then analyzes charge scope, meter, rate and application independently. It is not an official Feishu or ByteDance product, and the reference does not imply that every product uses the same method.

## 日本語

**中国AI製品の料金設計（飛書を参考に）**

中国AI製品の料金構造と設計ロジックを理解するためのSkill。**課金対象 → 計量方法 → 単価 → 適用**の四層で整理し、原価回収、顧客価値、競争と代替、理解しやすさ、実装複雑性から妥当性を考える。飛書は製品事例の参照としてのみ使う。

使用例：

> $ai-pricing-logicを使って、この料金規則を分析してください。各費目を四層に置き、この計量方式を採る理由、構造の妥当性、適用範囲、要確認事項を平易な言葉と図で示してください。

このフォルダを`ai-pricing-logic`としてSKILL.md対応環境に配置する。Codexでは個人スキルディレクトリに置き、スキルを再読み込みする。[SKILL.md](SKILL.md)と[三言語の図](references/framework.md)を参照。中国語・英語・日本語を含み、通常は利用者の言語で回答する。

このSkillは事実、推測、不明点を分け、課金対象、計量単位、単価、適用条件を別々に分析する。飛書・ByteDanceの公式製品ではなく、参照事例が全製品に共通するとはみなさない。

---

Created with the [Codex skill-creator](https://github.com/openai/skills/tree/main/skills/.system/skill-creator) workflow. Feishu is used as a product reference; this is not an official vendor methodology.
