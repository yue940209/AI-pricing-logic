---
name: ai-pricing-logic
description: 分析国产 AI 产品的计费设计，参照飞书产品案例，按收什么、怎么算、定多贵、怎么实施四层定位规则，解释收费结构、设计取舍与适用边界。Analyze Chinese AI pricing structures using Feishu as a product reference. 中国AI製品の料金設計を飛書の製品事例を参考に分析する。用于定价结构拆解和收费方案分析，不用于自动采购或改套餐。
---

# 国产 AI 产品计费逻辑（参照飞书）

## 简体中文

### 目的与使用

把计费文档放进一张定价地图，回答四个问题：客户在为什么付费、账单按什么计算、每单位多少钱、规则如何适用。适用于读懂现有收费规则或评估一个收费方案。飞书只作为产品案例参照，不代表全部国产 AI 产品的统一规律。

默认使用用户语言；用户要求三语时输出中文、英文、日文，并保持事实、费率和限定条件一致。写得通俗：先给结论和地图，再给表格与细节；术语首次出现时解释，减少理解负担。

### 先确定证据

读取用户提供的正文、合同、价目表和既有分析，记录适用时间、单位、币种与来源。正文、摘要、网页自动速览和合同不是同等级证据；如有冲突，指出冲突并以实际适用的正文与合同为准。用户已提供正文或要求不访问网页时，不重复浏览；如果用户要求核实当前规则且缺少原文，查询官方来源或经授权的已登录会话。

将规则事实、分析推断和待核实信息分开。不要因为名称相似就假定收费口径相同，也不要从单个案例推断厂商一定会采取某种策略。解释设计目的时，给出可能机制和替代解释，不断言刻意不透明、生态分成或未来涨价。

### 四层地图

| 层 | 问什么 | 飞书产品案例可参照的内容 | 分析动作 |
|---|---|---|---|
| ① 收什么 | 客户为哪项服务付钱？ | 使用资格、任务执行、持续运行与存储 | 拆分每项服务，说明套餐包含什么、额外收费什么 |
| ② 怎么算 | 什么单位决定账单？ | 套餐、席位、次数、单元格、分钟、实际资源、开机天数 | 区分标准单位、实际资源和混合方式；明确成功条件、取整、去重与触发条件 |
| ③ 定多贵 | 每单位费率是多少？ | 每次点数、模型与工具费率、套餐人民币价格 | 分开点数费率与实际采购价；说明基础价、附加价和总价的关系 |
| ④ 怎么实施 | 谁能用、什么时候适用、如何抵扣？ | 权限范围、共享方式、额度有效期、扣减顺序、赠点和暂免 | 列出适用对象、开始与结束条件；不把局部规则扩展到全部功能 |

这是按问题分层的分析工具，不宣称穷尽所有定价因素。一个产品同时涉及四层很正常；以一笔费用或一条规则为分析单位。套餐包含的服务归①，计量单位归②，套餐或单位价格归③，资格与抵扣条件归④。

### 判断为什么采用这种方式

- 工作量稳定：按次、按条或按分钟容易理解，也便于预算和核账。
- 单次任务差异大：模型、工具、上下文和执行步骤的消耗不同，实际资源计价更容易匹配成本。
- 资源持续占用：运行环境、开机时长和存储有独立成本，适合按时间或容量计费。
- 客户价值差异明显：席位、功能包或分层套餐可让不同用户按所需能力购买。
- 新功能价值尚未稳定：试用、赠送或暂免可以降低体验门槛，但应明确适用范围和结束条件。
- 规则需要落地：权限、共享、抵扣顺序和合同条件决定同一标价最终如何形成账单。

把每个原因放回对应层，不要把计量方式、促销和适用条件当成同一层的 MECE 分类。再分别检查五个评价维度：成本能否覆盖、客户是否感到有价值、竞争与替代方案、规则是否容易理解和控制、实施复杂度是否合理。这些是评价维度，彼此可以相关。

### 分析与输出

先把每条规则放进四层，再回答：结构是否完整；收费对象和计量单位是否匹配；单价是否与价值和成本相称；适用条件是否清楚；哪些结论仍需核实。

按任务规模输出：一句话结论；四层映射与逻辑图；设计逻辑与可能的替代解释；对客户理解、使用行为和预算方式的影响；适用边界与待核实事项。用户只问局部时，不强制生成完整长报告。图用 Mermaid，节点按四层组织；厂商目的和潜在影响标为推断。可复用[三语框架图](references/framework.md)。

## English

### Purpose and evidence

Map an AI pricing document to four questions: what the customer buys, what drives the bill, how much each unit costs, and how the rules apply. Use it to interpret a pricing policy or assess a proposed pricing design. Feishu is a product reference, not a universal rule for Chinese AI products.

Respond in the user's language. When three languages are requested, keep Chinese, English and Japanese facts, rates and qualifications aligned. Lead with a plain conclusion and map, then add tables and detail.

Read the supplied policy text, contracts, price sheets and prior analysis. Record applicability, units, currency and sources. Full text, summaries, automated previews and contracts are not equal evidence. Surface conflicts and rely on the governing text and contract. Do not browse again when the user has supplied the text or asked not to browse. If the user asks to verify a current rule and the source is missing, use official material or an authorized signed-in session.

Separate facts, inferences and unknowns. Similar labels do not prove identical billing logic, and one product example does not prove a vendor-wide strategy. Give plausible mechanisms and alternatives instead of asserting deliberate opacity, ecosystem revenue sharing or future price increases.

### Four-layer map

