# Tutorial self-review checklist

Use this list when auditing a draft tutorial against `SKILL.md`. The checklist
separates generic tutorial-quality judgements from Course Docs-only platform
contracts.

## Purpose / outcome alignment

- [ ] The adopted normative purpose guides capability growth and positive learning; it is not presented as an empirical research finding.
- [ ] Outcomes, learner experience, and evidence are designed before selecting presentation components.
- [ ] A component's existence or prop does not impose a learning activity, fixed ordering, or local ending.

## Learner state / prior knowledge

- [ ] The target learner and relevant prior knowledge are stated or reliably implied.
- [ ] Prior instruction is considered rather than treating every first textual appearance as unfamiliar knowledge.
- [ ] The intended instructional horizon is identified: initial performance, learning (including retention), transfer, or a deliberate combination.
- [ ] First-attempt speed is not treated as the sole quality metric when retention or transfer is an explicit goal.
- [ ] The page is organised around learner goals rather than software features/menu structure.
- [ ] Assistance, signaling, Concept density, and narrative depth match the target learner.
- [ ] Expert or already-trained readers are not forced through redundant novice guidance.

## Learner-facing orientation

- [ ] Each learner-facing orientation item gives concrete value for the
  activity, structure, or decision where it appears.
- [ ] An orientation item is not merely a restatement of its heading or
  adjacent prose, a guaranteed course sequence, or the canonical Unit
  objective.
- [ ] Orientation does not front-load information the learner cannot yet use
  without a clear purpose.
- [ ] For Course Docs, the learner action promised by a heading matches the
  action required by the immediate explanation and activity.
- [ ] For Course Docs, verbs such as “look,” “write,” and “fix” do not ambiguously
  describe different actions at the same stage; natural paraphrases for the
  same action remain acceptable.
- [ ] When multiple actions are intended, their order and stage boundaries are
  explicit.
- [ ] An unfamiliar term is not relied on before its meaning is understood;
  it may still first appear in a heading or preview when understanding is not
  yet required.
- [ ] Pre-training teaches the name plus relevant characteristics or relations
  needed later; a name-only list is not treated as pre-training.
- [ ] A prerequisite callout has actionable value for preparation, re-entry,
  or recovery; prior knowledge does not justify a mechanical callout on every
  page.
- [ ] Each novice initial-instruction sentence is normally interpretable from
  information introduced so far; future material is not required to decode it.
- [ ] Current/known state → need/problem → concept → use is used only when it
  fits the lesson's causal structure, not as a universal required sequence.
- [ ] Responsive-layout targets have stable names/identifiers; spatial terms
  are not their sole locator when the layout can move them.
- [ ] Learner-facing prompts identify the object/content, required
  judgment/action, and expected response form at the point of asking.
- [ ] Vague prompts do not leave a referent or baseline to infer unless it is
  already unambiguous.
- [ ] Selection options complete or answer the stem naturally, without adding
  an accidental Japanese wording-decoding task or presupposing the target
  category in a way that cues the answer.
- [ ] Choice items keep the central idea in the stem; options are natural
  answers to it, and prompt decoding does not add construct-irrelevant
  difficulty.
- [ ] Exact Japanese-copy checks are treated as a local Course Docs quality
  synthesis, not as a universal research law.
- [ ] Task language is direct rather than authoring/meta language where the
  learner's action can be stated plainly.
- [ ] A sentence-completion response shown back for comparison reconstructs the
  complete semantic sentence when useful; this remains a bounded local
  convention, not a universal law.

## Instructional continuity / local coherence

- [ ] In novice-oriented initial instruction, the learner's current state makes
  clear why the next topic, operation, or concept appears now.
- [ ] A new concept, tool, or operation is introduced after its need becomes
  clear, or its purpose is stated before the learner must use it.
- [ ] A heading read ahead of its section does not jump to a conclusion beyond
  the learner's current state.
- [ ] The cause or purpose connecting a previous result to the next explanation
  or operation is easy to follow.
- [ ] Sequence / discourse continuity is reviewed separately from learner-
  action consistency between a heading, explanation, task, and UI cue.
