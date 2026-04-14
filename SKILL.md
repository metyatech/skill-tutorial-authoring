---
name: tutorial-authoring
description: >-
  Author, revise, reorganize, or review step-by-step tutorials (software,
  hardware, any tool) to minimize cognitive load and maximize first-attempt
  success rate. Use when writing a new guide, improving an existing one,
  auditing tutorial structure, or reorganizing course content. Apply multimedia
  learning theory and minimalism automatically. Triggers on: 'tutorial',
  'step-by-step guide', 'hands-on guide', 'walkthrough', 'how-to', 'reorganize
  tutorial', 'revise guide', 'improve tutorial quality', 'review tutorial
  structure', 'チュートリアル', '整理し直す', 'マルチメディア学習'.
---

# Tutorial authoring

Use this skill when writing, revising, or auditing any document
where a reader follows steps to build or achieve something.

## Target learner (expertise reversal boundary)

This skill is optimised for **beginner-to-intermediate**
learners encountering the subject for the first or second time.
Most multimedia learning principles (Signaling, Pre-training,
Personalization, heavy imagery) are strongest in that range and
weaken — or reverse — for experts (Kalyuga's *expertise
reversal effect*). If the artefact is an expert-facing quick
reference, the author MUST scale back Signaling, Concept
density, and hand-holding narrative, and lean on Reference
tables. When in doubt, state the target learner explicitly in
the document's opening.

## Scientific foundations

All authoring rules below derive from the principles in this
table. Principles are stated so their scopes do NOT overlap;
when two seem to conflict, the "Scope & limits" column
resolves the boundary. The agent MUST apply them actively when
writing new tutorials and when reviewing existing ones.

### Underlying load model (Sweller's CLT)

Every principle in the table below is a tactic for managing one
of the three load types in Cognitive Load Theory (Sweller, 1988).
When two principles compete, resolve by asking *which load type
currently dominates*.

| Load type | What it is | Which principles address it |
|---|---|---|
| **Intrinsic** — inherent difficulty of the material | Cannot be reduced, only sequenced | Segmenting, Pre-training |
| **Extraneous** — effort wasted on poor presentation | MUST be minimised | Coherence, Redundancy, Spatial/Temporal contiguity, Signaling, Modality |
| **Germane** — effort spent on schema construction | SHOULD be fostered | Multimedia, Personalization, Generative activity, Worked example, Feedback |

Expertise reversal (Kalyuga, 2007) predicts that tactics which
reduce extraneous load for novices can *increase* extraneous
load for experts (because redundant signals compete with
established schemas). This is why the skill scopes itself to
beginner-to-intermediate learners.

