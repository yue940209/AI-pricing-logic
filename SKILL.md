---
name: ai-pricing-logic
description: 分析国产 AI 产品的计费设计与版本变化，参照飞书，按收什么、怎么算、定多贵、怎么实施四层定位规则，解释保留或调整的可能原因并评估企业成本。Analyze Chinese AI pricing and billing changes using Feishu as a reference. 中国AI製品の料金設計と変更を分析する。用于定价分析、计费规则对比和企业成本优化，不用于自动采购或改套餐。
---

# 国产 AI 产品计费逻辑（参照飞书）

## 简体中文

### 目的与使用

把计费文档放进同一张定价地图，说明规则改在哪里、可能为什么改、影响谁、企业如何应对。适用于分析既有规则、比较版本、评估自己的收费方案。飞书只是参考案例，不是全部国产 AI 产品的统一规律。

默认使用用户语言；用户要三语时输出中文、英文、日文，保持事实、日期、费率、限定条件一致。写得通俗：先结论和地图，再表格和细节；术语首次出现解释，不堆抽象词。

### 先确定证据

读取用户提供的文档、粘贴正文及既有分析，记录版本、生效日期、单位、币种和来源。全文、摘要、网页自动速览、合同不是同等级证据；正文与速览冲突时指出，以适用正文和合同核对。用户已给正文或要求不访问网页时，不重复浏览；如果要求核实当前规则且缺原文，查官方来源或经授权的已登录会话。缺上一版就给当前规则映射，明确不能证明新增、取消或涨价。

不把“旧摘要没提到”当作“本次新增”；不把更名当作商业模式已彻底改变；不假设旧套餐无限使用。将规则事实、分析推断、待核实信息分开。解释厂商目的时给可能机制和替代解释，不断言诱饵、收割、刻意不透明、生态分成或未来涨价。

### 四层地图

| 层 | 问什么 | 飞书参考落点 | 分析动作 |
|---|---|---|---|
| ① 收什么 | 客户为哪项服务付钱？ | 使用资格；任务执行；持续运行与存储 | 拆分每笔收费，核对套餐已含内容，避免预算重复计算 |
| ② 怎么算 | 什么单位决定账单？ | 套餐、席位、次数、单元格、分钟、实际资源、开机天数 | 区分标准单位、实际资源和混合方式；明确成功、取整、去重和触发条件 |
| ③ 定多贵 | 每单位费率是多少？ | 每次点数、模型与工具费率、套餐人民币价格 | 分开点数费率与实际采购价；基础费不等于总费，历史标价不等于当前加购价 |
| ④ 怎么实施 | 谁能用、何时生效、如何抵扣和过渡？ | 权限适用、共享范围、额度有效期、扣减顺序、赠点、暂免、老客安排 | 列适用对象、日期、结束条件；局部豁免不扩展到所有功能 |

这是按问题分层的分析工具，不宣称穷尽所有定价因素。一个产品同时涉及四层很正常；以一笔费用或一条规则为分析单位。套餐含什么归①、套餐价归③、额度适用与抵扣归④；“按席位”归②、席位价格归③、资格内容归①。

### 判断为什么改或没改

- 工作量稳定：按次、按条、按分钟可能足够；保留简单单价能降低解释与核账负担。
- 一次操作内部差异很大：模型、工具、长上下文和多步执行会令按次费用偏离成本，可能需要实际资源计价。
- 持续占用资源：运行、开机和存储有独立成本，不必随对话方式同步调整。
- 体验与价值尚不确定：试用、赠送或自主任务暂免可能降低尝试阻力；暂免不是长期承诺。
- 已有合同与预算：切换涉及沟通、计量和合同成本，过渡安排可能比立即统一更合适。
- 没改还可能是暂未调整、竞争约束、合同限制或证据不足，不等于已经最优。

把前三项分别放回①②，后两项放回④；不要把它们当成同层 MECE 分类。对每一层另外检查成本覆盖、客户价值、竞争替代、理解与控制难度，以及调整收益能否覆盖实施和切换成本。这些评估维度有关联，不宣称互斥。

### 版本比较与输出

逐条用“旧规则｜新规则｜改变层次｜证据与状态｜可能逻辑｜受影响对象与动作”表。层次可多选：收费范围扩大、计量单位／口径改变、同单位费率改变、实施条件改变。不要统称涨价；账单增加也可能来自使用增加或优惠到期。必要时做同一业务量下的新旧情景比较，列假设、已含额度和失败重试，避免重复计算套餐与已含用量。

输出顺序按任务规模调整：一句话结论；四层映射与逻辑图；变化表；保留／调整原因及证据边界；企业与项目影响；优先省钱动作；待核实事项。用户只问局部时不强制完整长报告。图用 Mermaid，节点按四层组织；目的与影响标为推断。可复用 [三语框架图](references/framework.md)。只有需要飞书例子或理解常见误读时读取 [日期化案例](references/feishu-case.md)。

### 企业成本与项目动作