- [ ] An essential principle needed for the main path, a later operation, or a
  QuickCheck is explained on the main path, not only in a Hint, collapsed
  block, or optional callout.
- [ ] Mutually dependent operations, results, code, and explanations are close
  enough to integrate without unnecessary search or split attention.
- [ ] No fixed local instructional sequence is attributed to example-based,
  contiguity, or coherence research unless that sequence itself is supported.
- [ ] The S continuity synthesis does not add transitions mechanically between
  every paragraph, remove intended retrieval or problem-solving inference, or
  demand universally high coherence from knowledgeable learners.
- [ ] Sequential dynamic content appears at or after its triggering action in
  meaningful reading/focus order when this helps avoid backward search; any
  local layout pattern is kept distinct from a WCAG mandate.
- [ ] An action does not silently change upstream prose and require the learner
  to rediscover or reread it; step-transition feedback appears near the current
  position, and top-level progress alone is not the primary change cue.
- [ ] Semantic, visual, programmatic reading, and keyboard focus order remain
  aligned when their order carries meaning; ordinary top-to-bottom flow is a
  local default, not a research law.

## Learning Unit / Event / Evidence

- [ ] Each stable learning objective/capability is treated as a Learning Unit; pages are not treated as Learning Units.
- [ ] A Learning Event is one occurrence of learning/practice targeting one or more Learning Units.
- [ ] Course progression represents the ordered recurrence of Events, with later retrieval/distributed practice, cumulative or mixed practice, appropriate interleaving, and transfer considered where they fit the objectives.
- [ ] A locally designed course sequence is not presented as a single research-proven optimum.
- [ ] Observable evidence/assessment is aligned to the Learning Unit objective.
- [ ] Evidence is placed at useful Event/progression points; Section boundaries do not require local closure.
- [ ] An Exercise is treated as a task/container format that may be ordinary practice or transfer.
- [ ] When Course Docs uses its local `phase="transfer"`, the task satisfies the deliberately strict local criterion of selecting/adapting a learned principle under meaningfully changed conditions; this is not presented as the universal scientific definition of transfer.
- [ ] Pages are treated as presentation/distribution units; teaching can normally follow learner-visible material in Event order without a duplicate teacher lesson plan.
- [ ] Initial-learning order, when relevant, is described as I-PS (instruction-first) or PS-I (problem-solving-first), rather than a global page template.
- [ ] Strategies are optional and compatible with the selected Pattern; Productive Failure is a high-fidelity PS-I subset/variant, and Inquiry-Based Learning is not unguided discovery.
- [ ] Smaller techniques remain conceptually separate where useful without requiring a heavy taxonomy.

## Primary representation / multimedia

- [ ] Each learner action deliberately chooses the most efficient primary representation for both the task and intended instructional horizon: visual, code/CodePreview, text, diagram, or motion media.
- [ ] Images are used when spatial position, appearance, or visual relationships matter; they are not added merely because a step is operational.
- [ ] Code changes use real code/CodePreview rather than screenshots when that is clearer and more accessible.
- [ ] Secondary prose adds complementary information or mapping cues rather than restating the complete procedure.
- [ ] Exact values, user-specific paths, and distinctions such as hover vs click remain available in text or another accessible equivalent.
- [ ] Short identity cues may appear in both representations when they reduce mapping/search cost.
- [ ] Accessibility-equivalent content is retained even when it repeats essential visual information; it is not removed as “redundancy”.
- [ ] A visual-primary Action is executable as a whole without requiring visible prose to restate the complete visual path; a complete accessible equivalent exists separately when needed.
- [ ] Code, UI, diagram, and rendered output have an explicit semantic mapping
  when learners must integrate them; proximity/selective cues are used where
  useful without assuming adjacency alone explains the relationship.
- [ ] Rendered panels are named in learner language before relying on their
  meaning; auxiliary labels/notation do not add an unexplained decoding task.
  Exact left/right or stacked placement is not treated as a proven optimum.

## Action unit and segmenting