| Principle (source) | Core insight | Scope & limits | Authoring implication |
|---|---|---|---|
| **マルチメディアの原理** (Mayer, 2009) | 補完的情報を異なる表現（画像とテキスト）に分担すると学習が促進される | 「組み合わせ」は**補完**であって**重複**ではない。同一情報の二重提示は本原理では正当化されない(→ 冗長性原理) | 操作ステップでは、画像が WHERE（位置・順序・選択肢の外観）を、テキストが WHAT（動作の種類・画像に映らない値）を担う |
| **空間的接近の原理** (Mayer, 2009) | 対応する画像とテキストが空間的に近いほど効果的 | 1:1 対応のペアに限定。無関係な画像とテキストを並置する理由にはならない | 1 Action = 1 画像。画像は対応テキストの直前・隣接に配置する |
| **時間的近接の原理** (Mayer, 2009) | 対応する画像とテキスト（または音声）は同時に提示するほど効果的 | **音声または動画など時間軸を持つ媒体にのみ**適用。静的ページでは空間的接近原理で代替 | ナレーション付き動画では、画像切替とナレーションを同期させる |
| **一貫性の原理** (Mayer, 2009) | 教示目的と無関係な文書・画像・音は学習を阻害する | 「無関係」は学習目的から見た判定。面白さや装飾性は保持の根拠にならない | 装飾画像・余談・BGM・装飾的アニメーションは除去 |
| **モダリティの原理** (Mayer, 2009) | 視覚＋聴覚の分担は視覚独占より有効（視覚チャネル過負荷回避） | **音声モダリティを含む媒体（動画・音声教材）でのみ**適用。静的テキスト＋画像の媒体では無関係 | ナレーションと同一文章を画面に出さない |
| **冗長性の原理** (Mayer, 2009) | 意味的に同一の情報を複数フォーマットで重複提示すると学習を阻害する | 適用対象は**意味的に同一**の情報（同じ UI ラベル・同じ値・同じ説明）に限定。補完的情報の併置は該当しない(→ マルチメディア原理) | 画像に映っている UI ラベル・選択肢名・既定値をテキストで再掲しない |
| **セグメンティングの原理** (Mayer, 2009) | 学習者がペースを制御できる単位に分割するほど効果的 | セグメント単位は**1つの意味的に閉じたサブゴール**。単一画面・単一状態内の連続操作は原則 1 セグメント。画面遷移・状態遷移・モード切替が自然な境界 | 画面内の項目数で機械的にセグメントを割らない。画面遷移で区切る |
| **ミニマリズム** (Carroll, 1990) | 学習者はすぐ行動しながら学ぶ（doing で学ぶ） | 適用対象は**まだ不要な情報の除去**。必要情報の補完的分担(→ マルチメディア原理)を削ることは含意しない | 前置きの概念説明を最小化し、最初の Action を早める。Concept は first-use 直前に置く |
| **シグナリングの原理** (Mayer, 2009) | 重要箇所を視覚的手がかりで強調すると注意配分が改善し本質処理に集中できる | 合図は**学習目的に沿った要素**にのみ付ける。装飾目的の強調・感情表現の太字は一貫性原理違反 | Section の goal 宣言、画像の番号吹き出し、太字 UI 要素名、①②③ の順序番号で重要箇所を示す |
| **事前トレーニングの原理** (Mayer, 2009) | キー用語の名前と特徴を事前に提示すると主学習時の外在的処理が下がる | 予習は**これから出る概念のみ**に限定。遠い将来に出る概念や全体概論はミニマリズム違反 | Concept は first-use の直前に置き、「名前＋鍵となる特徴」を最小単位で提示する |
| **個人化の原理** (Mayer, 2009) | 会話的・二人称・能動的文体はフォーマル文体より学習効果が高い | 文体の**親しみやすさ**が本質。馴れ馴れしさ・絵文字濫用・感情過剰は一貫性原理違反になり得る | 学習者に直接語りかける二人称・能動形で書く（日本語：「〜しましょう」「確認してください」）。三人称で読者を描写しない（「受講者が〜する」「初学者向け」等を禁止） |
| **生成活動の原理** (Mayer, 2014) | 学習者に要約・予測・説明などの生成活動を求めると学習が深まる | 活動は**学習目的に関連**していること。単なる作業の追加は一貫性原理違反 | Verify で「何が起きるか」を観察判断させる。Checkpoint で behavior を自己確認させる。Exercise を周期的に織り込む |
| **熟達度反転効果** (Kalyuga, 2007) | 初心者に効く合図・概念予習・詳細説明は熟達者には逆効果になる | 本スキルは**初〜中級者向け**に最適化。熟達者向け資料では Signaling・Concept 密度・narrative を縮退させる | 対象者を冒頭で宣言し、原理の適用量を対象者に合わせる |
| **フィードバックの原理** (Shute, 2008) | 学習者が自分の行動の正誤・結果を確認できると schema 構築が促進される | フィードバックは**即時・具体・観察可能**であるべき。汎用的な「成功しました」表示は Coherence に接するため実体のある状態記述にする | Verify は Procedure の観察可能な結果、Recovery は失敗の原因と回復手順、Checkpoint は Step 末の自己確認、という三層のフィードバックを必ず配置する |
| **ワークトエグザンプル効果** (Sweller, 1985; Atkinson et al., 2000) | 完全な解法例を示してから自力演習に移す方が、最初から演習するより初心者には効果的 | 熟達が進むと逆転（Expertise Reversal）して演習先行が有効になる。本スキルは初〜中級向けなので**例→演習**の順を優先 | 新しい手順や概念では、まず完成例（画像＋完結した Action 列）を通しで見せてから、変化点を差し替える演習（Exercise）を置く |

