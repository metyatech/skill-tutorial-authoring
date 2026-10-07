# Course Docs platform contract

Load this reference only when authoring for a site that uses
`@metyatech/course-docs-platform` or the matching `course-docs` agent rules.

These rules are **local platform contracts and quality conventions**. Do not
present them as universal learning-science requirements and do not force them on
unrelated Markdown/tutorial systems.

Design Unit outcomes, Event experiences, and aligned Evidence before choosing
MDX components. Components express those choices. See the platform's
[Learning System documentation](https://github.com/metyatech/course-docs-site/blob/main/docs/learning-system.md)
for metadata contracts; component names or Section boundaries do not determine
pedagogy.

## Structured learner-facing sources and runtime fallback

Course Docs learner-visible content remains instructional content even when it
is stored outside MDX. Apply learner-facing authoring rules to prompts, labels,
code context, feedback, explanations, and visible state text in JSON/YAML/TS
fixtures, Learning Bundle source, generated source, and test fixtures.

Shared platform/runtime components own mechanics and neutral platform behavior;
they must not invent domain-specific instructional copy from generic response or
evaluator kinds. If a task needs a subject-specific prompt, response label,
causal explanation, or feedback relation, author and validate that meaning
upstream. Missing instructional meaning is not safely repaired by a plausible
runtime fallback.

For response-bearing activities, the pre-attempt state must make clear what the
learner is responding about, the required learner action, and the expected
response form. Structured learner-facing runtimes should also preserve explicit
semantic hierarchy for lesson/page identity, meaningful activity/task headings,
task prompts, response surfaces, and results/feedback rather than deriving
those roles from internal IDs or rendering them all as generic body text.

After commitment, keep the learner response directly comparable when that
comparison supports learning, and avoid an immediately repeated canonical
answer unless the second representation has a distinct instructional or
accessibility role.

For controlled visual comparisons, preserve presentation conditions that affect
the observed result, including preview/container width, viewport, scale, zoom,
and clipping. Do not force side-by-side columns when that layout changes the
baseline or masks the target effect; stack or preserve an equivalent reference
viewport instead.

## Component composition

Course Docs tutorials are composed from local task components. There is no
page-wide tutorial/non-tutorial authoring mode and no mandatory fixed page-wide
flow.

Available components:

| Component | Contract / role |
|---|---|
| `<Prerequisites>` | Page-level requirements before the first Section |
| `<Section>` | Recursive presentation container; `title` required; `goal` optional at all depths |
| `<Action>` | Coherent learner action episode; optional `img` / `alt` |
| `<Verify>` | Observable result evidence; optional expected-result image |
| `<Concept>` | Conceptual support for current/near activity, pre-training, summary, retrieval, or reference |
| `<Reference>` | Collapsible lookup material |
| `<Recovery>` | Reactive diagnosis/recovery support near a failure point |
| `<Checkpoint>` | Optional checklist for a meaningful multi-condition milestone |
| `<QuickCheck>` | Short retrieval/understanding task |
| `<Exercise>` | Applied task for practice or transfer, depending on its design |
| `<Hint>` | Progressive support inside QuickCheck or Exercise |
| `<Answer>` | Final answer/explanation inside QuickCheck or Exercise |
| `<NextSteps>` | Optional concrete follow-up actions, normally at document end |
| `<Instruction>` / `<ProblemSolving>` | Direct-child initial Event stage markers ordered by `pattern` |
| `<Evidence>` | Metadata-only binding to one existing assessment surface |

A single `<Section>` is recursive. Heading depth is injected automatically:
depth 0 → `h2`, depth 1 → `h3`, and so on, capped at `h6`.

## Instructional horizon

Before choosing representation or assistance, identify whether the lesson or
Learning Unit/Event is intended mainly for **initial performance**, **learning (including
retention)**, **transfer**, or a deliberate combination. This is a Course Docs
quality convention rather than an MDX parser requirement.

Do not optimise only first-attempt speed when retention or transfer is an
explicit goal. Representation, fading, QuickChecks, and Exercises should follow
the intended horizon.

## Section goals

Section `goal` is optional at all depths, including Event-bearing Sections.
Use it when learner-facing orientation helps. It is neither the canonical Unit
objective (defined once in course-root `learning-units.yaml`) nor Evidence;
do not duplicate Unit objectives into it.

Non-empty goal text renders verbatim below the heading. Empty/whitespace-only
values render no goal banner. No tense pattern is required or linted.

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

A Concept supports conceptual knowledge needed for current or near learning
activity. Near meaningful first use is a default; intentional pre-training,
summary, retrieval, or reference placement is also valid.

The following-usage-site detector is an advisory approximation, not semantic
validation. Six or more sentences prompts review for mixed concepts/reference
detail; no preferred sentence count, hard limit, or research threshold follows.

## Recovery

Recovery is not learning-goal closure. Place it after a plausible failure point
and write it as **symptom → likely cause → concrete fix**.

Preventive warnings belong before the risky Action; they are distinct from the
reactive Recovery component.

## QuickCheck and Exercise task structure

In Course Docs, both task components have this **platform contract**:

```text
problem content
→ zero or more <Hint> blocks
→ exactly one final <Answer>
```

Hints and Answer must be direct children of the task block. Content after
`<Answer>`, a Hint after Answer, nested task blocks, or the removed legacy
Solution component are invalid.

The contract is `problem → Hint* → Answer`. Problem content and exactly one
non-empty final Answer are required. Hints are optional; when supplied they
must be non-empty and precede Answer, with no later problem content.

This structure is local to Course Docs. A generic tutorial outside this platform
may use a different exercise/feedback structure when pedagogically appropriate.

The first Hint should avoid unnecessarily revealing the answer immediately.
Multiple Hints may become progressively stronger or more explicit. Default to
material already established by this or a guaranteed earlier lesson, but a Hint
may explicitly teach new information. Do not require unfamiliar information as
already known without explaining it.

An Answer must provide feedback that lets learners understand correctness.
For simple, self-explanatory tasks, a concise Answer is appropriate when
additional explanation adds no learning value. Explain the reasoning or address
a likely misconception when it helps the learner; do not invent a misconception
merely to satisfy the template.

## Unit/Event/Evidence alignment

Design evidence for Unit objectives at useful points in Event/course
progression. Section-local closure is not required. Assessment surfaces include:

- `<Verify>` — observable state/behavior;
- `<QuickCheck>` — retrieval/understanding;
- `<Checkpoint>` — meaningful multi-condition milestone;
- `<Exercise>` — applied practice or transfer, depending on task conditions.

An Exercise is a task format, not automatic transfer evidence. To support a
transfer claim, change conditions meaningfully and require learners to select or
adapt the learned principle. Align evidence to the targeted Unit outcome.

`<Recovery>` provides error support rather than objective Evidence.

Do not add assessment components mechanically. Bind an existing surface with
`<Evidence>` when explicit Unit/Event mapping is needed. A goal banner does not
establish evidence.

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

## Visual/reference acceptance

When a Course Docs learner-facing runtime has an explicit reference experience
or visual acceptance contract, passing unit/E2E/accessibility tests is necessary
but not sufficient for final acceptance. Inspect the specified rendered states
in a real browser against the reference. When rendered size, spacing, clipping,
or responsive behavior carries instructional meaning, inspect the actual
rendered geometry/environment rather than only DOM structure or labels. Until the designated visual reviewer
accepts them, the work remains waiting for visual acceptance rather than final
PASS.

This is a local Course Docs QA contract, not a general learning-science claim.

## Mechanised tutorial lint

Severity is based on artefact impact and machine-detection confidence, not
research strength.

| Rule ID | Severity | Intent |
|---|---|---|
| `tutorial/action-single-image` | note | Multiple images in one Action; review integration |
| `tutorial/section-no-hrule` | warn | Horizontal rule inside a Section |
| `tutorial/verify-no-duplicate-arrow` | warn | Verify source starts with `→` |
| `tutorial/verify-shot-action-role` | warn | Verify shot manifest contains action-role annotations |
| `tutorial/reference-image-only` | note | Image-only Reference |
| `tutorial/action-bold-overuse` | note | Six or more bold spans in one Action |
| `tutorial/third-person-reader` | note | Learner-audience meta-prose heuristic |
| `tutorial/page-opens-with-doc-description` | note | Document-description opener heuristic |
| `tutorial/verify-internal-mechanics` | note | Verify appears to describe internal mechanics |
| `tutorial/concept-length` | note | Six or more Concept sentences |
| `tutorial/concept-placement` | note | Review meaningful-use, pre-training, summary, retrieval, or reference placement |
| `tutorial/decorative-emoji` | note | Review goal-aligned signaling/affect versus competing ornament |
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