- [ ] Each Action is one coherent learner action episode or short locally unified sequence toward an immediate sub-goal.
- [ ] Actions are not split mechanically per click, field, or callout number.
- [ ] A multi-step UI navigation sequence remains one Action when it is cognitively one coherent episode.
- [ ] An Action is split when a meaningful state/sub-goal boundary, recovery point, or verification boundary makes the split useful.
- [ ] Segments are learner-manageable semantic chunks; “one screen = one segment” is not applied as a universal law.
- [ ] Screen/state transitions are treated as useful boundary candidates, not mandatory boundaries.
- [ ] Semantic/causal boundaries, not screen count, drive segmentation.
- [ ] Simultaneous changes are separated when needed to expose what caused
  what, and meaningful “no visible change yet” states are preserved when they
  explain a role or mental model.
- [ ] Splitting does not mechanically raise integration cost.
- [ ] Earlier relevant information remains available or easy to reopen when
  later understanding requires comparison/integration; guided forward progress
  may coexist with review access.
- [ ] Reviewing earlier steps preserves learner state and answers where
  practical; an intended reset is clear.
- [ ] Cumulative presentation is treated as a promising candidate, not a
  universal or uniquely proven optimum; exact tabs/accordions/layout remain
  local or experimental.
- [ ] A compact post-completion reference is added only when useful for likely
  later re-entry, not as a requirement on every page.

## Contiguity / split attention

- [ ] Mutually dependent visual/text or code/explanation sources are close enough to integrate without unnecessary search.
- [ ] The learner is not forced to scroll repeatedly between a screenshot and a required settings/value list.
- [ ] Split attention is judged by the need for mental integration, not physical distance alone.
- [ ] Video: motion is used when it contributes to understanding/performance; relevant narration and visual changes are synchronised, and signaling/segments help learners follow the material.
- [ ] Video: learners can control playback; exact values/commands remain available in text; captions, transcripts, and audio description are provided as applicable.
- [ ] Video controls and any required interaction are keyboard accessible; gratuitous motion is removed.

## Coherence and redundancy

- [ ] Every retained element has a task, warning, reference, accessibility, explanation, or feedback role.
- [ ] Irrelevant decorative images, sidebars, audio, animation, emoji, and digressions are removed.
- [ ] The same complete instructional path is not presented twice as competing primary routes without benefit.
- [ ] Each visible sentence materially helps understanding, a decision, next
  action, error prevention/recovery, state interpretation, reference value, or
  accessibility; obvious UI-state narration is reworked when it adds no value.
- [ ] The prose-value check retains useful causal explanation, misconception
  prevention, directions, status/accessibility messages, and clarifying
  elaboration; it is not applied as “shorter is always better”.
- [ ] Useful verification/performance feedback that resolves learner
  uncertainty is not removed as UI-state narration merely because the result is
  also visible; redundant status narration is distinguished from feedback.
- [ ] An identical duplicate visible result sentence with no distinct role is
  removed, while a visual-to-text mapping or accessibility equivalent is kept
  when it provides access or interpretation.
- [ ] Invisible assistive-technology status announcements serve their own
  purpose and are not forced into visible prose when that would add noise.
- [ ] Mapping cues, labels, numbers, exact values, and accessibility equivalents are not removed mechanically as duplicate content.
- [ ] A settings table does not duplicate a primary visual/code example row-for-row unless it has a distinct lookup/accessibility purpose.

## Concepts and pre-training

- [ ] Need/context comes before the term where useful; a first appearance may itself name and define the term before later use.
- [ ] No term is used as if already known, and no glossary is front-loaded just to satisfy a definition-first rule.
- [ ] Each Concept supports knowledge needed for current or near activity; near-first-use is a default with intentional pre-training, summary, retrieval, or reference exceptions.
- [ ] Placement is judged by the learner's activity and knowledge rather than a component-position template.
- [ ] Each Concept makes its meaning and relevance to the intended activity clear.
- [ ] Length serves clarity; 6+ sentences triggers review for mixed ideas rather than a hard limit or scientific threshold. There is no preferred sentence-count target.

## Activation