### Out-of-scope principles (noted explicitly, not applied here)

The following Mayer principles require audio or speaker presence
and therefore do NOT apply to static text-and-image tutorials.
If the artefact is a narrated video or an avatar-driven
walkthrough, consult the primary sources — this skill does not
cover their application.

| Principle | Applies to | Why out of scope here |
|---|---|---|
| **Voice principle** (Mayer, 2009) | 音声ナレーション媒体 | 人間の声 vs 機械音声の比較。静的ページに音声はない |
| **Image principle** (Mayer, 2009) | 動画教材で話者の画像を画面に出すか | 話者の顔映像の有無は静的ページで判断不能 |
| **Embodiment principle** (Mayer, 2014) | 動画で話者がジェスチャーを伴うか | ジェスチャーは動画特有 |
| **Immersion principle** (Mayer, 2021) | VR / 没入型媒体 | 本スキルは 2D 静的ページに限定 |

Authors writing narrated video or VR content MUST NOT assume
this skill covers these principles; apply them separately from
Mayer's primary sources.

## Information hierarchy

Every tutorial MUST be composed of exactly these layers:

```
Tutorial (page)
 └── Step (milestone: "when done, you can X")
      ├── goal — 1 future-tense sentence declaring what the learner will achieve
      ├── Concept × N — term/background, always collapsible, before first use
      ├── Reference × N — lookup tables, always collapsible, near relevant procedure
      ├── Procedure × N — a group of actions toward one sub-goal
      │    ├── why — 1 sentence: why this procedure exists (optional)
      │    ├── Action × N — the atomic unit (image + instruction + result)
      │    └── Verify — "→ expected result" (1 line)
      ├── Recovery — error recovery, inline, after the action that can fail
      └── Checkpoint — end-of-step checklist (exactly one per Step)
```

## Five information types and display rules

| Type | Content | Display | Placement |
|---|---|---|---|
| **Action** | Image + instruction + result | Always visible. Image above text, 1:1 mapping | Inside Procedure |
| **Verify** | Success confirmation | Always visible, `→` prefix, 1 line | End of Procedure |
| **Concept** | Term definition, background | Collapsible (`<details>`) | Before procedure that first uses it |
| **Reference** | Key tables, panel lists | Collapsible (`<details>`) | Near procedure that needs it |
| **Recovery** | Error recovery steps | Always visible, short | After action that can fail |

## Image / text / video hierarchy

| Subject | Primary | Secondary | Rationale |
|---|---|---|---|
| UI operation (where to click) | Annotated screenshot | Label text only | Unknown UI requires visual anchor |
| Result (what happened) | Text (`→` 1 line) | Screenshot (optional) | State changes are faster to judge via text |
| Concept (why) | Text only | — | Abstraction does not benefit from images |
| Multi-step continuous flow | Video/GIF | Text (supplement) | Motion cannot be conveyed in stills |

## Atomic unit: Action

The smallest learning unit is:

```
[Image: WHERE to interact] → [Text: WHAT to do] → [Text: WHAT happens (optional)]
```

Rules:

- The author MUST use one image per action. The author MUST NOT
  batch images. *(mechanised: `tutorial/action-single-image`)*
- The image MUST be placed above or before the text (spatial
  contiguity).
- The author MUST NOT describe in text what the image already
  shows (redundancy elimination).
- The image and the text MUST cover non-overlapping channels:
  the image carries **WHERE** (position, visual anchor, step
  ordering via numbered callouts); the text carries the
  imperative **WHAT** plus any values the image cannot convey.
- The author MUST keep in the text: values the learner types by
  hand (e.g. `UE90min`, `CLEAR!`), user-specific paths the
  screenshot cannot generalise, and UI element names that are
  not labelled in the shot.
- The author MUST remove from the text: positional prefixes when
  the image already shows position *(mechanised:
  `tutorial/action-positional-prefix`)*; label/value pairs
  already paired in the image's numbered callouts; micro-
  interaction details already conveyed by the image's arrows or
  step markers.
