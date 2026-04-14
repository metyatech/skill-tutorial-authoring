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

## Scientific foundations

All authoring rules below derive from the principles in this
table. Principles are stated so their scopes do NOT overlap;
when two seem to conflict, the "Scope & limits" column
resolves the boundary. The agent MUST apply them actively when
writing new tutorials and when reviewing existing ones.

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

- A Concept MUST be at most 5 sentences or 1 short table.
- A Concept MUST answer "what is it?" and "why does the learner
  need to know right now?".
- If a Concept needs more than 5 sentences, the author MUST split
  it into multiple Concepts.

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
