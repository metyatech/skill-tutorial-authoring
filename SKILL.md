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

Treat learner-visible material as instructional content regardless of file type
or path. Prompts, labels, code context, feedback, explanations, and visible
state text embedded in JSON/YAML/TypeScript fixtures, Bundle source, test
fixtures, or generated source receive the same authoring review as prose in a
tutorial document.

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

Use research provenance separately from enforcement severity:

| Code | Meaning |
|---|---|
| **R — multiple-research-supported** | Multiple independent studies or research syntheses support the direction within relevant boundary conditions |
| **S — multi-study research synthesis** | A conclusion follows from an explicit inference chain using only research-supported premises from multiple studies/syntheses |
| **L — local decision** | Normative purpose, writing convention, product decision, or platform contract; not a scientific finding |
| **U — unresolved** | The available research does not determine the decision |

The educational purpose above is normative and therefore local, not empirical.
A rule may be promoted to **R** or **S** only when its evidence and boundary
conditions are traceable in
[references/research-foundations.md](references/research-foundations.md).
For **S**, record the inference chain; do not combine one research result with
unaudited design intuition. **U** items do not become pedagogical rules merely
to fill a design gap: gather more evidence, test the alternatives, or keep the
choice explicitly local/experimental.

Evidence strength and enforcement severity are separate axes. A strict platform
contract can be **L**; an **R** principle can remain advisory when correct
application requires semantic judgement.

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

For any response-bearing activity, the visible pre-attempt state must make clear
what the learner is responding about, what action or judgment is required, and
the expected response form. Do not rely on a shared renderer to invent
domain-specific task meaning that authoring omitted; neutral accessibility or
platform labels are acceptable only when they cannot misstate the task.

## Segmenting and split attention

Use **meaningful learner-controlled chunks**, not a mechanical “one screen =
one segment” law.

Screen/state transitions are useful boundary candidates in GUI tutorials, but a
semantic sub-goal is the stronger criterion. Coding or conceptual tasks may need
segmentation without any screen transition.

Segment at meaningful semantic or causal boundaries, not by screen count. If
simultaneous changes would obscure which change caused which result, separate
them so each contribution can be observed. Preserve an intentional “no visible
change yet” state when it distinguishes roles or clarifies the mental model;
for example, adding an HTML class before CSS selects that class. Do not split
mechanically when the resulting integration cost would rise.

Meaningful segments may be progressively disclosed. When later understanding
requires comparison or integration with earlier material, keep that material
available or easy to reopen. A novice guided flow may guide forward progression
while keeping covered content reviewable; this does not imply that unrestricted
navigation is always beneficial. When reviewing earlier steps, preserve learner
state and answers where practical; make an intended reset clear. After a
learner commits a response, preserve it in place or in an immediately comparable
representation when comparison matters. Do not add an identical canonical
answer immediately beside an already-visible correct response unless the second
representation adds a distinct explanatory, normalization, comparison, or
accessibility role. Cumulative
presentation is a promising, evidence-aligned candidate, not a proven universal
or uniquely optimal UI. In-page cumulative review supports offloading, but does
not replace later spaced retrieval or transfer practice.
Exact tabs, accordions, collapsing, and layout remain local/experimental
choices. A compact post-completion reference may help quick re-entry when
learners need it; it is not required on every page.

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
- When pre-training is needed, teach the name and the relevant
  characteristics/relations the learner must understand before a later task can
  depend on them; a list of names alone does not prepare that understanding.
- Use the length needed for clarity. Six or more sentences may trigger review
  for mixed concepts or reference detail; this is neither a hard limit nor a
  research threshold, and shorter blocks are not inherently better.

If the learner already knows the concept, a collapsible/reference form or no
Concept at all may be better.

## Learner-facing orientation

Use a page introduction, prerequisite callout, objective summary, Section
goal, preview, or sequence announcement when it gives concrete help with the
current activity, structure, or decision at that point. In cold-read review,
consider reworking an item that only repeats its heading or adjacent prose, a
guaranteed course sequence, a canonical Unit objective, or information the
learner cannot yet use. This **L review convention** does not reject learning
objectives or advance organizers; they can orient attention or expose structure
when useful.
See [references/research-foundations.md](references/research-foundations.md).

An unfamiliar term may appear in an orientation or heading before explanation.
If the learner needs its meaning to understand or act, explain the name and
relevant characteristics or relations before depending on that understanding;
do not call a name-only preview pre-training. A prerequisite callout is useful
when it enables actionable preparation, re-entry, or recovery. In a
guaranteed linear progression, omit it when it adds no such value; prior
knowledge matters without requiring prerequisite UI on every page.