| Layer | Question | Feishu product reference | Analysis |
|---|---|---|---|
| 1. Charge scope | What service is purchased? | Entitlements, task execution, reserved runtime and storage | Separate services and state what is included or charged additionally |
| 2. Meter | What unit drives billing? | Packages, seats, events, cells, minutes, actual resources, powered-on days | Identify standard units, actual usage or hybrids; capture success, rounding, deduplication and triggers |
| 3. Rate | What does each unit cost? | Credits per event, model and tool rates, package currency price | Separate credit rates from purchase price and show the relationship among base, add-on and total price |
| 4. Application | Who is eligible, when does it apply, and how are balances used? | Access, sharing, expiry, deduction order, promotions and exemptions | Identify eligible parties and start/end conditions; do not generalize a local rule |

This is a hierarchy of questions, not an exhaustive pricing theory. Analyze each charge or clause; one product can involve all four layers. Included services belong in 1, the metering unit in 2, prices in 3, and eligibility or deduction rules in 4.

### Explain the design choice

- Stable workloads support simple event, item or time rates that are easy to understand and budget.
- Variable tasks may need actual model, tool, context and compute usage to align the bill with cost.
- Reserved runtime and storage create continuing costs suited to time or capacity rates.
- Different customer value can support seats, feature bundles or tiered packages.
- New features may use trials, credits or temporary exemptions to lower the entry barrier, with clear scope and end conditions.
- Access, sharing, deduction order and contracts determine how a list price becomes an actual bill.

Place each mechanism in its relevant layer rather than treating meters, promotions and application rules as peer MECE categories. Evaluate every layer for cost coverage, customer value, competition and alternatives, clarity and control, and implementation complexity. These evaluation criteria can overlap.

### Analysis and output

Map each clause first, then assess completeness, fit between charge scope and meter, the relationship between rate, value and cost, clarity of application, and remaining unknowns.

Scale the deliverable to the request: a one-sentence conclusion; four-layer mapping and diagram; design rationale and alternatives; effects on customer understanding, usage behavior and budgeting; boundaries and unknowns. Do not force a full report for a narrow question. Use a four-layer Mermaid diagram and label vendor intent or effects as inference. See the [trilingual diagrams](references/framework.md).

## 日本語

### 目的と根拠

AI料金文書を、何を買うか、何を単位に計算するか、一単位いくらか、規則をどう適用するか、という四つの問いに整理する。現行の料金規則を理解するとき、または料金案を評価するときに使う。飛書は製品事例の参照であり、中国AI製品全体の共通ルールではない。

通常は利用者の言語で答える。三言語指定時は中国語・英語・日本語の事実、単価、適用条件を一致させる。平易な結論と全体図を先に示し、表と詳細を続ける。

提供された本文、契約、価格表、既存分析を読み、適用時期、単位、通貨、出典を記録する。本文、要約、自動プレビュー、契約は同じ強さの根拠ではない。矛盾を明示し、実際に適用される本文と契約を確認する。本文が提供済み、または閲覧不要と指定された場合は再閲覧しない。現行規則の確認を求められ、原文がなければ公式情報または許可されたログイン済みセッションを使う。

事実、推測、不明点を分ける。似た名称から同一の課金方式を推定せず、一つの製品事例から全社戦略を断定しない。意図的な不透明化、収益分配、将来の値上げなどを断言せず、考えられる仕組みと代替説明を示す。

### 四層の地図

| 層 | 問うこと | 飛書の製品事例で参照できる内容 | 分析の要点 |
|---|---|---|---|
| ① 課金対象 | 何のサービスを買うか | 利用権、タスク実行、実行環境と保存容量 | サービスを分け、何が含まれ、何が追加課金かを示す |
| ② 計量方法 | 何の単位で計算するか | パッケージ、席、回数、セル、分、実消費、起動日数 | 標準単位・実消費・組合せを区別し、成功条件、端数、重複除外、発火条件を確認する |
| ③ 単価 | 一単位いくらか | ポイント単価、モデル・ツール料金、通貨での購入価格 | ポイント単価と購入価格を分け、基本・追加・総額の関係を示す |
| ④ 適用 | 誰に、いつ、どの残高を適用するか | 権限、共有、有効期限、控除順序、特典、免除 | 対象と開始・終了条件を明示し、一部の規則を全体に広げない |

これは問いを分ける枠組みであり、料金設計の全要因を網羅する理論ではない。一費目・一条項を単位とし、一製品が四層すべてに関わってよい。含まれるサービスは①、計量単位は②、価格は③、資格と控除条件は④に置く。

### この方式を採る理由を考える

- 作業量が安定していれば、回数・件数・時間単価は理解と予算管理がしやすい。
- タスクごとの差が大きければ、モデル、ツール、文脈、計算資源の実消費が原価に合いやすい。
- 実行環境と保存容量には継続費用があり、時間や容量による課金に向く。
- 顧客価値の差には、席、機能パック、段階別パッケージが対応しやすい。
- 新機能には試用、付与ポイント、一時免除を使えるが、対象と終了条件を明示する。
- 権限、共有、控除順序、契約条件が、表示価格から実際の請求額を決める。

各理由を対応する層に戻し、計量、販促、適用条件を同列のMECE分類にしない。各層を、原価回収、顧客価値、競争と代替、理解と制御、実装複雑性の五つで評価する。評価軸は互いに関連してよい。

### 分析と成果物

各条項を四層に置いた後、構造が揃っているか、課金対象と計量単位が合うか、単価が価値と原価に見合うか、適用条件が明確か、何が未確認かを判断する。

依頼に応じて、一文の結論、四層対応と図、設計理由と代替説明、顧客の理解・利用行動・予算方法への影響、適用範囲、要確認事項を示す。部分質問に長い報告を強制しない。図は四層のMermaidとし、提供者の意図と影響は推測と明示する。[三言語の図](references/framework.md)を利用できる。