- Reducing Action text to a bare verb such as "クリックします"
  MUST NOT be used as a redundancy fix. The imperative WHAT
  plus the values the image cannot convey is the minimum;
  strip only what the image already carries.
- If the action produces a visible result, the author MUST state
  it inline. The author MUST NOT create a separate Verify for
  this — Verify is reserved for Procedure-level confirmation only.

## Signaling (visual cueing)

学習者の注意を本質的な情報に誘導するために、情報階層を**視覚的な
合図**で表現する。合図は学習目的に沿った要素にのみ付ける。

Signaling surfaces in this skill:

| Surface | Cue | Purpose |
|---|---|---|
| Section heading | `goal` banner (future-declarative) | Step の到達点を宣言 |
| Action image | Numbered callout (①②③) + arrow | Position / Sequence を強調 |
| Action text | Bold for unlabelled UI element names, typed values, key gestures | Identity / Typed value の強調 |
| Procedure | `why` one-liner | Procedure の目的を宣言 |
| Verify / Recovery | Component framing (→, title) | 状態判定と回復手段の境界を明示 |

Rules:

- 合図は**必ず学習目的に沿う**こと。装飾目的の太字、感情表現の
  強調、文末の飾り記号は Signaling ではなく一貫性原理違反。
- 画像の番号吹き出しとテキストの ① 番号は**併記する**（Sequence
  channel の二重化は Redundancy に該当しない補完関係）。
- 太字の濫用（1 文に 3 箇所以上など）は合図の効力を破壊するため
  禁止。強調は本当に注視すべき要素のみに絞る。

## Personalization (reader-addressing voice)

学習者に**直接語りかける**二人称・能動・会話的な文体で書く。

Rules:

- Use second-person direct address to the reader. Do not
  describe the reader in third person ("受講者が〜する",
  "初学者が〜", "学習者は〜").
- Use active, conversational Japanese: 「〜しましょう」
  「〜してください」「ここで〜を確認します」.
- Do not open a page by describing what the document *is* or
  *who it is for* ("この教材は〜のための資料です" は NG).
  Open with the first learner-facing step or an inviting
  goal statement.
- Personalization is about **friendliness, not familiarity**.
  Emoji spam, 余談, 感情過剰な装飾はむしろ Coherence 原理違反
  になるため避ける。親しみやすさの上限は「先輩が隣で教えて
  くれる」程度が目安。
- Goal strings already use future-declarative form; they also
  implicitly address the reader — do not revert them to
  third-person ("受講者が〜する状態になります" は Goal と
  Personalization の両方に違反する).

## Generative activity (prediction / retrieval)

学習者が**受動的に読むだけ**にならないよう、生成活動（予測・
説明・自己確認）を組み込む。活動は必ず学習目的に関連させる。

Surfaces:

| Surface | Generative role |
|---|---|
| Verify | 直前の Procedure の結果を**観察判断**させる（受動受領でなく能動観察） |
| Checkpoint | Step 末で behavior を**自己確認**させる retrieval 活動 |
| Exercise (course-docs-platform の `<Exercise>`) | 学習単位の周期的な応用課題 |
| Recovery | 失敗時の**原因推論**を補助する（一行で原因→回復） |

Rules:

- Verify の文面は「**観察可能な状態**」で書く（例: 「キューブが
  消えれば成功」）。内部処理・実行履歴の記述（例: 「Destroy
  Actor が実行されました」）は生成活動を奪う。
- Checkpoint の項目は学習者自身が視覚・操作で確かめられる内容に
  限定。内部状態や jargon は不可。
- Exercise は**学習目的に関連**していること。作業量稼ぎの演習、
  本筋と関係ない応用は一貫性原理違反。
- 予測を促すプロンプト（「実行前に、何が起こるか予想してみて
  ください」）は有効だが、過剰使用は認知負荷を上げる。Step ごとに
  1 回が目安。

## Writing rules

### Goal text

- The `goal` string is rendered verbatim as a banner directly below
  the section heading; no prefix such as "ゴール:" is added. It MUST
  read as a complete sentence on its own. Bare noun-phrase endings
  such as 「〜した状態」 are forbidden because they render as
  incomplete prose.
