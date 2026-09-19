---
name: tutorial-authoring
description: >-
  Author, revise, reorganize, or review step-by-step tutorials for
  beginner-to-intermediate learners, primarily static text-and-image format.
  Grounded in Mayer's CTML, Sweller's CLT, and van der Meij & Carroll's
  minimalism. Use when writing a new guide, improving an existing one,
  auditing tutorial structure, or reorganizing course content. Triggers
  on: 'tutorial', 'step-by-step guide', 'hands-on guide', 'walkthrough',
  'how-to', 'reorganize tutorial', 'revise guide', 'improve tutorial
  quality', 'review tutorial structure', 'チュートリアル', '整理し直す',
  'マルチメディア学習'.
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
tables. When in doubt, state the target learner explicitly in the
authoring context or metadata. Do not leak author-facing audience
labels such as "初心者向け" into learner-facing prose unless the
reader genuinely needs that information.

## Scientific foundations

All authoring rules below derive from the principles in this
table. Principles are stated so their scopes do NOT overlap;
when two seem to conflict, the "Scope & limits" column
resolves the boundary. The agent MUST apply them actively when
writing new tutorials and when reviewing existing ones.

### Underlying load model (current CLT formulation)

Use the current formulation of Cognitive Load Theory described by
Sweller, van Merriënboer & Paas (2019), not the older three-additive-
load shorthand. **Intrinsic** and **extraneous** cognitive load are
the two basic categories. What older literature called *germane
cognitive load* is better treated as the working-memory resources
devoted to learning-relevant intrinsic aspects of the task rather
than as a third load that independently adds to total load.

| Category | What it means | Authoring response |
|---|---|---|
| **Intrinsic load** | Element interactivity created by the material *and the learner's current expertise* | Sequence and segment the material; provide pre-training, activation, worked examples, and fading appropriate to prior knowledge |
| **Extraneous load** | Element interactivity created by avoidable presentation or instructional procedure | Minimise split attention, irrelevant detail, unnecessary duplication, navigation cost, and other presentation overhead |
| **Germane processing / resource allocation** | Working-memory resources successfully redirected from extraneous activity toward learning-relevant intrinsic processing | Create room for useful retrieval, self-explanation, practice, and feedback after avoidable extraneous load has been controlled |

When principles compete, first remove avoidable extraneous load,
then manage intrinsic complexity for the learner's expertise, and
only then add learning-relevant activity that still fits within
available working-memory capacity. Germane processing is therefore
not a licence to add arbitrary difficulty.

Expertise reversal (Kalyuga, 2007) predicts that tactics which
reduce extraneous load for novices can *increase* extraneous load
for experts because redundant signals compete with established
schemas. This is why the skill scopes itself to beginner-to-
intermediate learners.