For Course Docs, use **learner-action consistency** as an **S research synthesis**: a learner-facing heading, its immediate explanation, the task
statement, and relevant UI cues should communicate the action required at the
same stage. Review a mismatch as a learner-facing defect when it leaves the
learner unsure whether to look, write, choose, fix, try, check, answer, or
create. Natural paraphrases are fine when they mean the same action; do not
require identical words. Multiple actions are fine when their order is explicit
and each stage is clear. This synthesis combines heading/signaling, coherence, and consistent task-action mapping evidence;
it is not a directly tested rule about particular verb pairs. See
[`references/research-foundations.md`](references/research-foundations.md).

Separately review **sequence / discourse continuity** across adjacent
material: does the learner's current state make it clear why the next topic,
operation, or concept appears now? This is broader than checking whether a
heading and its activity ask for the same action. It is especially useful for
novice-oriented initial instruction. A concise bridge may connect a learner
goal, an observed result, a limitation of the current method, a need for the
next concept or operation, or an explicit transition. Do not make learners
infer a logical bridge the material can state briefly. Cold-read questions
include:

- Would a learner who has just read the preceding material ask “why this now?”
- Does a new concept, tool, or operation appear after its need becomes clear?
- Does a heading reveal a conclusion that is ahead of the learner's current
  state?
- Does the purpose or cause connecting the previous result to the next
  explanation or operation read naturally?

Apply this as an **S research synthesis**, not as
a requirement to add transitions between every paragraph or maximize
coherence for every audience. Preserve intentional inference in retrieval
and problem-solving activities; do not make high coherence a universal rule
for learners with substantial prior knowledge.

For novice initial instruction, a sentence should normally be interpretable
from information introduced up to that point; do not make future content
necessary to understand an earlier sentence. When it fits the lesson's causal
structure, prefer current/known state → need/problem → new concept → use. This
sequence is a local heuristic, not a universally optimal order. Stable names or
identifiers (for example, `index.html`, `style.css`, or the browser result) are
an **L usability/accessibility convention** and more reliable than
viewport-dependent locations as the sole reference when a responsive layout
can move the target. Prefer direct task wording over
authoring/meta labels when the learner's action can be stated plainly.

Learner-facing prompts should make clear, at the point of asking, what object
or content is in question, what judgment/action is required, and what response
form is expected. Do not leave a referent or baseline for learners to infer
unless it is already unambiguous. Selection options should complete or answer
the stem naturally; avoid making Japanese wording a separate decoding task or
presupposing the answer's target category. Preserve intended retrieval or
generation before the first attempt. For Course Docs, exact Japanese-copy checks
are a local quality synthesis, not a universal research law. Prefer showing a
sentence-completion response as the complete semantic sentence when it is
returned for comparison; this is a bounded local convention, not a directly
tested universal rule.

Keep an explanation needed to understand the main instructional path, a later
operation, or a QuickCheck on that path; do not rely only on a Hint, collapsed
content, or optional callout for an essential principle. When mutually dependent
operations, results, code, and explanations must be integrated, keep them close
enough to avoid unnecessary search or split attention. Do not infer a fixed
instructional ordering from example-based learning, contiguity, or coherence
research; select the Event pattern and activity sequence for the actual goal and
learner state.

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

Useful verification is not UI-state narration. If a response is objectively or
checkably scorable and verification resolves learner uncertainty, retain that
performance feedback even when the result is also visible; do not remove it as
“redundant narration”. Verification alone is not sufficient when corrective or
explanatory information would help: connect feedback to the actual result,
correct information, a causal explanation, or a progressively useful hint as
appropriate. Correctness-only feedback should not end the loop when elaboration
would help.

Recovery is error-support, not objective Evidence. Active/generative activity
is not required on every job aid or initial-performance-only page.

Immediate success is evidence of **initial performance**, not durable learning
or transfer. Important knowledge should recur later through retrieval and
distributed practice when curriculum scope permits. Do not claim mastery from
one immediate success.

## Pre-attempt conditions for retrieval and generation activities

When a task is intentionally designed to elicit unaided retrieval or learner
generation (a QuickCheck testing recall, or a task requiring the learner to produce or generate the target response), learner-visible prompt material and
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

