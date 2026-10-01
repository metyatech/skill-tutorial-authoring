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
- Motion-based instruction and accessible video:
  [references/video.md](references/video.md)
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

## Educational purpose

Adopt this **normative purpose**: learners enjoy learning with a positive
outlook while increasing what they can actually do, and use what they learn to
think, create, and continue learning for themselves.

This is the educational system's value judgment, not a unique purpose proved by
research. Learning science informs the means, side effects, and boundary
conditions for pursuing it. Enjoyment does not mean constant ease; rigor does
not require unnecessary frustration. Preserve meaningful retrieval, decisions,
problem solving, and productive struggle while reducing accidental difficulty.

## Rule provenance

Do not present every concrete rule as a scientific finding. Classify rules as:

| Class | Meaning |
|---|---|
| **Normative purpose** (`normative-purpose`) | Adopted educational value judgment, not an empirical finding |
| **Evidence-backed principle** | Direction supported by learning-science evidence, applied within stated boundary conditions |
| **Quality convention** | Deliberate local writing standard for consistency or usability |
| **Platform contract** | Requirement imposed by the rendering/component system |
| **Context-dependent heuristic** | Review prompt whose usefulness depends on task, medium, or learner |

The remaining class identifiers are `evidence-backed-principle`,
`quality-convention`, `platform-contract`, and `context-dependent-heuristic`.

Evidence strength and enforcement severity are separate axes. A platform
contract may be strict without being a scientific finding; a strong research
principle may remain advisory when correct application requires semantic
judgement.

## Authoring procedure

When creating or reviewing a tutorial, follow this order.

1. **Purpose / intended outcome:** decide what worthwhile capability the learner
   should gain in service of the educational purpose.
2. **Learner state:** identify relevant prior knowledge, prior instruction, and
   intended horizon: initial performance, retention, transfer, or a combination.
3. **Learning Unit + aligned Evidence:** define what is learned and what
   observable evidence would demonstrate the intended outcome.
4. **Learning Event design:** choose the learning experience for this occasion,
   including a suitable Pattern/Strategy and meaningful activities.
5. **Appropriate assistance:** supply explanations, models, feedback, and
   recovery support matched to the learner, performance, and goal.
6. **Engagement / meaningful challenge:** support willingness to learn and
   achievable progress without making ease the measure of quality.
7. **Active learner processing:** design relevant retrieval, explanation,
   prediction, comparison, decisions, application, debugging, or creation.
8. **Course progression:** plan later practice, retrieval, and changed-condition
   transfer when the curriculum owns that horizon.
9. **Presentation / accessibility / cold-read:** choose representations and
   components, then check access, clarity, and accidental difficulty.

`Need / Context → Name + meaning → Use` is a context-dependent heuristic for
some explanations, not a fixed required or default authoring sequence.

## Learning system and tutorial pages

Design from purpose → Unit/intended outcome → Event/learner experience →
Evidence → progression over time. Units are **WHAT**, Events **HOW / NOW**,
Evidence **EVIDENCE**, and progression **OVER TIME**. Page / Section are
presentation/distribution choices below that model. Components express the
chosen experience; their props do not determine pedagogy. A Section does not
require local closure, a Concept, or a Hint merely because it exists.

For curriculum-level design, distinguish the stable objective from each
occasion on which learners work toward it:

- A **Learning Unit** is a stable learning objective or capability: what is to
  be learned. Units may form a hierarchy from broader objectives to leaf
  objectives. A page is not a Learning Unit.
- A **Learning Event** is one occurrence of learning or practice targeting one
  or more Learning Units: how learners engage this time. The same Unit may
  recur in multiple Events, with different activities and evidence.
- **Course progression** is the ordered recurrence of Events over time. Plan
  later retrieval and distributed practice, cumulative or mixed practice,
  interleaving where the content and goal support it, and transfer. These are
  evidence-informed design aims, not a locally synthesized fixed sequence
  claimed as a research-proven optimum.