| Principle (source) | Core insight | Scope & limits | Authoring implication |
|---|---|---|---|
| **マルチメディアの原理** (Mayer, 2009) | 学習に必要な情報を、その内容に適した複数の表現へ補完的に分担すると学習が促進される | 画像を常に必須化する原理ではない。コード操作では CodePreview、短い非空間操作では text、空間・位置関係では visual が primary になり得る。同じ完全な手順を複数表現へ重複させない | 各 Action で **Primary Representation**（visual / code / text / diagram）を選び、他の表現は primary が伝えにくい情報だけを補う |
| **空間的接近の原理** (Mayer, 2009) | 対応する表現同士が空間的に近いほど統合コストが下がる | 対応関係がある場合に適用する。画像が不要なActionへ画像を追加する理由にはならない | visual と補足text、CodePreview と説明など、対応する表現を直前・隣接に配置する |
| **時間的近接の原理** (Mayer, 2009) | 対応する画像とテキスト（または音声）は同時に提示するほど効果的 | **音声または動画など時間軸を持つ媒体にのみ**適用。静的ページでは空間的接近原理で代替 | ナレーション付き動画では、画像切替とナレーションを同期させる |
| **一貫性の原理** (Mayer, 2009) | 教示目的と無関係な文書・画像・音は学習を阻害する | 「無関係」は学習目的から見た判定。面白さや装飾性は保持の根拠にならない | 装飾画像・余談・BGM・装飾的アニメーションは除去 |
| **モダリティの原理** (Mayer, 2009) | 視覚＋聴覚の分担は視覚独占より有効（視覚チャネル過負荷回避） | **音声モダリティを含む媒体（動画・音声教材）でのみ**適用。静的テキスト＋画像の媒体では無関係 | ナレーションと同一文章を画面に出さない |
| **冗長性の原理** (Mayer, 2009) | 学習上の役割がないまま同じ完全な情報を複数フォーマットで重複提示すると統合コストが増える | 対象名・短いラベル・番号など、表現同士を対応付ける identity cue は単純な重複とは扱わない。冗長性は「同じ手順・説明を別経路でもう一度読ませるか」で判断する | visual-primary なら画像で位置・順序を伝え、本文は hover/click の違い・入力値・注意点など画像だけでは確定しにくい情報に絞る |
| **セグメンティングの原理** (Mayer, 2009) | 学習者がペースを制御できる単位に分割するほど効果的 | セグメント単位は**1つの意味的に閉じたサブゴール**。単一画面・単一状態内の連続操作は原則 1 セグメント。画面遷移・状態遷移・モード切替が自然な境界 | 画面内の項目数で機械的にセグメントを割らない。画面遷移で区切る |
| **分割注意の原理** (Ayres & Sweller, 2021) | 空間的に離れた複数の情報源を統合する必要があると外在的処理が増大する | スクリーンショットと注釈テキストの**物理的距離**が問題。空間的接近原理と相補関係にあるが、こちらは**離れた情報源の統合コスト**に焦点を当てる | 番号吹き出し付きスクリーンショットと説明テキストを隣接配置する。ページ下部にまとめた「設定一覧表」から遠いスクリーンショットを参照させる構成を避ける |
| **ミニマリズム P1: 行動志向** (van der Meij & Carroll, 1995; Carroll, 1990) | 学習者はすぐ行動しながら学ぶ（doing で学ぶ）。最初のアクションへの到達を最短にする | 適用対象は**まだ不要な情報の除去**。必要情報の補完的分担(→ マルチメディア原理)を削ることは含意しない | 前置きの概念説明を最小化し、最初の Action を早める。Concept は first-use 直前に置く |
| **ミニマリズム P2: タスク領域への定着** (van der Meij & Carroll, 1995) | 教材は学習者の実際の目標とタスクに基づく。機能ベースではなく目標ベースで構成する | 「実タスク」は学習者が**本当に達成したいこと**を指す。ソフトウェアの機能一覧に沿った構成はこの原則に違反する | 最上位 Section の goal は学習者の実タスク上の成果物で記述する。入れ子 Section の goal で「なぜこの小手順を行うのか」を実タスク文脈で説明する |
| **ミニマリズム P3: エラー認識・回復の支援** (van der Meij & Carroll, 1995) | エラーは学習機会であり、予防・検出・診断・回復の全段階を支援する | Recovery コンポーネントは**回復手順のみ**を扱う。予防（操作前の注意喚起）と検出（エラー症状の記述）も別途必要 | Recovery に加えて、失敗しやすい操作の**直前**に予防的注意を置く。Recovery 内では「症状→原因→回復手順」の3段構成で書く |
| **ミニマリズム P4: 柔軟な利用の支援** (van der Meij & Carroll, 1995) | 学習者は文書を最初から順に読まない。拾い読み・飛ばし読み・逆引きを支援する | 本スキルの主対象は**順序付きチュートリアル**であるため、完全な非線形設計は求めない。ただし各 Step は可能な限り自己完結させる | 各 Step 冒頭の goal で「この Step で何ができるようになるか」を宣言し、途中参入者が必要な Step を特定できるようにする。Concept と Reference を折りたたみにして既知の読者がスキップできるようにする |
| **シグナリングの原理** (Mayer, 2009) | 重要箇所を視覚的手がかりで強調すると注意配分が改善し本質処理に集中できる | 合図は**学習目的に沿った要素**にのみ付ける。装飾目的の強調・感情表現の太字は一貫性原理違反 | Section の goal 宣言、画像の番号吹き出し、太字 UI 要素名、①②③ の順序番号で重要箇所を示す |
| **事前トレーニングの原理** (Mayer, 2009) | キー用語の名前と特徴を事前に提示すると主学習時の外在的処理が下がる | 予習は**これから出る概念のみ**に限定。遠い将来に出る概念や全体概論はミニマリズム違反 | Concept は first-use の直前に置き、「名前＋鍵となる特徴」を最小単位で提示する |
| **個人化の原理** (Mayer, 2009) | 会話的・直接的な文体は、過度にフォーマルな文体より学習を助ける条件がある | 効果は媒体・課題・対象者で変わる。日本語の主語省略や敬体を機械的な「二人称必須」へ変換しない | 自然で直接的な能動文を優先する。「〜しましょう」「〜してください」等は使えるが、固定テンプレートにはしない |
| **生成活動の原理** (Mayer, 2014) | 学習者に要約・予測・説明・検索などの学習関連活動を求めると学習が深まる | 活動は**Section の学習目標に整合**していること。単なる作業追加は一貫性原理違反 | 目標に応じて Verify / QuickCheck / Checkpoint / Exercise から適切な closure を選び、学習者自身に結果・理解・転移を確認させる |
| **熟達度反転効果** (Kalyuga, 2007) | 初心者に効く合図・概念予習・詳細説明は熟達者には逆効果になる | 本スキルは**初〜中級者向け**に最適化。熟達者向け資料では Signaling・Concept 密度・narrative を縮退させる | 対象者は authoring context / metadata で明示し、原理の適用量を対象者に合わせる |
| **フィードバックの原理** (Shute, 2008) | 学習者が自分の行動・理解・適用結果を具体的に確認できると学習が促進される | すべてのSectionへ同じ部品を強制しない。**substantive learning goal は、その目標を実際に検証できる closure で閉じる**。Recovery は失敗時支援でありclosureの代替ではない | 動作結果なら Verify、概念想起なら QuickCheck、複数条件のmilestone確認なら Checkpoint、別条件への適用なら Exercise を選ぶ |
| **ワークトエグザンプル効果** (Sweller, 1985; Atkinson et al., 2000) | 完全な解法例を示してから自力演習に移す方が、最初から演習するより初心者には効果的 | 熟達が進むと逆転（Expertise Reversal）して演習先行が有効になる。本スキルは初〜中級向けなので**例→演習**の順を優先 | 新しい手順や概念では、まず適切な primary representation を使った完結した worked example を通しで示してから、変化点を差し替える演習（Exercise）を置く |
| **既有知識の活性化** (Merrill, 2002) | 新しい知識を学ぶ前に、学習者が既に持っている関連知識を呼び起こすと学習が促進される | 事前トレーニング原理（未知の用語を教える）とは異なり、こちらは**既知の概念との接続**を促す。対象が beginner-to-intermediate であっても、隣接領域の経験は存在する | 新しい概念を導入する際に「〜を使ったことがあれば、それと同じ仕組みです」のような既知概念へのアンカーを Concept 内で提供する |

**Citation note**: The Mayer principles above cite the 2nd
edition (Mayer, 2009) which defined 12 principles. The 3rd
edition (Mayer, 2021) expanded to 15, adding Split-attention,
Transient information, and Immersion. This skill incorporates
Split-attention (relevant to static tutorials) and notes
Immersion as out-of-scope. Transient information applies to
video/animation tutorials and is not covered here; consult
Jiang & Sweller (2021) when authoring such content.

