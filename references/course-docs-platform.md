# Course Docs platform contract

Load this reference only when authoring for a site that uses
`@metyatech/course-docs-platform` or the matching `course-docs` agent rules.

These rules are **local platform contracts and quality conventions**. Do not
present them as universal learning-science requirements and do not force them on
unrelated Markdown/tutorial systems.

This reference documents the learner-facing MDX composition and lint
conventions. Its components are presentation/task formats; do not infer a
platform-level Learning Unit or Learning Event data model from them.

## Component composition

Course Docs tutorials are composed from local task components. There is no
page-wide tutorial/non-tutorial authoring mode and no mandatory fixed page-wide
flow.

Available components:

| Component | Contract / role |
|---|---|
| `<Prerequisites>` | Page-level requirements before the first Section |
| `<Section>` | Recursive milestone/sub-goal container; `title` required; `goal` required only at depth 0 |
| `<Action>` | Coherent learner action episode; optional `img` / `alt` |
| `<Verify>` | Observable result evidence; optional expected-result image |
| `<Concept>` | Collapsible need-now term/background |
| `<Reference>` | Collapsible lookup material |
| `<Recovery>` | Reactive diagnosis/recovery support near a failure point |
| `<Checkpoint>` | Optional checklist for a meaningful multi-condition milestone |
| `<QuickCheck>` | Short retrieval/understanding task |
| `<Exercise>` | Applied task for practice or transfer, depending on its design |
| `<Hint>` | Progressive support inside QuickCheck or Exercise |
| `<Answer>` | Final answer/explanation inside QuickCheck or Exercise |
| `<NextSteps>` | Optional concrete follow-up actions, normally at document end |

A single `<Section>` is recursive. Heading depth is injected automatically:
depth 0 → `h2`, depth 1 → `h3`, and so on, capped at `h6`.

## Instructional horizon

Before choosing representation or assistance, identify whether the lesson or
Section is intended mainly for **initial performance**, **learning (including
retention)**, **transfer**, or a deliberate combination. This is a Course Docs
quality convention rather than an MDX parser requirement.

Do not optimise only first-attempt speed when retention or transfer is an
explicit goal. Representation, fading, QuickChecks, and Exercises should follow
the intended horizon.

## Section goals

Every top-level `<Section>` must declare a non-empty `goal`. Nested Section goals
are optional and should be used when they improve orientation.

This learner-facing Section goal is local to the rendered material; it does not
by itself define a curriculum-level Learning Unit or prove that aligned evidence
has been collected.

Goal text is rendered verbatim below the heading. Write a complete
future-declarative sentence describing what the learner will achieve by the end
of that Section.

Good patterns:

- 「キューブを1つ置きます」
- 「キャラクターを操作できるようになります」
- 「触れたら消えるようになります」

Avoid retrospective/completed wording such as 「〜した」「〜された」 or bare
noun phrases such as 「〜した状態」.

The tense check is heuristic/advisory; the required-goal check is structural.

## Action

`<Action>` uses:

```ts
{
  img?: string;
  alt?: string;
  children: ReactNode;
}
```

An Action may be text-primary, code-primary, or visual-primary. `img` is
optional. A short coherent navigation sequence may remain one Action when it
serves one immediate sub-goal; do not split mechanically per click or field.
The Action **as a whole** must be executable without guessing; visible prose
does not need to duplicate a complete visual-primary path when the visual and a
separate accessible text-equivalent route already carry that information.

Multiple images are an advisory smell, not a structural error. Consider one
annotated composite or multiple Actions when that reduces integration cost.

Positional wording such as 「右上の」 is allowed when it materially reduces
search or disambiguates the target.

## Verify

The component renders its own leading `→`; source text must **not** start with a
literal `→`.

Verify describes observable state/behavior, not internal engine mechanics.

- Good: 「キューブが消えれば成功です」
- Poor: 「Destroy Actor が実行されました」

Use a Verify image only when visual comparison helps establish the expected
result. Do not disguise a result-state screenshot as an Action merely to attach
an image.

## Concept

A Concept should contain one need-now idea and be near its first meaningful
use. The platform lint recognises Action, Section, Verify, QuickCheck, and
Exercise as plausible following usage sites.

Roughly 2–5 sentences or one short table is preferred. Six or more sentences
triggers a note to review whether multiple concepts/reference details are mixed;
it is not a hard failure.

## Recovery

Recovery is not learning-goal closure. Place it after a plausible failure point
and write it as **symptom → likely cause → concrete fix**.

Preventive warnings belong before the risky Action; they are distinct from the
reactive Recovery component.

## QuickCheck and Exercise task structure

In Course Docs, both task components have this **platform contract**:

```text
problem content
→ one or more <Hint> blocks
→ exactly one final <Answer>
```

Hints and Answer must be direct children of the task block. Content after
`<Answer>`, a Hint after Answer, nested task blocks, or the removed legacy
Solution component are invalid.

This structure is local to Course Docs. A generic tutorial outside this platform
may use a different exercise/feedback structure when pedagogically appropriate.