- The author MUST write goals in future-declarative form describing
  what the learner will achieve by the time the section is complete:
  - Action completion → 「〜します」（例: 「キューブを 1 つ置きます」）
  - Acquired capability → 「〜できるようになります」（例:
    「キャラクターを操作できるようになります」）
  - Acquired behavior / state → 「〜ようになります」 /
    「〜の状態になります」（例: 「触れたら消えるようになります」）
- The author MUST NOT write goals in past or completed form
  (「〜した」「〜された」「〜した状態」「〜している」「〜できます」) because
  those frame the section as a retrospective of what already happened
  instead of a preview of what the learner is about to build.
  *(mechanised: `tutorial/section-goal-required`, `tutorial/section-goal-tense`)*

### Action text

- The author MUST use the imperative mood: 「〜をクリックします」
  「〜と入力します」.
- The author MUST name a UI element in bold **only when** the
  image does not clearly label it with a visible caption or a
  numbered callout, or cannot disambiguate it from similar
  elements. Repeating an image-labelled element in text violates
  the Redundancy principle; Identity is image-primary when
  labelled in the shot (see the WHERE/WHAT channel rules in
  Atomic unit: Action).
- Panel and location names appear inline on first use **only
  when** the shot does not already make the panel unambiguous.
  A full-screen screenshot that shows the panel in context does
  not require redundant naming in text.
- Regardless of the above, values the learner must type
  (e.g. `UE90min`), user-specific paths, and gestures/motions
  (drag direction, hover vs click) MUST remain in text because
  a still image cannot convey them.

### Concept text

Concept serves the **Pre-training** principle: it teaches the
*name* and the *key features* of a term the learner is about
to encounter, so that main-task cognitive load is reduced.

- A Concept MUST be at most 5 sentences or 1 short table.
- A Concept MUST answer "what is it?" (name + key features)
  and "why does the learner need to know right now?".
- A Concept MUST be placed immediately before the first
  Procedure that uses the term. Placing Concepts far upfront
  violates Minimalism; omitting them until after first use
  violates Pre-training.
- Concepts for terms that appear much later MUST NOT be written
  now. Pre-training applies to the *next* sub-task, not to the
  entire page.
- If a Concept needs more than 5 sentences, the author MUST split
  it into multiple Concepts and place each before its own
  first-use Procedure.

### Verify text

- In component-based tutorials the Verify component renders its
  own leading `→`; the author MUST NOT include `→` in the source
  or the rendered output will have a doubled arrow.
  *(mechanised: `tutorial/verify-no-duplicate-arrow`)*
- In plain-Markdown tutorials (no component), the Verify line
  MUST start with `→`.
- A Verify line MUST describe observable state, not internal
  mechanics:
  - ✅ 「キューブが消えれば成功です」
  - ❌ 「Destroy Actor が実行されました」

### Checkpoint

- A Checkpoint MUST be a bullet list of observable behaviors.
- A Checkpoint MUST NOT include internal state or jargon.
- Exactly one Checkpoint per Step, placed as the last element
  of the Step. *(mechanised: `tutorial/checkpoint-placement`)*

## Anti-patterns (do NOT do)

Judgement-based anti-patterns; a tool cannot reliably detect
these, so the author is responsible for catching them.