**Boundary-condition note**: Cromley & Chen's 2025 meta-analysis of
Mayer's multimedia-learning corpus (92 articles, 181 studies, 591
effects) found substantial moderation by design principle, medium,
learning outcome, age, domain, and other study characteristics, with
active-learning interventions showing stronger effects than design
changes overall. Treat multimedia principles as evidence-informed
defaults with boundary conditions, not as unconditional formatting
laws. Keep hard MUST language for requirements whose scope is clear
(e.g. accessibility, structural validity, or an explicit local
contract); use judgement where the research does not justify a
universal threshold.

Updated sources used for this revision:

- Sweller, J., van Merriënboer, J. J. G., & Paas, F. (2019).
  *Cognitive Architecture and Instructional Design: 20 Years Later*.
  <https://doi.org/10.1007/s10648-019-09465-5>
- Cromley, J. G., & Chen, R. (2025). *A meta-analysis of Richard
  Mayer's multimedia learning research: Searching for boundary
  conditions of design principles across multiple media types*.
  <https://doi.org/10.1016/j.edurev.2025.100730>
- W3C. *Web Content Accessibility Guidelines (WCAG) 2.2*.
  <https://www.w3.org/TR/WCAG22/>

### Principles not applicable to static text-and-image tutorials

The following are canonical CTML principles, but they require
audio or speaker presence and therefore are **not applicable**
to static text-and-image tutorials. If the artefact is a
narrated video or an avatar-driven walkthrough, these
principles MUST be applied from the primary sources — this
skill does not cover their application.

| Principle | Applies to | Why out of scope here |
|---|---|---|
| **Voice principle** (Mayer, 2009) | 音声ナレーション媒体 | 人間の声 vs 機械音声の比較。静的ページに音声はない |
| **Image principle** (Mayer, 2009) | 動画教材で話者の画像を画面に出すか | 話者の顔映像の有無は静的ページで判断不能 |
| **Embodiment principle** (Mayer, 2014) | 動画で話者がジェスチャーを伴うか | ジェスチャーは動画特有 |
| **Immersion principle** (Mayer, 2021) | VR / 没入型媒体 | 本スキルは 2D 静的ページに限定 |

Authors writing narrated video or VR content MUST NOT assume
this skill covers these principles; apply them separately from
Mayer & Fiorella (2021), *Cambridge Handbook of Multimedia
Learning* (3rd ed.).

## Task component composition

Tutorials are composed from local task components, not from a
page-wide classification. A document may mix explanation,
Action, Verify, QuickCheck, Exercise, Reference, and other
components wherever the learner's immediate task requires them.
There is no fixed page-wide flow; preserve local contiguity,
task anchoring, and clear feedback instead.

Use these components where needed:

```
Document
 ├── Prerequisites — what the learner needs before a dependent task (optional)
 ├── Explanation prose — short task context when no component is needed
 └── Section (recursive) — milestone or sub-goal; `goal` required at depth 0
      ├── goal — future-declarative sentence at top level; optional when nested
      ├── Concept × N — term/background, collapsible, before first use
      ├── Reference × N — lookup tables, collapsible, near relevant sub-section
      ├── Action × N — atomic operation using an appropriate primary representation
      ├── Recovery — error recovery, inline, after the action that can fail
      ├── Verify — "→ expected result" (1 text line; optional result screenshot)
      ├── QuickCheck / Exercise — problem content → Hint+ → Answer
      ├── Section × N — nested group of actions toward one sub-goal
      ├── Checkpoint — optional checklist when a multi-condition milestone needs it
      └── NextSteps — concrete follow-up actions when the document ends
```

A single `<Section>` component is used recursively — it replaces what earlier
versions of this skill called `<Step>` (top-level milestone) and `<Procedure>`
(sub-goal grouping). Nesting depth is computed at compile time and mapped to
`h2` (depth 0) → `h3` → `h4` → … capped at `h6`.

## Task component display rules

| Type | Content | Display | Placement |
|---|---|---|---|
| **Prerequisites** | Required environment, software versions, prior knowledge, completed prior tutorials | Always visible, bullet list | Page top, before the first top-level Section |
| **Action** | One atomic learner operation | Always visible. Choose the most efficient primary representation: visual, code/CodePreview, text, or diagram | Inside a Section (nested or top-level) |
| **Verify** | Observable result confirmation + optional result-state screenshot | Always visible, `→` prefix; use when the goal is proved by an observable state | At the natural result boundary, not mechanically after every Action |
| **Concept** | One need-now term or idea | Collapsible (`<details>`) | Immediately before first use |
| **Reference** | Lookup details that need not stay in working memory | Collapsible (`<details>`) | Near the Section that needs it |
| **Recovery** | Error diagnosis and recovery | Always visible, short | After the Action that can fail; never counts as goal closure |
| **QuickCheck** | Short retrieval / understanding check | Problem content, one or more Hint blocks, then Answer | Where retrieval best tests the current learning goal |
| **Exercise** | Applied practice / transfer task | Problem content, one or more Hint blocks, then Answer | After enough worked or guided support for the requested independence |
| **Checkpoint** | Multi-item observable milestone checklist | Always visible | Only when several conditions together define a meaningful milestone |
| **Next steps** | What to do after completing this tutorial | Always visible, bullet list | At the document end |

## Primary Representation hierarchy

Choose the representation that communicates the learner's operation with
the least avoidable integration work. Images are one option, not a default
requirement.

| Operation | Typical primary representation | Useful secondary information |
|---|---|---|
| Spatial UI path, layout, visual relationship | Annotated visual | Short identity/gesture text where the visual cannot disambiguate hover, click, drag, or an exact value |
| Code authoring or code change | Code / CodePreview | Brief prose naming the intent, changed region, or observable result |
| Short non-spatial command or setting | Text | Visual only when location or appearance is genuinely hard to find |
| Structural relationship or state flow | Diagram / visual | Text for semantics that shapes/arrows alone do not establish |
| Motion-dependent continuous operation | Video/GIF when the medium supports it | Text equivalent and key values for accessibility and scanning |

