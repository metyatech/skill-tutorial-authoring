---
name: tutorial-authoring
description: >-
  Author, revise, reorganize, or review step-by-step tutorials for
  beginner-to-intermediate learners. Use when writing or auditing tutorials,
  hands-on guides, walkthroughs, procedural lessons, course content, or
  マルチメディア学習 materials. Choose representations by task, reduce avoidable
  cognitive overhead, align practice and feedback to goals, adapt assistance
  to prior knowledge, and preserve accessibility.
---

# Tutorial authoring

Use this skill for learner-facing material where a reader follows instructions
to build, configure, understand, or practice something.

This file is the **execution core**. Load detailed references only when the task
needs them:

- Research rationale, evidence boundaries, and citations:
  [references/research-foundations.md](references/research-foundations.md)
- Course Docs MDX contracts and mechanised lint:
  [references/course-docs-platform.md](references/course-docs-platform.md)
- Accessibility details and text-alternative patterns:
  [references/accessibility.md](references/accessibility.md)
- Reviewer checklist: [REVIEW-CHECKLIST.md](REVIEW-CHECKLIST.md)

## Scope

Default target: **beginner-to-intermediate learners**.

Instructional assistance can show expertise reversal: learners with lower
relevant prior knowledge often benefit from more guidance, while learners with
higher prior knowledge can be hindered by redundant assistance. Scale each form
of guidance to the target learner and the evidence for that tactic; do not
assume every multimedia principle reverses in exactly the same way.

Keep author-facing audience labels in authoring context or metadata. Do not leak
phrases such as 「初学者向け」 into learner-facing prose unless the learner
genuinely needs that information.

## Rule provenance

Do not present every concrete rule as a scientific finding. Classify rules as:

| Class | Meaning |
|---|---|
| **Evidence-backed principle** | Direction supported by learning-science evidence, applied within stated boundary conditions |
| **Quality convention** | Deliberate local writing standard for consistency or usability |
| **Platform contract** | Requirement imposed by the rendering/component system |
| **Context-dependent heuristic** | Review prompt whose usefulness depends on task, medium, or learner |

Evidence strength and enforcement severity are separate axes. A platform
contract may be strict without being a scientific finding; a strong research
principle may remain advisory when correct application requires semantic
judgement.

## Authoring procedure

When creating or reviewing a tutorial, follow this order.

1. Identify the **target learner**, relevant prior knowledge, and concrete task
   outcome.
2. Organise the material around **learner goals**, not software menus or feature
   lists.
3. For each learner action, choose the **primary representation** that makes the
   operation easiest to understand and execute.
4. Introduce concepts **just before first meaningful use**, not in a long
   front-loaded theory section.
5. Add only the guidance, signaling, examples, and recovery support that the
   current learner needs.
6. Close substantive learning goals with a **matching form of evidence**.
7. Check accessibility, coherence, and representation redundancy.
8. Perform a literal **cold read** from top to bottom: every term, value, or
   metaphor must be understandable when first encountered.

## Current cognitive-load model

Use the current CLT framing rather than the older three-additive-load shorthand.

- **Intrinsic load** depends on element interactivity and learner expertise.
  Manage it through sequencing, pre-training when needed, worked examples, and
  appropriate segmentation.
- **Extraneous load** comes from avoidable presentation or instructional
  overhead. Reduce unnecessary search, split attention, irrelevant detail,
  confusing navigation, and role-less duplication.
- **Germane processing** is not a third independent load to maximise. Create
  room for useful retrieval, self-explanation, practice, and feedback after
  avoidable extraneous demands are controlled.

When tactics conflict: first reduce avoidable extraneous processing, then manage
task complexity for the learner, then add learning-relevant activity that still
fits available capacity.

See [references/research-foundations.md](references/research-foundations.md)
for sources and limits.

## Primary representation

Choose the representation that communicates the learner's operation with the
least avoidable integration work. Images are an option, not a default.