Prediction/prequestion activities should ask about the concrete upcoming
relation or outcome. Evidence supports benefits for prequestioned content; do
not generalize those benefits to unrelated, unprequestioned content. A study of
novices predicting code output before explanation supports this option for
suitable initial programming instruction, not a mandatory pattern everywhere.
Present the object/code clearly and ask for a concrete result. Preserve the
pre-attempt state so the target answer is not leaked. After the attempt, give
concrete, task-focused feedback about the actual outcome or relation, with
causal or elaborated feedback rather than only a correctness judgment. For
exploratory prediction, supportive comparison wording may be preferable to
punitive wrong-labelling; exact wording, colour, and icon choices are local
decisions, not research-derived requirements.
When self-explanation is useful, scaffold the prompt to identify the relation,
error, or concept to explain; a generic “explain why” prompt is not
automatically better. Non-empty self-explanation text does not establish
correctness, and never fake semantic correctness for ungraded free text. If a
full explanation would leak a planned self-explanation or generation target,
stage feedback as verification plus the concrete observed result, then learner
generation/self-explanation, then the canonical causal or elaborated
explanation. If a reflection is not semantically graded, do not create a fake
mandatory gate; where appropriate, allow “I don't know” or let the learner
reveal the explanation or answer through an explicit route. Where useful, show
the learner's complete generated statement beside the canonical explanation.
Use self-explanation selectively at conceptual transitions, not after every
action.

Remove status narration such as “recorded”, “added”, or “result shown below”
when it adds no learning, action, recovery, orientation, or accessibility value.
Do not repeat the exact same visible result sentence when the second instance
has no distinct role. Do not mechanically treat a visual result plus concise
text mapping or accessibility equivalent as gratuitous duplication. Feedback
findings from Shute (2008) and Van der Kleij, Feskens, and Eggen (2015) are
R-level guidance within their stated boundary conditions; the staged sequence
is an S Course Docs synthesis; exact wording, tone, colour, and icon styling
are L local decisions.

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

Make important task-relevant information visually distinctive, while limiting
competing emphasis so the signal remains selective. Use grouping cues such as
proximity, common region, alignment, or connectivity when they communicate real
semantic structure. Keep the same task-action mapping and cue consistent when
the meaning/operation is the same. These are research-supported directions, not
a license to invent exact colours, border widths, radii, spacing, or component
families and call them research findings.

Remove decoration or emotional stimulation that is irrelevant to the learning
goal. Deliberate affective design may support motivation or attention when it
remains aligned with the goal and does not create competing processing. A
sidebar, visual, audio, or motion is appropriate when it has a real task,
warning, reference, accessibility, explanation, or feedback role.

Do not enforce arbitrary emphasis counts as scientific laws. If a platform lint
flags unusually dense bolding, treat it as a review prompt for competing visual
signals.

When learners must integrate code, a UI, diagram, or rendered output, make their
semantic relationship explicit and use proximity, a common region, or selective
mapping cues where useful. Do not assume novices will infer that a nearby
preview results from a particular HTML/CSS state. Auxiliary notation must not
create a new decoding task: explain labels directly instead of relying on
unexplained symbols such as `A + B → C`. Exact left/right or stacked layouts
remain local choices; research does not establish one arrangement as optimal.
Name rendered panels in learner language (for example, “browser result”) before
relying on that concept, and prefer stable object names over layout positions.

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

Use the **S — visible-prose value test**: if a learner-facing sentence does not
materially improve understanding, a decision, the next action, error
prevention/recovery, state interpretation, reference value, or accessibility,
consider removing or reworking it. UI narration that only repeats an obvious
interaction/result is usually unnecessary. Keep objectively scorable verification
that resolves learner uncertainty, useful performance feedback, causal
explanations, misconception prevention, task directions, useful
status/accessibility messages, and elaboration that improves clarity. This is
not “shorter is always better”: clarity and useful elaboration can help, while
reducing complexity alone has not reliably improved STEM text learning. Visible prose and
assistive-technology status messages serve different purposes. Accessibility-
equivalent content is not gratuitous redundancy. See the bounded synthesis in
[`references/research-foundations.md`](references/research-foundations.md).

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
- When a state-changing action matters to understanding, identify the changed
  source, target, or result without requiring comparison from memory. Animation
  alone is not the cue; retain a changed value/line marker, result text, or
  equivalent until the learner can inspect it. Motion may support continuity,
  but is supplemental. Respect reduced-motion preferences and preserve text/UI
  contrast during transitions. Do not narrate every change when direct visual
  signaling already makes it clear and prose adds no learning value.
- In sequential dynamic tutorials, newly revealed instruction should normally
  appear at or after its triggering action in meaningful reading/focus order,
  instead of silently changing earlier prose and requiring a backward search.
  Keep semantic, visual, DOM/reading, and keyboard focus order aligned when
  order affects meaning. Predictable, normally top-to-bottom reading flow is a
  local default for this tutorial context, not a universal rule for all
  layouts or languages. A major step change should be understandable near the
  learner's current position; a remote progress indicator may supplement that
  cue but is not a sufficient primary signal by itself.
- For an interactive single-line response with one primary submit/confirm
  action, prefer native form semantics so Enter and the visible submit control
  invoke the same validation and state transition where applicable. Do not
  apply this to multiline inputs or controls whose standard keyboard operation
  differs. Avoid custom Enter
  handlers that submit during IME composition unless composition is explicitly
  handled.

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