The author MUST NOT duplicate the **same complete procedure** across two
representations. Small identity cues are allowed when they bind the
representations together; for example, a visual callout labelled
`Settings` and a sentence that says "**Settings** を開きます" can be useful
rather than redundant.

## Atomic unit: Action

An Action represents one atomic learner operation. Its primary
representation may be visual, code, text, or diagram:

```
[Primary representation] + [only the complementary information needed to act]
```

Rules:

- The author MUST choose a primary representation deliberately instead of
  adding a screenshot to every operational step.
- When a visual is primary, place it directly adjacent to the complementary
  text. When code is primary, keep the explanation adjacent to the relevant
  code or CodePreview.
- The author MUST NOT restate the same complete sequence in text when the
  primary representation already communicates it.
- Identity cues, exact typed values, user-specific paths, and distinctions a
  static visual cannot reliably encode (e.g. hover vs click, drag direction)
  MAY appear in text even when they are also visible in the primary visual.
- Multiple images inside one Action are an authoring smell, not an automatic
  structural failure. Prefer one annotated composite or split into multiple
  Actions when that reduces integration cost. *(mechanised advisory:
  `tutorial/action-single-image`)*
- Reducing Action text to a bare verb such as "クリックします" MUST NOT be
  used as a redundancy fix. Keep enough context for the learner to identify
  the operation without guessing.
- If an Action produces an immediate visible result needed for the next
  operation, state it inline when useful. Use a separate `<Verify>` only when
  the observable state itself is the natural closure for a learning goal or
  meaningful sub-goal.

## Signaling (visual cueing)

学習者の注意を本質的な情報に誘導するために、情報階層を**視覚的な
合図**で表現する。合図は学習目的に沿った要素にのみ付ける。

Signaling surfaces in this skill:

| Surface | Cue | Purpose |
|---|---|---|
| Section heading (depth 0) | `goal` banner (future-declarative, required) | Section の到達点を宣言 |
| Section heading (nested, depth > 0) | `goal` banner (optional) | サブゴールをタスク言語で宣言 |
| Action image | Numbered callout (①②③) + arrow | Position / Sequence を強調 |
| Action text | Bold for unlabelled UI element names, typed values, key gestures | Identity / Typed value の強調 |
| Verify / Recovery | Component framing (→, title) | 状態判定と回復手段の境界を明示 |

Rules:

- 合図は**必ず学習目的に沿う**こと。装飾目的の太字、感情表現の
  強調、文末の飾り記号は Signaling ではなく一貫性原理違反。
- 画像の番号吹き出しと本文の番号・ラベルは、両方を読むことで対応
  関係が明確になる場合に併記してよい。対応付けのための cue を機械的に
  Redundancy とみなさない。
- 太字の濫用（1 文に 3 箇所以上など）は合図の効力を破壊するため
  禁止。強調は本当に注視すべき要素のみに絞る。

## Personalization (reader-addressing voice)

Use natural, direct, active language. Conversational tone can help, but do
not turn the principle into a rigid Japanese second-person template.

Rules:

- Prefer learner-facing task prose such as 「〜しましょう」「〜してください」
  when it reads naturally.
- Japanese zero-subject sentences are acceptable; explicit 「あなた」 is not
  required.
- Personalization is about **friendliness, not familiarity**. Emoji spam,
  余談, and emotional decoration can still violate Coherence.
- Goal strings already use future-declarative form. Keep them learner-facing
  and direct; do not rewrite them as author-facing audience descriptions.

### Learner-facing prose quality convention

The following is a **local authoring convention**, not a claim that Mayer's
Personalization principle scientifically forbids particular Japanese nouns.

- Keep audience classification and authoring rationale out of learner-facing
  prose when they do not help the learner perform the task.
- Avoid meta phrases such as 「受講者は〜」「学習者は〜」「初学者向け」
  in the tutorial body; rewrite them as direct task prose.
- Do not ban the word 「ユーザー」 globally. It is legitimate when it refers
  to an actual end user or domain actor, rather than to the tutorial reader
  as authoring metadata.

## Accessibility (authoring obligations)

visual / code / text を組み合わせるチュートリアルでは、アクセシビリティは
**プラットフォーム実装の責務**と**オーサリングの責務**の両方にまたがる。以下はオーサ
リング段階で著者が守るべき最低限のルール（WCAG 2.2 Level AA 準拠、
Section 508 E205 の教育・訓練資料要件に基づく）。

Rules:

- Every informative `<Action>` / `<Verify>` image MUST have an `alt`
  prop whose text equivalent preserves the information needed to follow
  or verify the step. For spatial UI visuals this often includes WHERE;
  for diagrams or result images it may instead describe relationships or
  observable state. If an image is genuinely decorative, use `alt=""`.
- Numbered callouts, arrows, and highlights in images MUST NOT
  rely on colour alone to convey meaning. Pair colour with
  shape (numbered circles, arrows with labels) so that readers
  with colour vision deficiencies can follow the sequence
  (WCAG SC 1.4.1).
- When an image conveys information not present anywhere in the
  surrounding text (e.g. a UI layout, a spatial relationship
  between panels), the author MUST provide a text equivalent
  nearby — either in the Action text, a Concept, or a
  Reference — so that the meaning is recoverable without the
  image.
- Text annotations overlaid on screenshots are text / images of
  text and MUST meet WCAG 2.2 SC 1.4.3: **4.5:1** for normal text,
  or **3:1** for large text. Meaningful non-text callout shapes,
  focus indicators, and graphical objects use the **3:1**
  non-text contrast requirement from SC 1.4.11 where applicable.
- Prefer real text to images of text whenever the same visual
  presentation can be achieved with text (WCAG 2.2 SC 1.4.5).
- The tutorial's heading hierarchy is produced by `<Section>`
  nesting depth (depth 0 → `h2`, depth 1 → `h3`, … capped at
  `h6`). The `remark-section-headings` plugin injects these
  semantic headings automatically so that screen-reader
  navigation by heading works correctly.