| Task | Typical primary representation |
|---|---|
| Spatial UI path, layout, or visual relationship | Annotated visual |
| Code authoring or code change | Code / CodePreview |
| Short non-spatial command or setting | Text |
| Structural relationship or state flow | Diagram |
| Motion-dependent continuous operation | Video/GIF when supported |

Secondary representations should add **complementary** information: exact typed
values, hover-vs-click distinctions, user-specific paths, labels that map prose
to a visual, or semantics that shapes alone cannot establish.

Do not duplicate the same complete procedure across two equally prominent
paths. Short identity cues, labels, numbers, and positional anchors may appear
in both when they reduce search or mapping cost.

**Accessibility-equivalent content is not gratuitous redundancy.** If a visual
carries essential information, provide an equivalent textual route. Prefer
presentation that keeps the equivalent available to assistive technology or on
demand without forcing every learner to process two complete parallel
procedures.

## Action unit

Treat an Action as **one coherent learner action episode**: a locally unified
operation or short sequence toward one immediate sub-goal. It need not mean one
mouse click.

For example, a visual-primary Action may legitimately show a short navigation
sequence such as click → open menu → hover submenu → choose item when the whole
sequence is one coherent episode.

Split an Action when doing so creates a meaningful state/sub-goal boundary,
reduces integration cost, or makes recovery/verification clearer. Do not split
mechanically per field, click, or numbered callout.

Action prose must remain sufficient to act without guessing. Do not “fix”
redundancy by reducing instructions to bare verbs such as 「クリックします」.

## Segmenting and split attention

Use **meaningful learner-controlled chunks**, not a mechanical “one screen =
one segment” law.

Screen/state transitions are useful boundary candidates in GUI tutorials, but a
semantic sub-goal is the stronger criterion. Coding or conceptual tasks may need
segmentation without any screen transition.

Split attention occurs when the learner must mentally integrate separated
sources. Physical distance is a common cause, not the definition. Keep
corresponding visuals, labels, values, and explanatory text close enough to
integrate without unnecessary search.

## Concepts and pre-training

A Concept introduces one need-now term or idea.

- Place it near the first meaningful use: Action, Section, Verify, QuickCheck,
  or Exercise as appropriate.
- Explain **what it is** and **why it matters now**.
- Do not introduce distant-future material.
- Roughly 2–5 sentences or one short table is a useful heuristic, not a hard
  scientific threshold. At 6+ sentences, review whether the block contains
  multiple concepts or reference detail.

If the learner already knows the concept, a collapsible/reference form or no
Concept at all may be better.

## Activation

Where a useful prior-knowledge anchor exists, activate it through recall,
comparison, an earlier lesson/task, or a sound analogy.

Do not invent an analogy merely to satisfy a checklist. Activation recalls
existing knowledge; pre-training teaches knowledge that is not yet established.

## Scaffolding and progressive independence

For low or unestablished relevant prior knowledge, default to enough worked or
guided support before substantial independent construction.

Fade, retain, or restore support according to prior knowledge and learner
performance. Do **not** use fixed thresholds such as “second occurrence =
guided” and “third occurrence = independent”.

Useful progression when appropriate:

- **Worked example:** complete model with necessary guidance.
- **Guided variation/completion:** learner makes selected decisions.
- **Independent application:** learner plans or transfers without procedural
  instructions.

Not every page needs all three phases. Learners with established prior knowledge
may appropriately start later in the progression.

## Practice, retrieval, feedback, and aligned closure

A substantive learning goal should have evidence appropriate to that goal.

| Goal/evidence need | Suitable closure |
|---|---|
| Observable behavior or state | Verify |
| Retrieval / understanding | QuickCheck |
| Several observable conditions forming a milestone | Checkpoint |
| Transfer / application to a new condition | Exercise |

This mapping is a **quality convention for choosing useful closure**, not a claim
that every closure is a generative-learning activity.