| Anti-pattern | Violated principle | Fix |
|---|---|---|
| Text restating what image shows | Redundancy | Remove the text or remove the image |
| Button/selection label repeated in bold text while the image already labels it with a numbered callout | Redundancy | Keep text to "① を選びます" etc.; Identity is carried by the image |
| Mechanical splitting of a single-screen unified task into many Actions (one per item in the same dialog) | Segmenting (misapplied) | Keep 1 screen = 1 Action when the sub-goal is unified; split only on screen/state transitions |
| Decorative images, fun sidebars, background music | Coherence | Remove entirely; they impair learning |
| Same content in narration AND on-screen text | Redundancy / Modality | Use narration OR on-screen text, not both |
| `:::note` for concepts | Segmenting | Not collapsible; use Concept component |
| Verify after every action | Segmenting | Verify at Procedure end only |
| Front-loading reference tables | Minimalism | Use Reference, near first use |
| Term introduced before it's needed | Minimalism | Concept before first-use Procedure |
| Reducing Action text to a bare "クリックします" to avoid redundancy | Redundancy (over-correction) | Keep the imperative WHAT plus the values the image cannot convey |
| Settings table duplicating the image's numbered callouts row-for-row | Redundancy | Keep in text only the values the image cannot convey (typed input, user-specific paths, dropdown values absent from the shot) |
| Micro-interaction detail ("空白で離す", "カーソルを乗せ") redundantly described when image's arrows already convey it | Redundancy | Remove — but only after confirming the image truly conveys the gesture; motion attributes ("drop in **empty** space", "hover vs click") often need text because a still image cannot encode them |
| Opening a page by describing what the document *is* or *who it is for* ("この教材は〜のための資料です", "受講者が〜する授業") | Personalization | Rewrite in second-person direct address; open with the first learner-facing action or an inviting goal |
| Describing the reader in third person ("学習者は〜", "初学者向け", "受講者が〜") anywhere in the tutorial body | Personalization | Use second-person active voice ("〜しましょう", "確認してください") |
| Front-loading a long concept chapter before the first Action (Pre-training misapplied) | Pre-training × Minimalism | Move each term's Concept to immediately before its first-use Procedure; keep each Concept to name + key features only |
| Bold/highlight used for emotional emphasis or decoration, not tied to a learning-objective cue | Signaling × Coherence | Reserve bold/highlight for the element the learner must find or type; remove decorative emphasis |
| Multiple bold spans crammed in one sentence | Signaling (dilution) | Bold only the single element that most matters; demote the rest to plain text |
| Verify line that describes internal mechanics instead of observable state ("Destroy Actor が実行されました") | Generative activity | Rewrite as an observable outcome the learner can check ("キューブが消えれば成功") |
| Exercises tacked on for practice volume rather than learning objective | Coherence / Generative activity (misapplied) | Tie every Exercise to the Step's stated goal; drop unrelated drills |
| Applying beginner-weight Signaling/Concept density to an expert-facing reference | Expertise reversal | Scale back: use compact Reference tables, drop hand-holding narrative |

## Mechanised checks (enforced at MDX build/dev time)

The following conventions are enforced by the
`remarkTutorialLint` plugin in
`@metyatech/course-docs-platform`. Violations surface in
`npm run dev` and `npm run build` output; author reliance on
memory is not required.

| Rule ID | Severity | Intent |
|---|---|---|
| `tutorial/section-goal-required` | error | Every `<Section>` declares its `goal` |
| `tutorial/section-goal-tense` | error | Goal uses future-declarative form |
| `tutorial/action-single-image` | error | One image per Action |
| `tutorial/section-no-hrule` | error | No `---` inside a Section |
| `tutorial/checkpoint-placement` | error | Exactly one `<Checkpoint>` per Step, placed last |
| `tutorial/reference-image-only` | warn | `<Reference>` whose only content is an image — success-verifying screenshots belong in a visible `<Action>` |
| `tutorial/verify-no-duplicate-arrow` | warn | `<Verify>` body starts with `→` — component already renders it |
| `tutorial/action-positional-prefix` | warn | `img`-bearing `<Action>` body starts with a positional prefix — either remove or add a callout to the image |

## Component system (course-docs-platform)

When writing for `@metyatech/course-docs-platform`-based sites,
the author MUST use the provided MDX components. They are
globally available (no import needed):

```mdx
<Step goal="アイテムに触れると消えてスコアが増えるようになります">

  <Concept title="コリジョンとは">
    当たり判定のこと。ブロック＝壁、オーバーラップ＝すり抜け＋検知。
  </Concept>

  <Procedure why="触れたことを検知できるようにする">
    <Action img="./img/overlap-events-on.png">
      **Generate Overlap Events** をオンにする
    </Action>
    <Action img="./img/overlap-all-dynamic.png">
      **コリジョンプリセット**を **OverlapAllDynamic** に変更する
    </Action>
    <Verify>アイテムをすり抜けて通れる</Verify>
  </Procedure>

  <Checkpoint>
    - アイテムに触れるとスコアが増える
    - アイテムに触れると消える
  </Checkpoint>

</Step>
```