- Interactive examples or embedded widgets (if any) MUST be
  operable by keyboard alone in a logical tab order.

## Generative activity (prediction / retrieval)

学習者が**受動的に読むだけ**にならないよう、生成活動（予測・
説明・自己確認）を組み込む。活動は必ず学習目的に関連させる。

Surfaces:

| Surface | Generative / closure role |
|---|---|
| Verify | 直前の goal の結果を**観察判断**させる |
| Checkpoint | 複数条件からなる meaningful milestone を**自己確認**させる |
| QuickCheck | Concept / Action の理解を短く取り出す retrieval 活動 |
| Exercise | 別条件への適用・転移を試す応用課題 |
| Recovery | 失敗時の診断と回復を支援する。**closure ではない** |

Rules:

- Verify の文面は「**観察可能な状態**」で書く。内部処理・実行履歴の記述は避ける。
- Every substantive learning goal MUST have an **aligned closure** that
  can actually test that goal. Choose by evidence needed: observable
  behavior/state → Verify; retrieval/understanding → QuickCheck; several
  milestone conditions → Checkpoint; transfer to a new condition → Exercise.
  Do not add all four mechanically.
- Recovery is error support and MUST NOT be counted as closure.
- Checkpoint の項目は学習者自身が視覚・操作で確かめられる内容に限定する。
- Exercise は**学習目的に関連**していること。作業量稼ぎの演習は追加しない。
- QuickCheck and Exercise MUST use this internal order:
  problem content → one or more Hint blocks → Answer.
- 予測プロンプトは、目標の達成確認に役立つときだけ使う。固定頻度で追加しない。

### Progressive independence (scaffolding / fading)

ワークトエグザンプル効果と生成活動原理を組み合わせて、チュートリアル
全体を通して**段階的に足場を外す**構成にする（Van de Pol et al.,
2010; backward fading: Renkl et al., 2002）。

静的チュートリアルにおける段階的撤退の実装:

| Phase | Structure | Learner role |
|---|---|---|
| **Phase 1: 完全例** (序盤の Step) | 各 Action に適切な primary representation と必要十分な補足を示す。Concept で用語を first-use 前に導入し、目標に合う closure で結果を確認する | 観察・模倣（worked example） |
| **Phase 2: ガイド付き変形** (中盤の Step) | 基本手順は示すが、一部の値・選択肢を「〜に変更してみましょう」で学習者に委ねる | 部分的な意思決定（completion problem） |
| **Phase 3: 独立課題** (終盤の Exercise) | Goal と期待結果のみ提示。手順は示さない | 自力での手順構成（independent practice） |

Rules:

- Tutorial の最初の Step は Phase 1（完全例）で始める。
  いきなり Phase 3 の独立課題を出すのはミニマリズム P1 と
  ワークトエグザンプル効果に反する。
- Phase 間の移行は**同種の手順の繰り返し**で自然に起こる。
  同じ操作パターンが 2 回目に出るときに Phase 2 へ、
  3 回目以降に Phase 3 へ移行するのが目安。
- Phase 2 の Exercise では、変更点（差分）を明示し、学習者が
  ゼロから構成する必要がない形にする。
- 足場の撤退量は対象読者の熟達度に比例させる。beginner 向け
  では Phase 1 を長めに、intermediate 向けでは Phase 2 から
  開始してもよい。

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

- The author MUST use an imperative or direct action form that makes the
  learner's next operation unambiguous.
- The author SHOULD bold only identifiers or values that materially help
  the learner bind the instruction to the primary representation. A short
  UI label may appear in both image and text when it functions as an
  identity cue rather than a second full instruction.
- Positional wording (e.g. "右上の") MAY remain when it materially reduces
  search or disambiguates the target. Remove it only when it adds no useful
  information; do not enforce this lexically.
- Values the learner must type, user-specific paths, and gestures/motions
  (drag direction, hover vs click) MUST remain available in text or another
  accessible equivalent because a static screenshot may not communicate
  them reliably.

### Concept text

Concept serves the **Pre-training** principle: it teaches the
*name* and the *key features* of a term the learner is about
to encounter, so that main-task cognitive load is reduced.

- A Concept MUST focus on **one new concept** and include only the
  information the learner needs for the imminent first use.
- A Concept MUST answer "what is it?" and "why does the learner need to know right now?".
- A Concept MUST be placed immediately before the first Section or Action
  that uses the term.
- Concepts for terms that appear much later MUST NOT be written now.
- Prefer roughly **2–5 sentences** or one short table. This is a readability
  heuristic, not a hard limit. At 6+ sentences, review whether the block
  contains multiple concepts or reference detail that should be split or
  moved to `<Reference>`. *(mechanised advisory: `tutorial/concept-length`)*

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

### Prerequisites text

- Prerequisites MUST appear at the page top, before the first
  top-level Section.
- Each prerequisite MUST be actionable or verifiable: state
  the required software version, completed prior tutorial,
  or assumed knowledge concretely.
  - ✅ 「Unreal Engine 5.4 以上がインストール済みであること」
  - ✅ 「Step 1〜3（前回のチュートリアル）を完了していること」
  - ❌ 「基本的な知識があること」(what knowledge?)
- If no prerequisites exist, omit the section entirely (do not
  write "特になし").

### Recovery text

Recovery serves **ミニマリズム P3** (error recognition and
recovery support). It covers the full error lifecycle:
prevention, detection, and correction.

- A Recovery block MUST be placed **after** the Action that can
  plausibly fail.
- A Recovery block MUST follow the structure: **symptom →
  cause → fix** (in that order). The symptom comes first
  because the learner sees the symptom, not the cause.
  - ✅ 「ブループリントが動かない場合 → コンパイルエラーが
    出ていないか確認してください → ノード名のタイプミスが
    原因です。正しい名前は〜」
  - ❌ 「うまくいかない場合はやり直してください」