- [ ] When a useful prior-knowledge anchor exists, the lesson activates it through recall, comparison, an earlier task/lesson, or a sound analogy.
- [ ] No analogy/metaphor is invented merely to satisfy an Activation checklist item.
- [ ] Activation recalls established knowledge; it is not used as a substitute for teaching an unfamiliar term.

## Appropriate assistance / progressive independence

- [ ] Assistance fits learner knowledge, performance, and goal; guidance minimization is not an objective.

- [ ] Learners with low or unestablished relevant prior knowledge receive enough worked/guided support before substantial independent construction.
- [ ] Default novice scaffolding allows a suitable, high-fidelity, supported PS-I/Productive Failure design; it is not mistaken for unguided struggle.
- [ ] Learners with established prior knowledge may start at guided or independent application when appropriate.
- [ ] Guidance is faded, retained, or restored according to prior knowledge/performance rather than a fixed repetition count.
- [ ] Guided variation makes the learner's decision points clear without unnecessarily re-teaching everything.
- [ ] The page is not forced to contain worked, guided, and independent phases when its scope does not require all three.

## Meaningful learner activity

- [ ] Relevant processing may include prediction, comparison, selection, organization, debugging, adaptation, creation, retrieval, explanation, or application.
- [ ] Active/generative learning is not mechanically required on every job-aid or initial-performance-only page.

## Engagement / meaningful challenge

- [ ] Enjoyment is not equated with ease; rigor is not equated with unnecessary frustration.
- [ ] Authentic relevance, visible progress, competence-supportive feedback, meaningful choice, or learner control are considered where useful, without requiring every option.
- [ ] Relevance is not fabricated and choice is not added for its own sake.
- [ ] Both actual capability evidence and learner experience inform revision; felt fluency alone does not establish learning.

## Durable learning / progression and aligned evidence

- [ ] Unit outcomes have appropriate evidence at useful Event/progression points, rather than a Section-local closure requirement.
- [ ] Observable behavior/state goals use a Verify-like check when appropriate.
- [ ] Retrieval/understanding goals use a QuickCheck-like retrieval task when appropriate.
- [ ] Multi-condition milestones use a checklist only when several conditions genuinely define the milestone.
- [ ] Applied tasks may test ordinary practice or transfer; transfer goals use a task with meaningfully changed conditions and selection/adaptation of the learned principle.
- [ ] Passive result verification is not mislabeled as generative learning.
- [ ] Generative activities require learners to retrieve, explain, predict, organise, integrate, or apply information.
- [ ] Prediction/prequestion prompts target a concrete upcoming relation or
  outcome, and benefits are not generalized to unrelated unprequestioned
  content.
- [ ] The code/object is clear, the pre-attempt state does not leak the answer,
  and post-attempt feedback shows the actual result with useful causal
  explanation rather than only correct/incorrect.
- [ ] Correctness-only feedback does not end the feedback loop when elaboration
  would help; the learner receives the concrete result and an appropriate
  explanation, correction, or next-step support.
- [ ] Code-output prediction is offered for suitable initial programming
  instruction, not required everywhere.
- [ ] When useful, self-explanation prompts identify the relation, error, or
  concept to explain; generic “explain why” is not presumed superior.
- [ ] Non-empty self-explanation text is not taken as evidence of correctness.
- [ ] Ungraded free text is not assigned fake semantic correctness or treated as
  a valid correctness gate without a real semantic assessment.
- [ ] Ungraded reflection does not become a fake required gate; an explicit
  reveal route exists when appropriate.
- [ ] When the canonical explanation would leak planned generation or
  self-explanation, feedback is staged as verification plus the concrete result,
  then learner generation/self-explanation, then canonical elaborated feedback.
- [ ] Where useful, the learner's complete generated statement appears near the
  canonical explanation; reflection is used selectively at conceptual
  transitions rather than mechanically after every action.
- [ ] Immediate success is described as initial performance, not proof of durable learning or transfer.
- [ ] Important knowledge is revisited in later events through retrieval and
  distributed practice when curriculum scope owns that scheduling; in-page
  cumulative review supports offloading but does not replace later spacing or
  transfer practice.