### Components

| Component | Props | Purpose |
|---|---|---|
| `<Step>` | `goal` (string) | Milestone wrapper |
| `<Procedure>` | `why` (string, optional) | Groups actions into a logical task |
| `<Action>` | `img` (string, optional), `alt` (string, optional) | Atomic operation with image |
| `<Verify>` | children | Procedure success confirmation |
| `<Concept>` | `title` (string) | Collapsible background/term |
| `<Reference>` | `title` (string) | Collapsible lookup table |
| `<Checkpoint>` | children | End-of-step checklist |

## Non-component tutorials

When components are not available (plain Markdown, Docusaurus,
etc.), the author MUST apply the same information hierarchy
using native syntax:

| Component equivalent | Plain Markdown |
|---|---|
| `<Step goal="...">` | `## Step N：タイトル` + first line = goal sentence |
| `<Concept>` | `<details><summary>💡 Title</summary>...</details>` |
| `<Reference>` | `<details><summary>📖 Title</summary>...</details>` |
| `<Procedure>` | `### N-M. Title` |
| `<Action>` | `![alt](img)` on its own line, then numbered list item |
| `<Verify>` | `**→ expected result**` |
| `<Checkpoint>` | `:::tip[確認ポイント]` or equivalent admonition |

The hierarchy and writing rules MUST remain identical regardless
of tooling.

## Limits of principled authoring

This skill encodes the best available tactics, but it does not
guarantee pedagogically correct output. Authors and reviewers
MUST treat the following as known limitations.

### Semantic checks that tooling cannot enforce

The `remarkTutorialLint` plugin catches structural violations
only. The following judgements are **author-only**; treat them
as explicit review gates, not as automated safety nets.

| Judgement | Why machine-unreachable |
|---|---|
| "Is this bold/highlight serving a learning objective, or decorative?" (Signaling × Coherence) | Requires knowing what is objective-relevant at this step |
| "Is this image decorative or essential?" (Coherence) | Same |
| "Is this prose second-person direct address, or third-person description?" (Personalization) | Japanese grammar allows zero-subject sentences; pattern matching over-triggers |
| "Does this Exercise serve the stated Step goal?" (Generative activity × Coherence) | Requires semantic alignment with the Step's goal string |
| "Is this Concept's 'why does the learner need to know now?' actually satisfied?" (Pre-training) | Intent-level check |
| "Is Signaling density appropriate for the target learner?" (Expertise reversal) | Requires modelling the reader's prior knowledge |

### Generalisation limits of the underlying research

- Mayer's effect sizes were measured primarily on **educational
  videos and science lessons** with short durations. Applying
  them to long-form software tutorials requires extrapolation;
  the *direction* of each effect is robust, but magnitude is not
  guaranteed.
- Most studies use novice learners in controlled settings.
  Real-world learners mix expertise levels, read non-linearly,
  and bring prior frustration. The skill's rules are the
  *baseline*, not a replacement for observing real learners.
- Language and cultural effects on Personalization / Voice have
  been studied mainly in English. Japanese-specific tactics
  (「〜しましょう」 vs 「〜します」 の丁寧度階調, etc.) are
  transferred by analogy, not by direct evidence.

### When principles appear to conflict

1. Identify which load type (Intrinsic / Extraneous / Germane)
   is currently dominant for the target learner at this step.
2. Apply the principle that directly addresses that load type.
3. If still ambiguous, ask *which tactic would a novice
   benefit more from right now?* — the skill is novice-biased.
4. If the conflict involves an out-of-scope principle (Voice,
   Image, Embodiment, Immersion), treat it as not resolved by
   this skill and consult the primary sources.

### Self-review

Use `REVIEW-CHECKLIST.md` (same repository) as a reviewer-facing
checklist. It mirrors the principle table and is the single
place to audit a draft tutorial against every principle in
sequence.