- For actions with a high failure probability, the author
  SHOULD place a **preventive note** (1 sentence) immediately
  before the Action, warning about the common mistake. This
  note is distinct from Recovery (which is reactive).
- Recovery MUST NOT be placed at the end of a Section as a
  catch-all. Each Recovery block addresses a specific failure
  point.

### Next steps text

- Next steps MUST appear only at the document end (inside the final
  top-level Section or immediately after it, according to the platform's
  supported composition).
- Each item MUST link to a concrete next action: another
  tutorial, a documentation page, or an exercise.
- The author MUST NOT use vague pointers ("詳しくは公式
  ドキュメントを参照してください" without a link).

### Checkpoint

- Use a Checkpoint when **several observable conditions together** define a
  meaningful milestone that benefits from a compact checklist.
- A Checkpoint MUST be a bullet list of observable behaviors or states.
- A Checkpoint MUST NOT include internal state or jargon.
- Do not add a Checkpoint merely because a Section exists, and do not require
  it to be the final element when a different aligned closure better matches
  the goal.

## Anti-patterns (do NOT do)

Judgement-based anti-patterns; a tool cannot reliably detect
these, so the author is responsible for catching them.

| Anti-pattern | Violated principle | Fix |
|---|---|---|
| Same complete procedure restated in both the primary representation and secondary prose | Redundancy | Keep one primary path and use secondary representation only for complementary or mapping information |
| Treating a short identity cue repeated across visual and text as automatically redundant | Redundancy (over-applied) | Keep the cue when it helps bind the representations; remove only duplication that makes the learner re-process the full instruction |
| Mechanical splitting of a single-screen unified task into many Actions (one per item in the same dialog) | Segmenting (misapplied) | Keep 1 screen = 1 Action when the sub-goal is unified; split only on screen/state transitions |
| Decorative images, fun sidebars, background music | Coherence | Remove entirely; they impair learning |
| Same content in narration AND on-screen text | Redundancy / Modality | Use narration OR on-screen text, not both |
| `:::note` for concepts | Segmenting | Not collapsible; use Concept component |
| Verify after every action | Segmenting | Verify at Section end only |
| Front-loading reference tables | Minimalism | Use Reference, near first use |
| Term introduced before it's needed | Minimalism | Concept before first-use Section |
| Reducing Action text to a bare "クリックします" to avoid redundancy | Redundancy (over-correction) | Keep the imperative WHAT plus the values the image cannot convey |
| Settings table duplicating the image's numbered callouts row-for-row | Redundancy | Keep in text only the values the image cannot convey (typed input, user-specific paths, dropdown values absent from the shot) |
| Micro-interaction detail ("空白で離す", "カーソルを乗せ") redundantly described when image's arrows already convey it | Redundancy | Remove — but only after confirming the image truly conveys the gesture; motion attributes ("drop in **empty** space", "hover vs click") often need text because a still image cannot encode them |
| Opening a page by describing what the document *is* or *who it is for* ("この教材は〜のための資料です", "受講者が〜する授業") | Personalization | Rewrite in second-person direct address; open with the first learner-facing action or an inviting goal |
| Author-facing audience meta prose in the tutorial body ("学習者は〜", "初学者向け", "受講者が〜") | Learner-facing prose quality convention | Rewrite as direct task prose; keep audience classification in authoring context/metadata instead of the lesson body |
| Front-loading a long concept chapter before the first Action (Pre-training misapplied) | Pre-training × Minimalism | Move each term's Concept to immediately before its first-use Section; keep each Concept to name + key features only |
| Bold/highlight used for emotional emphasis or decoration, not tied to a learning-objective cue | Signaling × Coherence | Reserve bold/highlight for the element the learner must find or type; remove decorative emphasis |
| Multiple bold spans crammed in one sentence | Signaling (dilution) | Bold only the single element that most matters; demote the rest to plain text |
| Verify line that describes internal mechanics instead of observable state ("Destroy Actor が実行されました") | Generative activity | Rewrite as an observable outcome the learner can check ("キューブが消えれば成功") |
| Exercises tacked on for practice volume rather than learning objective | Coherence / Generative activity (misapplied) | Tie every Exercise to the Step's stated goal; drop unrelated drills |
| Applying beginner-weight Signaling/Concept density to an expert-facing reference | Expertise reversal | Scale back: use compact Reference tables, drop hand-holding narrative |
| Using `<Action img>` to show a result-state screenshot while the text contains result-check language ("〜になれば成功", "〜ていることを確認") | Feedback (Verify workaround) | Replace with `<Verify img="...">` — the image carries the observable result state, the text carries the 1-line confirmation *(mechanised: `tutorial/verify-visual-workaround-as-action`)* |
| Organising tutorial sections by software feature/menu rather than by learner's task goal | ミニマリズム P2 (task anchoring) | Reorganise by what the learner wants to achieve, not by where the feature lives in the UI |
| No Recovery block for a common or high-impact novice failure mode | ミニマリズム P3 (error support) | Add Recovery with symptom → cause → fix structure at the specific failure point |
| Recovery that says "やり直してください" without diagnosing the cause | ミニマリズム P3 (error support) | Rewrite with concrete symptom, cause, and fix |
| All Steps require reading every prior Step to make sense; no standalone entry point | ミニマリズム P4 (flexible use) | Make each Step's goal self-explanatory; use collapsible Concepts/References so known readers can skip |
| Tutorial starts without stating required environment, software version, or prior knowledge | Prerequisites (ISO 26514) | Add a Prerequisites section at the page top listing concrete, verifiable requirements |
| Images with no `alt` text, or `alt` text that says "screenshot" / "image" | Accessibility (WCAG SC 1.1.1) | Write `alt` that describes WHERE information: which panel, button, or area is shown |
| Numbered callouts or highlights that use colour alone (no shape or label) to convey sequence | Accessibility (WCAG SC 1.4.1) | Pair colour with numbered circles, arrows with text labels, or other shape cues |
| Jumping straight to independent exercises without first showing a complete worked example | Scaffolding / Worked example | Start with Phase 1 (full example), then Phase 2 (guided variation), then Phase 3 (independent) |
| Introducing a new concept without connecting it to anything the learner already knows | Activation (Merrill) | Add an analogy or reference to a familiar concept in the Concept block |
| Screenshot + explanation table placed far apart, requiring the reader to scroll between them | Split-attention | Place the explanation immediately adjacent to (or overlaid on) the screenshot |

## Mechanised checks (enforced at MDX build/dev time)

The following conventions are enforced by the
`remarkTutorialLint` plugin in
`@metyatech/course-docs-platform`. Violations surface in
`npm run dev` and `npm run build` output; author reliance on
memory is not required.

### Severity policy (evidence-tiered)

Severity is tied to how strongly the rule is anchored in the
underlying research, so the tool does not over-reach.

| Severity | Semantics | Build effect |
|---|---|---|
| **error** | Structural break that makes the MDX incoherent or loses required authoring structure | Fails the MDX compile |
| **warn**  | Principle violation with solid empirical support, or a render/technical bug | Emitted via `console.warn` + `file.message()`. Fails under `TUTORIAL_LINT_STRICT=1` |
| **note**  | Advisory derived from a principle whose specific numeric threshold or lexical pattern is a professional guess rather than a direct research finding | Emitted via `console.info` only. **Never** promoted to an error, even under strict. In collect-all mode, notes appear in the summary but do not by themselves fail the build |

`TUTORIAL_LINT_COLLECT=1` aggregates every finding in a file
into a single failure message, so a PR author can fix all
violations in one pass instead of one at a time. If the
aggregated collection contains only notes, the summary is
printed via `console.info` and the build still passes.

### Rule → severity mapping

| Rule ID | Severity | Intent |
|---|---|---|
| `tutorial/section-goal-required` | **error** | Every top-level `<Section>` declares its `goal`; nested Section goals are optional |
| `tutorial/action-single-image` | *note* | An Action contains multiple images; review whether one annotated composite or multiple Actions would reduce integration cost |
| `tutorial/section-no-hrule` | warn | No `---` inside a Section |
| `tutorial/verify-no-duplicate-arrow` | warn | `<Verify>` body starts with `→` — component already renders it |
| `tutorial/section-lacks-closure` | warn | A substantive Section with learner work has no aligned `<Verify>` / `<QuickCheck>` / `<Checkpoint>` / `<Exercise>` closure; `<Recovery>` does not satisfy closure |
| `tutorial/section-goal-tense` | *note* | Goal endings matching heuristic future-declarative patterns |
| `tutorial/reference-image-only` | *note* | `<Reference>` whose only content is an image |
| `tutorial/action-bold-overuse` | *note* | 6+ bold spans in one Action |
| `tutorial/third-person-reader` | *note* | Learner-audience meta prose (e.g. 受講者 / 学習者 / 初学者向け) matches a local quality-convention heuristic; ordinary domain uses of 「ユーザー」 are not included |
| `tutorial/page-opens-with-doc-description` | *note* | First paragraph starts with "この教材は〜" etc. |
| `tutorial/verify-internal-mechanics` | *note* | Verify text matches the engine-state pattern list |
| `tutorial/concept-length` | *note* | Concept body reaches 6+ sentences; review whether it contains multiple concepts or reference detail |
| `tutorial/concept-placement` | *note* | Concept has no following Action / Section / Exercise |
| `tutorial/decorative-emoji` | *note* | Non-allowlisted emoji outside signalling surfaces |
| `tutorial/verify-visual-workaround-as-action` | *note* | `<Action img>` whose text matches result-check patterns — likely a Verify disguised as an Action |
| `tutorial/prerequisites-placement` | warn | `<Prerequisites>` appears after the first `<Section>` |
| `tutorial/nextsteps-placement` | *note* | `<NextSteps>` appears before the last `<Section>` |

The *note* tier exists because these rules are correct in
principle but their specific numeric boundary or lexical
trigger has no direct empirical backing — they are the
authoring equivalent of professional code review hints, not
hard gates.

## Forbidden notation

- Do not add `authoringMode` frontmatter or any tutorial /
  non-tutorial page classification. Components are used locally
  where the task needs them.
- Do not use Solution notation or any separate Solution block. Use
  `<Answer>` inside QuickCheck or Exercise after one or more
  `<Hint>` blocks.

## Component system (course-docs-platform)

When writing for `@metyatech/course-docs-platform`-based sites,
the author MUST use the provided MDX components where they serve
the local task. They are globally available (no import needed):

```mdx
<Section title="Step N：コリジョンを設定する" goal="アイテムに触れると消えてスコアが増えるようになります">

  <Concept title="コリジョンとは">
    当たり判定のこと。ブロック＝壁、オーバーラップ＝すり抜け＋検知。
  </Concept>

  <Section title="N-1. 触れたことを検知できるようにする" goal="アイテムをすり抜けて通れるようになります">
    <Action img="./img/overlap-events-on.png">
      **Generate Overlap Events** をオンにする
    </Action>
    <Action img="./img/overlap-all-dynamic.png">
      **コリジョンプリセット**を **OverlapAllDynamic** に変更する
    </Action>
    <Verify>アイテムをすり抜けて通れる</Verify>
  </Section>

  <QuickCheck>
    アイテムをすり抜けつつ接触を検知する設定はどれですか？
    <Hint>ブロックではなく、すり抜けながら検知する設定です。</Hint>
    <Answer>Overlap です。</Answer>
  </QuickCheck>

  <Checkpoint>
    - アイテムに触れるとスコアが増える
    - アイテムに触れると消える
  </Checkpoint>

</Section>
```

A single `<Section>` is used recursively at both the milestone
level (depth 0) and the sub-goal grouping level (depth > 0).
Nesting depth maps to heading level: `h2` → `h3` → … capped at
`h6`.

### Components

| Component | Props | Purpose |
|---|---|---|
| `<Prerequisites>` | children | Page-level requirements; placed at page top before the first Section |
| `<Section>` | `title: string` (required), `goal?: string` (required at depth 0, optional deeper) | Recursive milestone / sub-goal container; replaces the legacy `<Step>` and `<Procedure>` |
| `<Action>` | `img?: string`, `alt?: string`, children | Atomic operation with optional screenshot |
| `<Verify>` | `img?: string`, `alt?: string`, children | Observable result closure when the goal is proved by state/behavior; `img` may show the expected result state |
| `<Concept>` | `title: string`, children | Collapsible background/term; supports expertise-scaled default-collapse (see `?level=` query) |
| `<Reference>` | `title: string`, children | Collapsible lookup table |
| `<Recovery>` | `title: string`, children | Inline error-recovery block attached to the preceding Action |
| `<Checkpoint>` | children | Optional checklist for a meaningful multi-condition observable milestone |
| `<QuickCheck>` | children | Short retrieval prompt using problem content → Hint+ → Answer |
| `<Exercise>` | children | Applied practice using problem content → Hint+ → Answer |
| `<Hint>` | children | Progressive support inside QuickCheck or Exercise |
| `<Answer>` | children | Final answer inside QuickCheck or Exercise |
| `<NextSteps>` | children | End-of-tutorial next actions with links; placed at the document end |

## Non-component tutorials

When components are not available (plain Markdown, Docusaurus,
etc.), the author MUST preserve the same component semantics
using native syntax:

| Component equivalent | Plain Markdown |
|---|---|
| Prerequisites | `## 前提条件` + bullet list at page top |
| `<Section>` (depth 0) | `## タイトル` + first line = goal sentence |
| `<Section>` (nested, depth 1+) | `### タイトル` / `#### タイトル` (heading level = Markdown depth + 2, capped at `######`) |
| `<Concept>` | `<details><summary>💡 Title</summary>...</details>` |
| `<Reference>` | `<details><summary>📖 Title</summary>...</details>` |
| `<Action>` | Use the native representation best suited to the action: adjacent image + instruction, code fence + instruction, direct numbered instruction, or diagram + instruction |
| `<Verify>` | `**→ expected result**` |
| `<Recovery>` | `:::caution[〜のとき]` or equivalent admonition right after the Action |
| `<Checkpoint>` | `:::tip[確認ポイント]` or equivalent admonition |
| `<QuickCheck>` | Short question, collapsible Hint(s), then `**答え:** ...` |
| `<Exercise>` | Practice prompt, collapsible Hint(s), then `**答え:** ...` |
| Next steps | `## 次のステップ` + bullet list with links at the document end |

The component meanings and writing rules MUST remain identical
regardless of tooling.

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
| "Is this prose natural learner-facing task prose, or author-facing audience/meta prose?" (local quality convention) | Japanese grammar allows zero-subject sentences and domain prose may legitimately describe an app's end user; lexical matching over-triggers |
| "Does this Exercise serve the stated Section goal?" (Generative activity × Coherence) | Requires semantic alignment with the Section's goal string |
| "Is this Concept's 'why does the learner need to know now?' actually satisfied?" (Pre-training) | Intent-level check |
| "Is Signaling density appropriate for the target learner?" (Expertise reversal) | Requires modelling the reader's prior knowledge |
| "Does this `alt` text preserve the information the image contributes to this Action or Verify?" (Accessibility) | Requires understanding whether the image contributes location, relationship, sequence, or result-state information |
| "Does this Recovery follow symptom → cause → fix, and is the symptom what the learner actually sees?" (ミニマリズム P3) | Requires knowing the real failure mode, not just the technical cause |
| "Is this Exercise at the right scaffolding phase (1/2/3) for this point in the tutorial?" (Scaffolding) | Requires tracking cumulative learner exposure to the pattern |
| "Does this Concept's analogy accurately bridge to prior knowledge the target learner has?" (Activation) | Requires modelling the reader's adjacent-domain experience |

### Generalisation limits of the underlying research

- Multimedia-learning effects have meaningful **boundary conditions**.
  Cromley & Chen (2025) found substantial moderation across Mayer's corpus
  by principle, medium, learning outcome, age, domain, and other study
  characteristics. Do not assume a principle has the same effect size — or
  even practical relevance — for every software-tutorial step.
- Most studies use novice learners in controlled settings. Real-world
  learners mix expertise levels, read non-linearly, and bring prior
  frustration. The skill's rules are a baseline, not a replacement for
  observing real learners.
- Language and cultural effects on Personalization / Voice have been studied
  mainly in English. Japanese-specific wording conventions are transferred
  cautiously and MUST be labelled as local quality conventions when direct
  evidence is absent.
- The current CLT formulation distinguishes intrinsic and extraneous load as
  the basic load categories; germane processing redistributes working-memory
  resources toward learning-relevant intrinsic processing rather than adding
  a third independent load (Sweller, van Merriënboer & Paas, 2019).

### When principles appear to conflict

1. Remove avoidable **extraneous** processing first.
2. Check the learner's expertise and sequence/segment the task so its
   **intrinsic** element interactivity fits available working memory.
3. Add retrieval, explanation, practice, or feedback only when it is aligned
   to the goal and still fits the learner's remaining capacity; do not treat
   "germane load" as a third load to maximise.
4. If two multimedia principles still conflict, prefer the tactic whose
   boundary conditions best match the current medium, learning outcome, and
   learner population rather than applying a universal hierarchy.
5. If the conflict involves an out-of-scope principle, consult the primary sources.

### Self-review

Use `REVIEW-CHECKLIST.md` (same repository) as a reviewer-facing
checklist. It mirrors the principle table and is the single
place to audit a draft tutorial against every principle in
sequence.