区分权限／套餐、搭建、上线资源、日常 AI 执行支出；这是预算视角，不意味着四项必须分开采购。固定查询、金额计算、审批与日期提醒优先普通程序、数据库、接口或本地脚本；运行位置不决定是否扣 AI 费，是否再次调用模型才是关键。理解合同、模糊语义和复杂分析再考虑 AI；不牺牲质量、权限或人工控制。

按新增／变更记录触发、复用结果、先抽样再批量、限制重试；高频固定任务先比较专用节点与 Agent 的效果和总成本。复杂任务限定数据范围、输出与完成条件，减少无关上下文和多余调用。管理闲置实例并核对停费生效时间。自定义模型比较外部账单＋平台／工具费＋维护成本，不称免费。

按成功完成一笔业务的总成本管理，计入失败、重试、人工复核；跟踪场景消耗、成功数量、单位成本、重复失败闲置成本。保留成本匹配与平台依赖两种视角；不要以联网回答替代必须依靠企业知识的任务。分析不自动授权购买、调套餐、停生产或公开内部材料。

## English

### Purpose and evidence

Analyze Chinese AI billing, compare versions, or evaluate a proposed pricing design using Feishu as a reference—not a universal rule. Respond in the user's language; when three languages are requested, keep Chinese, English and Japanese facts, dates, rates and qualifications aligned. Lead with a plain conclusion and map, then tables and detail.

Read supplied rules and prior analysis. Record version, effective date, units, currency and provenance. Full rules, summaries, automatic previews and contracts carry different evidential weight; flag conflicts and verify the applicable text and contract. Do not browse again when text is supplied or browsing is declined. If current verification is requested and text is missing, use official sources or an authorized signed-in session. Without a complete earlier version, map the present rules and state which changes cannot be established.

Absence from an old summary does not prove a new charge. Renaming does not prove a complete business-model shift or previously unlimited use. Separate facts, inferred purposes and unknowns; offer alternative explanations rather than asserting bait, deliberate opacity, harvesting, revenue sharing or future price increases.

### Four-layer map

| Layer | Question | Feishu reference | Analysis |
|---|---|---|---|
| 1. Charge scope | What service is purchased? | Entitlements, task execution, reserved runtime and storage | Decompose charges and included benefits to avoid double counting |
| 2. Meter | What unit drives billing? | Packages, seats, events, cells, minutes, actual resources, powered-on days | Identify standard units, actual usage or hybrids; capture success, rounding, deduplication and triggers |
| 3. Rate | What does each unit cost? | Credits per event, model/tool rates, package currency price | Separate credit rates from purchase price, base from total, historical list from current incremental cost |
| 4. Application and transition | Who is eligible, when does it apply, how are balances used? | Sharing, expiry, deduction order, promotions, exemptions, legacy treatment | Identify eligible parties, dates and end conditions; do not generalize a local exemption |

This is a question hierarchy, not an exhaustive universal theory. Analyze each charge or clause; one product can involve all four layers. Package contents belong in 1, price in 3, balance eligibility and deduction in 4. Per-seat metering belongs in 2, seat rate in 3, entitlement in 1.

### Explain changes and retention

Stable workloads may retain simple event or time rates. Highly variable multi-step tasks may require actual model, tool and compute metering. Reserved resources have continuing costs independent of dialogue. Trials, credits and temporary autonomous-task exemptions may reduce adoption friction; they are not permanent promises. Contracts, budgets and migration costs can justify staged transitions. Unchanged rules may also reflect deferred changes, competition, contracts or missing evidence—not optimality.

Place mechanisms under their relevant layers rather than mixing meters, promotions and migration as peer MECE categories. Evaluate each layer against cost coverage, customer value, alternatives and competition, comprehensibility and control, and implementation/migration cost. These evaluation criteria interact and are not claimed to be mutually exclusive.

### Comparison, delivery and enterprise action

Use a clause-level table: previous rule | new rule | layer(s) changed | evidence/status | possible rationale | affected users/action. Distinguish expanded scope, changed metering, changed comparable unit rates and changed application conditions. Higher bills may instead reflect more use or expiring offers. Where useful, compare the same business volume with explicit assumptions, included allowances and failures/retries, without counting prepaid usage twice.

Scale the deliverable: conclusion; map and diagram; changes; plausible reasons and limits; enterprise/project impact; prioritized savings; unknowns. Do not force a full report for a narrow question. Use a four-layer Mermaid diagram and label inferred effects. See [trilingual diagrams](references/framework.md); read [dated Feishu examples](references/feishu-case.md) only when relevant.

Distinguish entitlements/packages, development, hosted resources and ongoing AI tasks without assuming separate purchases. Use deterministic code, databases, APIs or local scripts for fixed searches, calculations, routing and date reminders. Location does not determine AI charges; invoking a model does. Reserve AI for interpretation and judgment with appropriate quality, permissions and human controls.