- **Evidence / Assessment** is observable evidence aligned with a Learning
  Unit's objective. An **Exercise** is a task or container format; it may be
  ordinary practice or transfer. Transfer evidence requires meaningfully
  changed conditions and selection or adaptation of the learned principle.
- A **Page** is a presentation and distribution unit. It may present part of an
  Event or material for several Events; one Event may span pages or other
  formats. A Page does not define the objective or the occurrence. Teaching
  can normally follow the learner-visible material in Event order; do not
  require a duplicate teacher lesson plan.

For initial-learning order, use **I-PS** (instruction-first, then problem
solving) and **PS-I** (problem-solving-first, then instruction). This Pattern
describes the order of instruction and problem solving, not a whole-page
template. A larger Strategy may be used inside a compatible Pattern when it
helps enact the Event. **Productive Failure** is a specific high-fidelity
subset/variant of PS-I, not a synonym for all PS-I; a deliberately designed
problem-before-instruction Event is not unguided struggle. **Inquiry-Based
Learning** is a broader Strategy and does not mean unguided discovery. Keep
smaller techniques such as worked examples, self-explanation, and retrieval
practice distinct where useful; do not impose a taxonomy that makes authoring
heavier without improving execution.

## Instructional horizon

Do not optimise every tutorial for the same outcome.

- **Initial performance / job aid:** prioritise fast, accurate execution while
  the instructions are available. Detailed task-matching directions or a
  visual-primary path can be appropriate.
- **Learning (including retention):** include opportunities to retrieve,
  explain, or reproduce the procedure over time rather than measuring only
  first-attempt speed.
- **Transfer:** include principles, variation, or application under changed
  conditions so success is not limited to copying one worked path.

A tutorial may serve more than one horizon. When goals compete, do not maximise
first-attempt completion speed at the expense of an explicitly required
retention or transfer outcome. Fading and mixed instruction can support both.

## Cognitive-load framing used by this skill

Use Sweller, van Merriënboer & Paas (2019) as the operational baseline rather
than the older three-additive-load shorthand. Also account for the 2025 Kalyuga
& Plass **goal-driven revision proposal**: whether a demand is useful or
extraneous can depend on the instructional goal, learner prior knowledge,
motivation, and affect. Treat that proposal as an important extension, not
settled consensus.

- **Intrinsic load** depends on interacting task elements relative to learner
  expertise and the goal being pursued. Manage it through sequencing,
  pre-training when needed, worked examples, and appropriate segmentation.
- **Extraneous load** comes from avoidable processing relative to the current
  instructional goal. Reduce unnecessary search, split attention, irrelevant
  detail, confusing navigation, and role-less duplication.
- **Germane processing** is not a third independent load to maximise. Create
  room for useful retrieval, self-explanation, practice, and feedback after
  avoidable demands are controlled.

Reduce avoidable processing relative to the goal so learners can use capacity
for learning-relevant thinking. Retrieval, self-explanation, problem solving,
choosing, debugging, adapting, and transfer may be productive difficulty.
Do not remove them merely to lower reported effort.

When tactics conflict: identify the instructional goal first, reduce avoidable
processing relative to that goal, manage task complexity for the learner, then
add learning-relevant activity that still fits available capacity. Consider
motivation and affect when they materially change the learner's ability or
willingness to engage with the task.

See [references/research-foundations.md](references/research-foundations.md)
for sources and limits.

## Primary representation

Choose the representation that communicates the learner's operation with the
least avoidable integration work **while supporting the intended instructional
horizon**. Images are an option, not a default.

| Task | Typical primary representation |
|---|---|
| Spatial UI path, layout, or visual relationship | Annotated visual |
| Code authoring or code change | Code / CodePreview |
| Short non-spatial command or setting | Text |
| Structural relationship or state flow | Diagram |
| Motion, timing, or continuous change is instructional | Video/animation when supported; see [references/video.md](references/video.md) |

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

The **Action as a whole** must let the learner act without guessing. For a
visual-primary Action, visible prose may contain only complementary information
instead of restating the complete visual path. Preserve a complete accessible
text-equivalent route for essential visual instructions, but do not force that
route to compete visually with the primary path when the platform can expose it
programmatically or on demand.