Hints must not reveal the answer immediately and should rely only on material
already established by the lesson/curriculum. An Answer must provide enough
explanation to make the feedback instructive rather than returning only a bare
final token/value. Explain why the answer is correct and address a likely
misconception when one genuinely exists; do not invent a misconception merely
to satisfy the template.

## Aligned closure

A Section containing learner work should have evidence capable of testing its
learning goal. The platform recognises these closure surfaces:

- `<Verify>` — observable state/behavior;
- `<QuickCheck>` — retrieval/understanding;
- `<Checkpoint>` — meaningful multi-condition milestone;
- `<Exercise>` — applied practice or transfer, depending on task conditions.

An Exercise is a task format, not automatic transfer evidence. To support a
transfer claim, change conditions meaningfully and require learners to select or
adapt the learned principle. Align the evidence to the Section's learning goal.

`<Recovery>` does not count as closure.

Do not add every closure component mechanically. A grouping Section with no
local Action does not inherit child-Section Actions merely to satisfy closure.

## Prerequisites and NextSteps

`<Prerequisites>` belongs before the first top-level Section. Omit it when there
are genuinely no prerequisites.

Prerequisites should be concrete and verifiable: required software/version,
completed earlier lesson, or specific assumed knowledge.

`<NextSteps>` is optional. When it is useful, place it at the document end and
link to concrete next actions. Do not add a vague “see official docs” pointer
without a useful destination.

## Learner-facing prose convention

Course Docs keeps author-facing audience/meta commentary out of the learner
body. Avoid phrases such as 「受講者は〜」「学習者は〜」「初学者向け」 when they
only describe the audience or authoring rationale.

Do not ban 「ユーザー」 when it refers to a real app/product end user.

## Emphasis

Use bold for identities/values/gestures that materially help mapping or action.
Do not treat “three bold spans” or any other small number as a scientific
boundary. The current lint note begins at six bold spans in one Action and is a
review heuristic only.

## Forbidden notation

Do not use:

- `authoringMode` frontmatter;
- page-wide tutorial/non-tutorial classification;
- separate legacy Solution blocks.

## Mechanised tutorial lint

Severity is based on artefact impact and machine-detection confidence, not
research strength.

| Rule ID | Severity | Intent |
|---|---|---|
| `tutorial/section-goal-required` | error | Missing/empty top-level Section goal |
| `tutorial/action-single-image` | note | Multiple images in one Action; review integration |
| `tutorial/section-no-hrule` | warn | Horizontal rule inside a Section |
| `tutorial/verify-no-duplicate-arrow` | warn | Verify source starts with `→` |
| `tutorial/verify-shot-action-role` | warn | Verify shot manifest contains action-role annotations |
| `tutorial/section-lacks-closure` | warn | Local Action without aligned closure |
| `tutorial/section-goal-tense` | note | Goal-tense heuristic |
| `tutorial/reference-image-only` | note | Image-only Reference |
| `tutorial/action-bold-overuse` | note | Six or more bold spans in one Action |
| `tutorial/third-person-reader` | note | Learner-audience meta-prose heuristic |
| `tutorial/page-opens-with-doc-description` | note | Document-description opener heuristic |
| `tutorial/verify-internal-mechanics` | note | Verify appears to describe internal mechanics |
| `tutorial/concept-length` | note | Six or more Concept sentences |
| `tutorial/concept-placement` | note | No plausible following usage site |
| `tutorial/decorative-emoji` | note | Non-allowlisted emoji outside signaling surfaces |
| `tutorial/verify-visual-workaround-as-action` | note | Action image looks like Verify result state |
| `tutorial/prerequisites-placement` | warn | Prerequisites after first Section |
| `tutorial/nextsteps-placement` | note | NextSteps before last Section |

Warnings become build-failing only under `TUTORIAL_LINT_STRICT=1`. Notes never
become errors. `TUTORIAL_LINT_COLLECT=1` aggregates findings for review.

The live platform source and tests are the final source of truth for exact rule
IDs, severities, and parser behavior. Keep this reference synchronized with
`packages/platform/src/mdx/tutorial/remark-tutorial-lint.ts` rather than treating
a copied table as independently authoritative.

## Example

```mdx
<Section
  title="Step 1：コリジョンを設定する"
  goal="アイテムをすり抜けながら接触を検知できるようになります"
>
  <Concept title="オーバーラップとは">
    オーバーラップは、相手をブロックせずに接触を検知する設定です。
  </Concept>

  <Action img="./img/overlap.png" alt="コリジョン設定画面">
    **Collision Presets** を **OverlapAllDynamic** に変更します。
  </Action>

  <Verify>アイテムをすり抜けて通れれば成功です</Verify>

  <QuickCheck>
    ブロックせず接触を検知する設定は何ですか？
    <Hint>すり抜けながら検知する設定名を思い出してください。</Hint>
    <Answer>Overlap です。相手をブロックせず、接触だけを検知する設定です。</Answer>
  </QuickCheck>
</Section>
```

## Plain Markdown outside Course Docs

Preserve the **pedagogical roles** when useful, but do not pretend Course Docs
component syntax is universally required. Native Markdown/admonitions/details
may represent similar roles, and exercise feedback structures may differ when
the target platform or task calls for it.