- [ ] Error recovery is not counted as learning-goal closure.
- [ ] No closure surface is added mechanically just because a Section exists.

## Pre-attempt conditions for retrieval and generation

- [ ] When a task is intentionally designed to elicit unaided retrieval (e.g., a QuickCheck testing recall) or learner generation (e.g., a task requiring the learner to produce or generate the target response), learner-visible prompt material and default pre-attempt state do not reveal the target response or decisive cues that remove the intended retrieval/generation opportunity before the learner's first attempt.
- [ ] When a response is deliberately supplied as worked instruction, guided modeling, or scaffolded support, that design choice is recognised as guided practice, not unaided retrieval/generation evidence.
- [ ] Task design reflects the instructional goal, learner knowledge, and evidence for the tactic; exercises do not uniformly hide answers or minimise guidance.

## Error prevention and recovery

- [ ] Common/high-impact failure points receive useful prevention and/or diagnosis support.
- [ ] Preventive warnings appear before the risky action when appropriate.
- [ ] Reactive recovery appears after the plausible failure point.
- [ ] Recovery follows symptom → likely cause → concrete fix.
- [ ] No recovery advice merely says “try again” or “redo it” without diagnosis.

## Signaling

- [ ] Bold/callouts/highlights are tied to task-relevant identities, exact values, sequence, or gestures.
- [ ] Competing emphasis is limited so the important signal remains visually distinctive.
- [ ] Strong signals are selective; unimportant material is not given competing emphasis merely for decoration.
- [ ] Visual grouping cues represent actual semantic grouping rather than serving as generic decoration.
- [ ] Repeated task-action mappings use consistent cues when they represent the same meaning/operation.
- [ ] Exact colours, border widths, radii, spacing, or component-family counts are not presented as research-determined without direct evidence.
- [ ] Any numeric bold-density lint threshold is treated as an advisory heuristic, not a scientific boundary.
- [ ] Goal-irrelevant decoration/emotional stimulation is removed; deliberate affective design is retained only when aligned with the goal and not creating competing processing.

## Prose clarity

- [ ] Clarity takes priority over brevity; necessary causality, UI/state correspondence, action purpose, state transitions, and term meanings are retained.
- [ ] Headings predict the task, topic, or capability; terms are explained before their understanding is required, not necessarily before their first appearance.

- [ ] Prose is natural, direct, and active; Japanese zero-subject sentences are acceptable.
- [ ] The body does not contain author-facing audience meta prose such as 「受講者は〜」「学習者は〜」「初学者向け」 when it does not help the task.
- [ ] Ordinary domain uses of 「ユーザー」 remain allowed when they refer to a real app/product end user.
- [ ] The page does not open with authoring rationale or document-description prose when task context would be more useful.

## Accidental difficulty cold-read

- [ ] Cold-read review detects unexplained prerequisites, ambiguity, missing state, unnecessary backtracking, undefined assumptions, terminology gaps, and visual/prose mismatches.
- [ ] Review preserves retrieval effort, problem solving, decision making, productive struggle, and changed-condition transfer.

## Accessibility

- [ ] Every informative non-text visual has a text alternative that serves the same purpose or conveys the essential information.
- [ ] Complex annotated screenshots/diagrams/charts use a concise short alternative plus a detailed equivalent rather than one oversized alt string.
- [ ] Accessibility-equivalent instructions are retained even when the essential information also appears visually.
- [ ] Callouts/highlights do not rely on colour alone.
- [ ] Normal text/images of text meet 4.5:1 contrast; large text may use 3:1.
- [ ] Meaningful non-text UI/graphical indicators meet the applicable 3:1 non-text contrast requirement.
- [ ] Real text is preferred to images of text when equivalent presentation is practical.
- [ ] Interactive examples are keyboard operable in a logical order.
- [ ] After a meaningful state change, the changed source/target/result can be
  identified without memory-based comparison; a persistent cue remains until
  inspection is possible, and animation is supplemental.
- [ ] Reduced-motion preferences are respected and text/UI contrast remains
  intact during transitions.