Do not “fix” redundancy by leaving an underspecified instruction such as
「クリックします」 when neither the primary representation nor its accessible
equivalent identifies the target and operation clearly.

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

A Concept supports conceptual knowledge needed to understand or perform a
current or near learning activity.

- Near-first-use is a default, not an exclusive placement contract. Earlier
  pre-training may prepare learners for a complex activity; summary, retrieval,
  or reference placement may also be semantically appropriate.
- Explain what it is and why it matters for the activity; avoid unrelated
  distant-future material.
- Use the length needed for clarity. Six or more sentences may trigger review
  for mixed concepts or reference detail; this is neither a hard limit nor a
  research threshold, and shorter blocks are not inherently better.

If the learner already knows the concept, a collapsible/reference form or no
Concept at all may be better.

## Activation

Where a useful prior-knowledge anchor exists, activate it through recall,
comparison, an earlier lesson/task, or a sound analogy.

Do not invent an analogy merely to satisfy a checklist. Activation recalls
existing knowledge; pre-training teaches knowledge that is not yet established.

## Scaffolding and progressive independence

Aim for **appropriate assistance**, not guidance minimization. Increasing
independence is a capability outcome, not a requirement to withhold useful help.

For low or unknown relevant prior knowledge, default to enough worked or guided
support before substantial independent construction. This default does not
prohibit a high-fidelity, supported Productive Failure PS-I design where it
fits: deliberately designed problem-before-instruction is not unguided
struggle. See the boundaries in
[references/research-foundations.md](references/research-foundations.md).

Fade, retain, or restore support according to prior knowledge and learner
performance. Do **not** use fixed thresholds such as “second occurrence =
guided” and “third occurrence = independent”.

Adjust assistance to available knowledge about the intended learner and observed
performance; individualized adaptive-mastery tracking is future scope, not a
required implementation for this skill.

Useful progression when appropriate:

- **Worked example:** complete model with necessary guidance.
- **Guided variation/completion:** learner makes selected decisions.
- **Independent application:** learner plans or transfers without procedural
  instructions.

Not every page needs all three phases. Learners with established prior knowledge
may appropriately start later in the progression.

## Engagement, enjoyment, and autonomy

Consider authentic relevance, meaningful challenge, visible progress,
competence-supportive feedback, meaningful choice, learner control, and positive
engagement where they support the outcome. These are design options, not a
checklist to include on every page. Do not invent relevance or make choice an
end in itself. Enjoyment ≠ ease; rigor ≠ unnecessary frustration.

Evaluate both learning and experience: pleasant fluency or a feeling of learning
does not by itself demonstrate capability growth, and useful effort may feel
difficult. Use appropriate evidence and learner feedback together.

## Practice, retrieval, feedback, and aligned evidence

A substantive learning goal should have evidence appropriate to that goal and
its intended instructional horizon.

| Goal/evidence need | Possible evidence surface |
|---|---|
| Observable behavior or state | Verify |
| Retrieval / understanding | QuickCheck |
| Several observable conditions forming a milestone | Checkpoint |
| Application or transfer task | Exercise |

This mapping is a **quality convention for choosing evidence surfaces**, not a
Section-local closure contract. Align Evidence to Units and Events at useful
points in progression, rather than adding a check to every Section.

Generative activity specifically asks learners to select, organise, integrate,
retrieve, explain, predict, compare, apply, debug, adapt, or create. QuickChecks,
self-explanation, and suitably designed Exercises can serve this role. A passive
Verify may be valuable feedback without being generative activity.

Recovery is error-support, not objective Evidence. Active/generative activity
is not required on every job aid or initial-performance-only page.

Immediate success is evidence of **initial performance**, not durable learning
or transfer. Important knowledge should recur later through retrieval and
distributed practice when curriculum scope permits. Do not claim mastery from
one immediate success.

## Pre-attempt conditions for retrieval and generation activities

When a task is intentionally designed to elicit unaided retrieval or learner
generation (a QuickCheck testing recall, or a problem-solving task), learner-visible prompt material and
default pre-attempt state should not reveal the target response or decisive
cues that remove the intended retrieval or generation opportunity before the
learner's first attempt.