Generative activity specifically asks learners to select, organise, integrate,
retrieve, explain, predict, or apply information. QuickChecks,
self-explanation, and suitably designed Exercises can serve this role. A passive
Verify may be valuable feedback without being generative activity.

Recovery is error-support, not learning-goal closure.

Immediate closure is evidence of **current performance**, not durable mastery.
Important knowledge should be revisited later through retrieval/distributed
practice when curriculum scope permits. Do not claim permanent mastery from one
immediate success.

## Recovery and error support

Minimalist error support covers prevention, detection, diagnosis, and recovery.
The `<Recovery>`-style component itself is mainly the **reactive** part.

- Put a preventive warning before an action when a common mistake can be
  avoided cheaply.
- Put Recovery after a plausible failure point.
- Structure Recovery as **symptom → likely cause → concrete fix**.
- Do not use catch-all “try again” advice at the end of a section.

## Signaling and coherence

Use signaling only to help the learner find, map, sequence, or interpret
goal-relevant information.

Good signals include a concise goal, visual callouts, an important UI label, an
exact value to type, or a key gesture. Decorative emphasis is not signaling.

Avoid irrelevant images, sidebars, audio, animations, emoji, or digressions. A
sidebar or visual is fine when it has a real task, warning, reference,
accessibility, or feedback role.

Do not enforce arbitrary emphasis counts as scientific laws. If a platform lint
flags unusually dense bolding, treat it as a review prompt for competing visual
signals.

## Learner-facing prose

Use natural, direct, active language. Japanese zero-subject sentences are fine;
explicit 「あなた」 is not required.

Keep authoring rationale and audience classification out of learner-facing prose
when they do not help the task. Rewrite 「受講者は〜」「学習者は〜」
「初学者向け」 as task-facing prose. Do not ban 「ユーザー」 when it refers
to a real product/domain end user.

## Accessibility essentials

Apply these rules to **all informative non-text content**, not only screenshots
inside specific components.

- Provide a text alternative that serves the same purpose or conveys the
  essential information.
- For complex annotated visuals, use a concise short alternative plus a
  learner-visible or otherwise associated detailed description.
- Do not rely on colour alone for meaning.
- Normal text/images of text require 4.5:1 contrast; large text may use 3:1.
  Meaningful non-text UI/graphical indicators use the applicable 3:1
  non-text-contrast requirement.
- Prefer real text to images of text when equivalent presentation is practical.
- Interactive examples must be keyboard operable.

WCAG 2.2 AA is the default accessibility target for this skill. U.S. Section
508 E205 is additionally relevant when the material falls within U.S. federal
ICT scope; it is not a universal legal requirement for every tutorial.

Load [references/accessibility.md](references/accessibility.md) when authoring or
reviewing informative images, diagrams, charts, annotated screenshots, or
interactive examples.

## Course Docs environments

When the target site uses `@metyatech/course-docs-platform`, load
[references/course-docs-platform.md](references/course-docs-platform.md).

That reference contains local MDX contracts such as:

- top-level `<Section>` goal requirements;
- QuickCheck/Exercise `problem → Hint+ → Answer` structure;
- `Verify` source notation;
- component placement conventions;
- lint rule IDs and severities.

Do not generalise those platform contracts into universal tutorial-science
claims or force them onto unrelated Markdown/tutorial systems.

## Final review

Before delivering or approving a tutorial:

- verify the page is organised by learner goals;
- cold-read every heading, term, value, metaphor, and code comment in rendered
  order;
- confirm representation choice and accessibility equivalents;
- confirm Concepts occur near meaningful first use;
- confirm guidance matches prior knowledge;
- confirm practice/closure tests the stated goal;
- confirm failure support addresses plausible failures;
- remove irrelevant or duplicate processing;
- use [REVIEW-CHECKLIST.md](REVIEW-CHECKLIST.md) for a full audit.

This skill encodes evidence-informed defaults and local quality conventions; it
does not guarantee pedagogically correct output. Observe real learners and
revise when evidence from actual use conflicts with an assumed heuristic.