- [ ] Applicable status changes are exposed accessibly; W3C techniques are
  treated as examples rather than universal mandates.
- [ ] A single-line response with one primary submit action uses native form
  semantics where applicable so Enter and the visible control mean the same
  validation and state transition; multiline/control exceptions are respected.
- [ ] Custom Enter handling accounts for IME composition or is avoided.
- [ ] Section 508 is invoked only when the content is actually in U.S. federal ICT scope; WCAG 2.2 AA is the default target.

## Flexible use / re-entry

- [ ] Major section goals/headings are self-explanatory enough for a reader arriving mid-tutorial to orient themselves.
- [ ] Optional background/reference detail can be skipped or collapsed when the platform supports it.
- [ ] Sequential dependencies are explicit rather than forcing the reader to infer what prior steps were required.

## Next actions

- [ ] If next-step guidance is useful, it appears at the document end and links to concrete follow-up actions.
- [ ] A tutorial is not given a meaningless NextSteps block merely to satisfy structure.
- [ ] No vague “see official docs” pointer appears without a useful destination.

## Course Docs platform contracts *(only when applicable)*

Load `references/course-docs-platform.md` and check these items when the target
site uses `@metyatech/course-docs-platform`.

- [ ] Section goals are optional orientation at all depths, including Event-bearing Sections; goals are neither canonical Unit objectives nor Evidence.
- [ ] No `---` horizontal rule appears inside a Section.
- [ ] `<Verify>` source does not include the leading `→` rendered by the component.
- [ ] Course Docs QuickCheck/Exercise tasks use problem content → zero or more `<Hint>` blocks → exactly one non-empty final `<Answer>`; optional Hints are non-empty direct children before Answer.
- [ ] The first Hint avoids unnecessarily revealing the answer immediately; later Hints may become progressively stronger or more explicit.
- [ ] Hints default to established material but may explicitly teach new information; unfamiliar information is explained before it is required as known.
- [ ] Each `<Answer>` lets learners understand correctness; simple, self-explanatory tasks may use concise answers when additional explanation adds no learning value. Reasoning or a plausible misconception is addressed when useful without inventing one.
- [ ] No `authoringMode` or legacy Solution block is present.
- [ ] `<Prerequisites>` appears before the first Section when prerequisites exist.
- [ ] `<NextSteps>` is optional; when used, it is at the document end.
- [ ] Multiple images, Concept length, bold density, learner-meta prose, and similar note-tier findings are reviewed as heuristics rather than treated as automatic pedagogical failures.

## Evidence and boundary conditions

- [ ] Each disputed/high-impact rule is classified as R, S, L, or U before being presented as research-based.
- [ ] R claims have multiple-study/research-synthesis support within relevant boundary conditions.
- [ ] S claims have a traceable multi-study inference chain and do not combine one research result with unaudited design intuition.
- [ ] L decisions are explicitly local/normative/platform choices rather than research findings.
- [ ] U decisions are not promoted into pedagogical rules merely to fill a design gap.
- [ ] The author has loaded `references/research-foundations.md` when a disputed or high-impact pedagogical rule needs evidence review.
- [ ] Research principles are not presented as universal formatting laws when medium, expertise, outcome, or population changes the boundary conditions.
- [ ] Course Docs contracts and local quality conventions are not misrepresented as direct scientific findings.
- [ ] Real learner evidence takes priority over an assumed heuristic when the heuristic demonstrably harms task performance or learning.

## Review-execution policy *(user-specific QA procedure)*

These items represent user-adopted quality assurance practice and process policy,
not empirical learning-science claims. They are encoded here as explicit
user-specific execution standards for tutorial approval and review.

- [ ] Final tutorial approval and review inspect the complete final artifact, not only the diff or a subset of changes.
- [ ] For sequential or cumulative tutorials, review proceeds in learner-visible order while carrying forward the state produced by each required step and by each optional branch when evaluating consequences.
- [ ] When an out-of-edit-scope issue violates applicable rules or is blocking, do not silently ignore it; report it and do not claim a clean PASS status.