See [references/research-foundations.md](references/research-foundations.md)
for evidence and boundaries on retrieval practice and generation effect.

If the response is deliberately supplied as worked instruction, guided modeling,
or scaffolded support (worked examples, completion tasks, faded support), that
learner interaction serves guided practice or verification, not unaided retrieval
or generation. This is compatible with retrieval and generation principles; it
reflects a deliberate choice about support form.

This does NOT imply that all exercises must hide answers, that guidance should
always be minimized, or that every learning event must maximize generative
difficulty. Choose task design to fit instructional goal, learner knowledge, and
evidence for the tactic being applied.

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

Remove decoration or emotional stimulation that is irrelevant to the learning
goal. Deliberate affective design may support motivation or attention when it
remains aligned with the goal and does not create competing processing. A
sidebar, visual, audio, or motion is appropriate when it has a real task,
warning, reference, accessibility, explanation, or feedback role.

Do not enforce arbitrary emphasis counts as scientific laws. If a platform lint
flags unusually dense bolding, treat it as a review prompt for competing visual
signals.

## Learner-facing prose

**Clarity > brevity.** Do not shorten away causal relationships, UI/state
correspondence, why an action matters, state transitions, or term meanings that
learners need. A term may appear in a heading or title before definition, but
explain it before requiring understanding of it. Prefer headings that predict
the task, topic, or capability.

Use natural, direct, active language. Japanese zero-subject sentences are fine;
explicit 「あなた」 is not required.

Keep authoring rationale and audience classification out of learner-facing prose
when they do not help the task. Rewrite 「受講者は〜」「学習者は〜」
「初学者向け」 as task-facing prose. Do not ban 「ユーザー」 when it refers
to a real product/domain end user.

## Cold-read: accidental difficulty detector

Read the material in rendered order to detect unexplained prerequisites,
ambiguous instructions, missing state, unnecessary backtracking, undefined
assumptions, terminology gaps, and visual/prose mismatches. Re-entry should be
understandable where the material supports it.

Preserve intended retrieval effort, problem solving, decision making,
productive struggle, and changed-condition transfer. Cold-read review should
remove accidental confusion, not solve the learner's meaningful challenge.

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

Video is within this skill's scope. Use it when motion, timing, or continuous
change is important to understanding or performing the task; keep exact values
and commands available in accessible text. Load
[references/video.md](references/video.md) for learner control, signaling,
segmenting, synchronization, and time-based-media accessibility.

## Course Docs environments

When the target site uses `@metyatech/course-docs-platform`, load
[references/course-docs-platform.md](references/course-docs-platform.md).

That reference contains local MDX contracts such as:

- optional `<Section>` orientation goals at every depth;
- QuickCheck/Exercise `problem → Hint* → Answer` structure;
- `Verify` source notation;
- component placement conventions;
- lint rule IDs and severities.

Do not generalise those platform contracts into universal tutorial-science
claims or force them onto unrelated Markdown/tutorial systems.

## Final review

Before delivering or approving a tutorial:

- verify the intended instructional horizon (initial performance, learning
  including retention, transfer, or a combination) is explicit enough to guide
  design decisions;
- verify the page is organised by learner goals;
- cold-read every heading, term, value, metaphor, and code comment in rendered
  order;
- confirm representation choice and accessibility equivalents;
- confirm Concept placement serves meaningful use or intentional pre-training,
  summary, retrieval, or reference;
- confirm appropriate assistance matches prior knowledge/performance;
- confirm Evidence tests Unit outcomes at useful points in progression;
- confirm engagement supports meaningful challenge without equating enjoyment
  with ease;
- confirm failure support addresses plausible failures;
- remove irrelevant or duplicate processing;
- use [REVIEW-CHECKLIST.md](REVIEW-CHECKLIST.md) for a full audit.

This skill encodes evidence-informed defaults and local quality conventions; it
does not guarantee pedagogically correct output. Observe real learners and
revise when evidence from actual use conflicts with an assumed heuristic.