Process only new/changed records, reuse results, sample before bulk runs and cap retries. Compare specialized nodes with Agents by quality and total cost. Bound task inputs, outputs, context and completion. Manage idle instances and stop-billing dates. Compare custom models using external model bills plus platform/tool fees and maintenance. Track cost per successful business outcome including retries and review, scenario spend, successful volume and waste. Do not replace enterprise knowledge with web answers merely to save credits. Analysis does not authorize purchases, plan changes, production shutdowns or disclosure of internal material.

## 日本語

### 目的と根拠

飛書を参考に、中国の AI 製品の料金設計、版の違い、自社の料金案を分析する。飛書の事例を全製品の共通ルールとみなさない。通常は利用者の言語で答え、三言語指定時は中国語・英語・日本語の事実、日付、単価、適用条件を一致させる。平易な結論と全体図を先に示し、表と詳細を続ける。

提供された本文と過去の分析を読み、版、発効日、単位、通貨、出典を記録する。本文、要約、自動プレビュー、契約は同じ証拠ではない。矛盾を明示し、適用本文と契約を確認する。本文が提供済み、または閲覧不要と指定された場合は再閲覧しない。現行ルールの確認を求められ、本文がなければ公式情報または許可されたログイン済みセッションを使う。旧版が不完全なら現行ルールを整理し、立証できない変更を明記する。

旧要約にないだけで新規課金としない。名称変更から全面的な事業モデル変更や従来の無制限利用を推定しない。事実、目的の推測、不明点を分け、意図的な不透明化、囲い込み後の搾取、収益分配、将来の値上げなどを断定しない。

### 四層の地図

| 層 | 問うこと | 飛書の例 | 分析の要点 |
|---|---|---|---|
| ① 課金対象 | 何のサービスを買うか | 利用権、タスク実行、実行環境と保存容量 | 費目と含まれる特典を分け、二重計上を避ける |
| ② 計量方法 | 何の単位で計算するか | パッケージ、席、回数、セル、分、実消費、起動日数 | 標準単位・実消費・組合せを区別し、成功条件、端数、重複除外、発火条件を確認 |
| ③ 単価 | 一単位いくらか | ポイント単価、モデル・ツール料金、通貨での購入価格 | 基本料金と総額、過去の定価と現行の追加購入費を区別 |
| ④ 適用と移行 | 誰に、いつ、どの残高を適用するか | 共有、有効期限、控除順序、特典、免除、既存顧客対応 | 対象、日付、終了条件を明示し、一部免除を全体に広げない |

これは問いを分ける枠組みであり、定価設計の全要因を網羅する理論ではない。一費目・一条項を単位とし、一製品が四層すべてに関わることは問題ない。パッケージの内容は①、価格は③、残高の適用と控除は④。席ごとの計量は②、席単価は③、権限の内容は①に置く。

### 変更・据置きの考え方

作業量が安定していれば回数・時間単価の維持が合理的な場合がある。複数ステップで消費差が大きければモデル、ツール、計算資源の実消費が必要になり得る。継続確保する資源には会話と別の費用がある。試用、付与ポイント、自律タスクの一時免除は導入の抵抗を下げ得るが、永久無料ではない。既存契約、予算、切替負担は段階移行の理由となる。据置きには未着手、競争、契約制約、証拠不足もあり、最適との証明にはならない。

各項目を対応する層に戻し、計量・販促・移行を同列の MECE 分類にしない。各層を、原価回収、顧客価値、競合と代替、理解・制御のしやすさ、実装・移行負担で評価する。これらの評価軸には関連があり、相互排他的とは主張しない。

### 比較・成果物・企業の対応

旧規則｜新規則｜変更層｜根拠と確度｜考えられる理由｜影響と対応、の条項別表を作る。課金対象の追加、計量変更、同一単位の値上げ、適用条件の変更を区別する。利用増や特典終了でも請求は増える。同じ業務量で比較する場合は前提、内包枠、失敗と再試行を明示し、前払い分を二重計上しない。

依頼に応じて、結論、四層対応と図、変更点、理由の仮説と限界、企業・案件への影響、節約策、要確認事項を示す。部分質問に長い報告を強制しない。図は四層の Mermaid とし、推測の効果を明示する。[三言語の図](references/framework.md)を利用できる。[日付付き飛書事例](references/feishu-case.md)は必要時だけ読む。

権限・パッケージ、開発、稼働資源、日常 AI 実行を区別するが、別々の購入が必要とは限らない。固定検索、計算、承認振分け、期日通知は通常のコード、DB、API、ローカルスクリプトで処理する。場所ではなくモデルを呼ぶかが AI 費用を左右する。解釈と判断に AI を用い、品質、権限、人の確認を維持する。

追加・変更データのみ処理し、結果再利用、少量検証、再試行上限を設ける。専用ノードと Agent は品質と総費用で比較する。入力範囲、出力、文脈、完了条件を限定し、遊休環境と課金停止日を管理する。独自モデルは外部モデル費＋プラットフォーム・ツール費＋保守費で比較する。再試行と人の確認を含む業務成功一件当たりの費用、用途別消費、成功件数、無駄を追う。節約だけを理由に社内知識をウェブ回答で代替しない。分析は購入、プラン変更、本番停止、社内情報公開の許可を意味しない。
