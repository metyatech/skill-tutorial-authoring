# Research foundations and evidence boundaries

Load this reference when a tutorial-authoring decision needs research rationale,
a boundary-condition check, or source verification. Do not treat every concrete
Course Docs convention as a scientific mandate.

## Cognitive-load framing used by this skill

Sweller, van Merriënboer & Paas (2019) provide the operational baseline used by
this skill: do not treat intrinsic, extraneous, and germane load as three
independent additive loads.

- **Intrinsic load** reflects interacting task elements relative to learner
  knowledge.
- **Extraneous load** reflects avoidable processing introduced by presentation
  or instructional procedure relative to the instructional goal.
- What older literature called **germane load** is better understood as
  working-memory resources devoted to learning-relevant processing, not a third
  independent load that should simply be maximised.

Kalyuga & Plass (2025) propose a further **integrated, goal-driven revision** of
CLT. Their framework makes load classification explicitly relative to
instructional goals and incorporates learner characteristics including prior
knowledge, motivation, and affect. They also discuss evidence from productive
failure/desirable-difficulty research where higher initial load can support
conceptual learning or transfer under some conditions.

Treat this 2025 account as an important proposed revision rather than claiming
that one formulation is universally settled. Authoring implication: define the
instructional goal first, reduce processing that is avoidable relative to that
goal, manage task complexity for the learner, and consider motivation/affect
when they materially affect engagement or capacity.

## Rule provenance

Research provenance uses four codes:

| Code | Meaning |
|---|---|
| **R — multiple-research-supported** | Multiple independent studies or research syntheses support the direction within relevant boundary conditions |
| **S — multi-study research synthesis** | An explicit inference chain combines only research-supported premises from multiple studies/syntheses |
| **L — local decision** | Normative purpose, quality convention, product choice, or platform contract; not an empirical finding |
| **U — unresolved** | Available research does not determine the authoring/design decision |

The adopted educational purpose is **L/normative**: enjoyable, positive learning
with actual capability growth and increasing ability to think, create, and
continue learning independently. Research evaluates means, effects, and boundary
conditions; it does not uniquely determine that value judgment.

For **S**, document the premises and inference chain here. Do not combine one
research result with unaudited design intuition and call the result
research-based. **U** items remain unresolved until additional evidence or
direct evaluation justifies a local choice; they are not pedagogical rules by
default. Evidence strength and lint/enforcement severity remain separate axes.

## Learning objectives, events, and aligned evidence

Biggs's constructive alignment connects intended learning outcomes, teaching
and learning activities, and assessment: activities and evidence should call on
the kinds of learning named in the objectives. This grounds the design
relationship among **Learning Units** (stable objectives/capabilities),
**Learning Events** (individual learning/practice occurrences targeting Units),
and **Evidence / Assessment** (observable evidence aligned to the objective).
The distinction between Learning Unit and Event is a useful local model, not a
standardized taxonomy imposed by Biggs.

A **Page** is a presentation/distribution unit, not an objective or learning
occurrence. One Unit may recur in Events across multiple pages or occasions; an
Event may target more than one Unit. Teaching material can normally be followed
in Event order without a separate teacher lesson plan duplicating the
learner-visible experience.

An **Exercise** names a task/container format, not an evidence level. It can
support ordinary practice or transfer. Evidence counts as transfer when the
conditions meaningfully differ and learners must select or adapt a learned
principle; relabeling routine practice as an Exercise does not establish
transfer.

Section-local closure is not part of this Learning System model. Evidence is
aligned to Unit outcomes at suitable Event/progression points; presentation
boundaries and goal banners do not establish assessment or mastery.

## Learner-facing orientation

**Evidence:** Hamilton (1985) proposed a context-sensitive framework for
evaluating adjunct questions and objectives in instructional prose that
accounts for text structure and learner characteristics. This framework is not
direct evidence that objectives are effective. Luiten, Ames, and Ackerson's
(1980) meta-analysis of 135 published and unpublished studies found that
advance organizers can facilitate learning and retention. For findings on
preinstructional objectives, directions, and questions, see
[`Preinstructional objectives`](#preinstructional-objectives).

**Boundary / what this does NOT prove:** These findings support keeping useful
objectives and organizers available as options; they do not make an orientation
banner useful merely because it exists, establish one optimal placement for
every learner/task, or show that every orientation form improves learning.
They do not support a blanket rule to remove objectives or advance organizers.

**Authoring implication:** Review an introduction, objective summary, Section
goal, preview, prerequisite callout, or sequence announcement for concrete
value to the activity, structure, or decision at its location. Consider
reworking material that only repeats nearby headings/prose, a guaranteed
sequence, a canonical Unit objective, or information not yet usable. This is
an **L review convention**, not a research finding or a ban on orientation.

An unfamiliar term may appear before its explanation, including in a heading.
When understanding is needed, explain its meaning before relying on it. Mayer's
**Pre-training Principle** is research-backed for multimedia learning: people
learn better when a complex lesson is preceded by training in the names and
characteristics of its main concepts. Applying this principle to Course Docs
text/code tutorials by explaining a relation before a later activity depends on
it is a bounded application; Mayer did not directly establish that result for
these tutorial formats or that relations must always be pre-taught. Do not
require defining every term before its first appearance or pre-training in
every lesson.

Prior knowledge can matter without requiring prerequisite UI on every page.
In a guaranteed linear sequence, a callout with no added preparation, re-entry,
or recovery value is a candidate for removal; retain it when it supports an
actual learner decision or use.

## Instructional continuity and local coherence

Keep the direct research findings separate from the Course Docs **S synthesis**.

### McNamara, Kintsch, Songer, and Kintsch (1996)

**Direct research finding:** Two experiments studied junior-high students'
comprehension of science texts with different levels of coherence. Coherence
helped readers with low domain knowledge. Readers with sufficient background
knowledge could benefit from minimally coherent text that prompted them to
infer unstated relations, including deeper understanding in some measures
([McNamara et al., 1996](https://doi.org/10.1207/s1532690xci1401_1)).

**Boundary:** These were science-text comprehension studies, not tests of
Course Docs paragraph order, transition sentences, or the timing of a tool or
concept in a tutorial. The results do not show that adding explanations or
transitions is always better.

**Contribution to S synthesis:** These findings support the premise that
low-prior-knowledge learners can need explicitly stated relations that more
knowledgeable learners may infer. Combined with heading/signaling evidence and
evidence that some inference is intentionally useful in retrieval/problem
solving, this contributes to the later **S — novice local discourse continuity**
rule. This study alone does not establish a required transition form or a
need-before-concept sequence.

### McNamara and Kintsch (1996)

**Direct research finding:** In two experiments using high- and low-coherence
history texts, low-coherence text required more inference processing. Readers'
prior knowledge affected whether those inferences were successful and useful;
high-knowledge readers did better on some deep-comprehension measures after
low-coherence text ([McNamara & Kintsch, 1996](https://doi.org/10.1080/01638539609544975)).

**Boundary:** The authors studied history-text comprehension and specific
outcomes. The finding does not prescribe low coherence as an instructional
strategy, nor does it test transition wording or Course Docs sequencing.

**Course Docs bounded implication:** Do not turn local coherence into a
universal maximum-coherence rule. Preserve inference deliberately required by
retrieval or problem-solving activities, and do not require novice-level
bridging for learners whose relevant prior knowledge supports the intended
inference.

### Renkl (2014)

**Direct research finding:** Example-based learning is effective for initial
cognitive skill acquisition. Renkl's theory integrates work on worked
examples, observational learning, and analogical reasoning; it emphasizes
learner processing of solution rationales and structural relations so that
examples support principle-based understanding, rather than assuming that
watching an example alone guarantees abstraction
([Renkl, 2014](https://doi.org/10.1111/cogs.12086)).

**Boundary:** This theory does not test the specific CSS example sequence
`class="nedan"` → `.nedan`, nor establish one universal placement for a
general rule, Verify, or QuickCheck in Course Docs.

**Research-synthesis implication:** Example-based learning supports using worked
or guided examples where they fit learner knowledge and the learning goal, but
it does not establish one universal Course Docs ordering of need, operation,
result, principle, and check. Apply separate evidence for contiguity when
mutually dependent sources must be integrated, and apply the retrieval/generation
pre-attempt evidence below only when those activities are intended. Essential
main-path explanation should not be hidden only in optional support when later
activity depends on it.

## Academic enjoyment and achievement emotions

**Evidence:** Camacho-Morles et al. (2021) found positive associations between
academic enjoyment and performance and negative associations for anger and
boredom, with variation by school level and measurement.

**Boundary / what this does NOT prove:** Associations do not establish that
making every task easy causes learning. Enjoyment, felt fluency, and achievement
are different outcomes; this evidence does not prove the normative purpose.

**Authoring implication:** Attend to positive engagement and unnecessary
frustration alongside capability evidence. Preserve meaningful challenge and
competence-supportive feedback; do not treat constant comfort as a criterion.

## Autonomy support

**Evidence:** Mammadov and Schroeder (2023) synthesized perceived teacher/parent
autonomy support and positive learning outcomes. Relationships were strongest
for autonomous motivation, engagement, and self-beliefs and weaker for academic
performance, with substantial heterogeneity.

**Boundary / what this does NOT prove:** Correlational evidence does not show
that removing instruction or adding choices causes mastery. Autonomy support is
compatible with structure and appropriate assistance.

**Authoring implication:** Respect learner agency and offer useful control while
keeping expectations, support, and feedback clear. Guidance minimization is not
the aim; use enough support for the learner and task.

## Meaningful choice and utility value

**Evidence:** Patall, Cooper, and Robinson (2008) found benefits of choice for
motivation and related outcomes across varied child/adult settings, with
moderators. Hulleman and Harackiewicz (2009) tested learner-generated relevance
connections in high-school science; interest and grades improved particularly
for students with low success expectations.

**Boundary / what this does NOT prove:** Choice is not itself a learning
objective; no choice-count recipe follows. A specific relevance intervention
does not justify fabricated relevance or guarantee benefits in every domain.

**Authoring implication:** Offer meaningful choices when they serve agency or
learning, and help learners identify authentic uses of what they learn. Do not
add choice merely to satisfy a template.

## Actual learning versus feeling of learning

**Evidence:** Deslauriers et al. (2019) compared active and passive instruction
in introductory college physics. Students could learn more under active
instruction while feeling that they learned less.

**Boundary / what this does NOT prove:** This setting does not establish that
all difficulty is beneficial or that learner experience should be ignored.

**Authoring implication:** Use outcome-aligned evidence alongside experience
feedback. Make progress visible and explain the role of meaningful effort;
retain retrieval, problem solving, and decisions while removing accidental
confusion. Neither enjoyment nor perceived ease demonstrates mastery alone.

## Linguistic clarity and elaboration

**Evidence:** Strohmaier et al. (2023) synthesized experimental modifications
of STEM texts: 45 studies, *N* = 6,477 learners, and 188 effects. The small
overall effect was *g* = .15. Personalization and increasing clarity/elaboration
showed positive effects; reducing complexity and increasing cohesion alone did
not show significant effects. Learners with lower content prior knowledge
benefited more.

**Boundary / what this does NOT prove:** This does not establish sentence-count
limits or prove that shorter prose is clearer. STEM text findings are not a
universal Japanese writing template.

**Authoring implication:** Clarity > brevity is a local quality convention
consistent with these boundaries. Keep causal relations, term meanings,
UI/state correspondence, action purposes, and state transitions when needed;
review length semantically rather than targeting 2–5 sentences.

Prompt completeness (object/content, required judgment/action, and expected
response form) and natural stem/option wording are Course Docs quality
conventions synthesized from clarity and task-action alignment, not outcomes
directly tested by this meta-analysis. Exact Japanese-copy checks remain a
local quality convention. These findings support clarity/context-sensitive
revision, not a claim that shorter or simpler text is always better.

Breakall, Randles, and Tasker (2019) developed and evaluated a multiple-choice
item-writing flaws instrument on general chemistry exams. Their account treats
item-writing flaws as threats to validity because they can change performance
independently of the target chemistry knowledge and add unwanted noise. It
includes flaws such as moving the central idea from the stem into the choices.
This supports keeping the central idea in the stem and making choices read as
natural answers for that stem in multiple-choice items. It does not establish a
universal rule for every open-response prompt or discipline.

## Prediction and scaffolded self-explanation

**Prequestions:** St. Hilaire, Chan, and Ahn's (2024) meta-analysis found a
substantial prequestion effect on prequestioned material (*g* = .54), while the
average general effect on untested material was virtually zero (*g* = .04).
Prequestions should therefore target a concrete upcoming relation or outcome;
their benefits must not be generalized to unrelated, unprequestioned content.

**Programming prediction:** Tucker et al. (2024) randomly assigned 121 college
novices with no coding experience to predict code output before explanation or
to receive tell-and-practice instruction. The prediction group showed greater
learning and more positive non-cognitive outcomes. This is domain- and
population-specific evidence supporting prediction as an option for suitable
initial programming instruction, not a mandatory tutorial pattern.

**Scaffolded self-explanation:** In two experiments on feedback after physics
problem-solving errors, generic self-explanation prompts did not consistently
outperform no prompt. In Experiment 2, scaffolded prompts led to higher-quality
explanations, more error correction, and better near (but not far) transfer
than standard prompts or no prompt. Use this narrowly: when learners need to
explain an error or relation, identify what to explain when useful; do not claim
that a generic “explain why” prompt is automatically superior. Text entry alone
is not evidence that the explanation is correct.

Not grading reflection semantically is a local interaction contract: do not
make a self-explanation a fake mandatory gate, and provide an explicit route to
reveal the explanation or answer when appropriate. This is not a learning
finding and does not replace appropriate feedback or retrieval practice.

## Formative feedback and post-attempt results

**Feedback principle:** Shute (2008) defines formative feedback as information
communicated to a learner with the intent of modifying thinking or behaviour to
improve learning. Her review supports feedback that is specific, focused on the
task/process or useful self-regulation, and actionable, while noting that
effectiveness depends on factors such as timing, learner characteristics, and
task context. This supports giving a learner useful information about what
actually happened and what to do or understand next; it does not support
turning every visible interface change into extra explanatory prose.

**Computer-based feedback meta-analysis:** Van der Kleij, Feskens, and Eggen
(2015) synthesised item-based feedback in computer-based learning environments
across 40 studies and 70 effect sizes. Elaborated feedback had an effect size
of .49, correct-answer (knowledge-of-correct-response) feedback had .32, and
correctness-only / knowledge-of-results feedback had .05. Elaborated
feedback was particularly more effective than the other forms for higher-order
learning outcomes. These results are bounded to the reviewed computer-based,
item-level feedback literature and its measured outcomes; they do not establish
that one feedback form is best for every task, medium, learner, or ungraded
free-text response.

**Authoring implication:** Distinguish useful verification or performance
feedback from redundant UI-state narration. Retain objectively or checkably
scorable feedback when it resolves uncertainty about the learner's performance,
even when a visual result is also present. After a prediction, give the concrete
observed outcome or relation; correctness-only feedback is not sufficient when
elaboration would help. Supportive comparison wording may be useful for an
exploratory prediction, but its exact wording, tone, colour, and icon style are
local decisions. Remove status narration such as “recorded”, “added”, or “result
shown below” when it adds no learning, action, recovery, orientation, or
accessibility value. Avoid an identical duplicate visible result sentence when
it has no distinct role, while retaining a concise visual-to-text mapping or
accessibility equivalent when it provides access or interpretation.

If a canonical explanation would leak a planned self-explanation or generation
target, stage the response as: verification plus the concrete result; learner
generation or self-explanation; then the canonical elaborated explanation. Do
not assign fake semantic correctness to ungraded free text. In provenance terms,
the Shute and Van der Kleij feedback principle is **R** within these boundaries;
the staged sequence is an **S** Course Docs synthesis from feedback plus
generation/self-explanation evidence; exact wording, tone, and styling are **L**
local decisions.

## Headings and structural signaling

**Evidence:** Lorch, Lemarié, and Chen (2013) compared headings and preview
sentences in two text-processing experiments. In one experiment, headings
improved memory for subtopics over preview sentences, with no difference for
memory of simple facts. In another, outlining was better when topic structure
was signaled than when it was not, with no reliable difference between headings
and previews. Effects depended on the reading task and outcome.

Ritchey, Schuster, and Allen (2008) had college students read a multiple-topic
expository text while experimentally varying the relatedness of headings to
text content and the distance between them. Free recall of main topics was
facilitated when content was related to and close to headings, and inhibited
when it was unrelated or distant. Conditional recall of subordinate information
was not affected by relatedness or distance.

**Boundary / what this does NOT prove:** Headings do not prescribe one teaching
order, numbering format, or goal-first page layout. These studies do not directly
compare verbs such as “look” and “write” in headings and activities. Ritchey et
al. support the narrower claim that heading/content relatedness can affect
readers' recall of main topics; they do not directly demonstrate learner-action
consistency or show that matching action language causes better comprehension
or learning.

**Authoring implication:** Use headings that predict the task, topic, or
capability and expose useful structure. A title can name a new term before it
is explained; explain it before its understanding is required.

### S — Course Docs learner-action consistency

This is a multi-study research synthesis, not a directly tested rule about
particular verbs. The inference chain is:

1. heading/content relatedness and signaling can improve attention to useful
   structure and memory for that structure;
2. HCI studies of consistent task-action mappings show benefits for learning
   and use when the same meaning/action recurs consistently;
3. text-coherence research shows that low-prior-knowledge readers can be harmed
   when needed relations must be inferred without enough support.

Therefore, when a Course Docs heading, immediate explanation, task statement,
and relevant UI cue all refer to the same learner-action stage, keep their
action mapping semantically consistent. Treat a mismatch as a defect when it
forces a decision unrelated to the learning task. Natural paraphrases are
acceptable; multiple actions are acceptable when order and stages are explicit.
Do not turn this synthesis into a mechanical same-word lint rule.

### S — novice local discourse continuity

This is also a multi-study synthesis. McNamara/Kintsch coherence findings show
that low-prior-knowledge readers often need more explicit relations, while
heading/signaling research supports exposing useful structure. Retrieval,
problem solving, and productive-failure evidence simultaneously shows that some
inference and struggle can be intentional.

Therefore, in novice-oriented initial instruction, state short causal or purpose
bridges when they are required to understand why the next topic, operation, or
concept appears. Do not add transitions mechanically, maximize coherence for
every learner, or remove inference that is itself the intended learning
activity.

## Signaling selectivity, perceptual grouping, and visual complexity

**R — signaling:** Schneider, Beege, Nebel, and Rey (2018) meta-analysed 103
studies with 12,201 participants. Signaling improved retention and transfer on
average and reduced cognitive load. This supports making task-relevant structure
and important information perceptually distinctive.

**R/S — selective emphasis:** Lorch, Lorch, and Klusewitz (1995) compared no,
light, and heavy typographical signaling. Target-only signaling improved cued
recall, while heavy signaling did not outperform the control condition. Combined
with the broader signaling meta-analysis, the supported direction is to keep
strong emphasis selective rather than giving many competing elements equivalent
salience. This does not determine a specific colour, background, icon, or border.

**R/S — grouping:** Palmer (1992) showed that common region is a strong
perceptual grouping cue. Bae and Watson (2014) found that reinforcing combinations
of proximity, colour similarity, common region, connectivity, and alignment can
communicate more complex informational structure, with effectiveness depending
on the cue combination and structure. Authoring implication: use grouping cues
to represent actual semantic grouping; a border is one possible common-region
encoding, not a generic marker of importance.

**R/S — visual complexity:** Tuch et al. (2009) found that greater website
visual complexity increased visual-search time and reduced later recognition in
their tasks. Combined with signaling/selectivity evidence, avoid visual elements
that add complexity without a task, structure, feedback, accessibility, or
learning role. This does not imply that all borders, colour, or decoration are
harmful.

**S — task-action consistency:** Barnard et al. (1981), Tanaka, Eberts, and
Salvendy (1991), and Howes (1996) support benefits of consistent mappings or
positioning in interface learning/use. The bounded implication is to keep the
same task-action meaning mapped consistently when it recurs. These studies do
not establish that all components should share one visual style or that surface
uniformity itself improves learning.

## Preinstructional objectives

**Evidence:** Klauer (1984) synthesized preinstructional objectives,
directions, and questions shown before instructional text. Goal-relevant
learning improved, goal-irrelevant learning decreased, and overall learning was
slightly improved. Effects depended on text/task conditions.

**Boundary / what this does NOT prove:** This historical text literature does
not make every Section goal banner mandatory, prescribe Japanese verb tense,
or make a goal statement evidence of attainment.

**Authoring implication:** Offer learner-facing orientation when useful; keep
canonical Unit objectives separate from optional Section goals. An example,
problem, context, action, or goal may each orient a learner appropriately.

## Seductive details

**Evidence:** Cheng, Wu, Wang, and Wang (2026) synthesized effects of seductive
details on recall, comprehension, and transfer. Average effects were negative,
with moderators including language and learning environment.

**Boundary / what this does NOT prove:** Interesting features are not all
irrelevant details. The synthesis does not establish an emoji ban or disallow
goal-aligned emotional design; its mediation model is not a mandate to revert
to a three-additive-load account.

**Authoring implication:** Review whether an element supports explanation,
signaling, accessibility, or engagement, or competes for attention without a
learning role. Do not convert an average effect into a hard formatting rule.

## Initial-learning order and course progression

Use **I-PS** for instruction-first followed by problem solving, and **PS-I** for
problem-solving-first followed by instruction. These labels describe the order
of the initial instructional/problem-solving phases, not a page template or a
full course sequence.

Sinha and Kapur's meta-analysis compared PS-I with I-PS across 53 studies and
166 comparisons and found an average advantage for PS-I (Hedges' *g* = .36).
Effects were stronger in studies implementing PS-I with high fidelity to
Productive Failure principles (*g* range .37–.58). Grade level, intervention
duration, and study design moderated outcomes; trends favored I-PS for younger
learners (grades 2–5) and domain-general skills. Productive Failure is therefore
a high-fidelity subset/variant of PS-I, not a synonym for PS-I generally. A
deliberately designed, supported problem-before-instruction experience is not
unguided struggle. Inquiry-Based Learning is a broader Strategy and does not
mean unguided discovery: a meta-analysis of 72 studies found that guidance
facilitated inquiry learning activities, performance success, and learning
outcomes. Use a Strategy only when compatible with the Pattern and objectives;
smaller techniques such as worked examples, self-explanation, and retrieval
practice need not be forced into a single taxonomy.

Course progression is the ordered recurrence of Events. Consider later
retrieval and distributed practice, cumulative/mixed practice, interleaving
where it fits the material and objective, and transfer. No meta-analysis below
establishes one universal event order or locally synthesized sequence as an
optimal recipe:

- Yang et al. synthesized 222 classroom studies involving 48,478 students;
  classroom testing/quizzing improved achievement overall (Hedges' *g* = .499),
  with effects moderated by factors such as corrective feedback, repetition,
  timing, and test/material alignment.
- Mawson and Kang reviewed 22 applied classroom reports (31 effect sizes,
  *N* > 3,000) and found a moderate benefit for distributed over massed
  practice (*d* = .54). A quantitative moderator analysis was not possible due
  to the number of included studies.
- Brunmair and Richter synthesized 59 studies (238 effect sizes) and found an
  overall interleaving effect (*g* = .42), but the advantage varied by material:
  it was stronger for paintings/visual materials, smaller for mathematical
  tasks, nonsignificant for expository text and taste, and blocking favored for
  word material. Treat interleaving as conditional, not a universal schedule.
- Freeman et al. meta-analysed 225 undergraduate STEM studies. In the 158
  studies reporting exam/concept-inventory outcomes, active-learning designs
  improved performance by 0.47 SD; in the 67 failure-rate studies, students in
  traditional lecture courses were about 1.5 times as likely to fail. This
  supports meaningful learner engagement, not a fixed page/event structure or
  any particular engagement technique.

## Instructional goal: initial performance, learning, and transfer

Procedural instructions do not have one universal objective. Eiriksdottir &
Catrambone (2011) distinguish **initial performance**, **learning (including
retention)**, and **transfer** and review trade-offs among them. Highly specific procedural
directions often support immediate execution, while learning and transfer can
benefit from principles, problem solving, fading, examples, or variation that
require more active processing. Their review also notes that these goals can be
combined rather than treated as mutually exclusive.

Authoring implication:

- decide the intended horizon before choosing representation or assistance;
- do not use fastest first-attempt completion as the sole quality metric when
  retention or transfer is required;
- a one-time job aid can legitimately optimise differently from a lesson meant
  to be recalled later without the instructions;
- fading and combined instruction can preserve usability while building
  independence.

Lemarié, Castillan & Eyrolle (2016) found in one procedural domain that novices
executed better with text-plus-picture than picture-only instructions, while
experts did not show the same need. Treat that study as domain-specific evidence
that representation needs depend on expertise, not as a universal
text-plus-picture mandate.

## Multimedia-learning principles

### Multimedia principle

Mayer's multimedia principle concerns learning from **words and pictures** versus
words alone when the representations support understanding. It is not a rule
that every operational step needs an image.

For software tutorials, the **Primary Representation** model in SKILL.md is
an **L local design model**. Multimedia, contiguity, split-attention, redundancy,
signaling, and minimalism evidence constrain that choice, but do not uniquely
derive the model or its table. Do not present the model as a research synthesis
or as the literal statement of Mayer's multimedia principle.

### Spatial contiguity

Place corresponding words and visuals close enough that the learner does not
have to search or remember one source while locating the other. This applies
when two sources genuinely correspond; it is not a reason to create a visual
for an otherwise clear text/code action.

### Temporal contiguity

Synchronise corresponding words and visuals in media with a time axis, such as
narrated video or animation. For a static page, spatial contiguity is the more
relevant principle.

### Coherence and emotional design

Remove information, decoration, media, or digressions that do not serve the
learning objective. “Decorative” is not a property of a visual format by itself:
a sidebar, image, or callout is appropriate when it carries task, warning,
reference, accessibility, or feedback information.

Goal-irrelevant decoration and emotional stimulation can capture attention and
add competing processing. Emotional-design studies also find that selected,
goal-aligned affective features can support learning or motivation in some
multimedia contexts. A 2021 meta-analysis of 28 studies reported positive
effects for the examined design features, while other syntheses identify
variation by feature, outcome, and learner/material conditions. Treat emotional
design as purposeful and conditional: use it when it can support motivation or
attention without distracting from the learning goal or increasing competing
processing; do not equate all affective design with decoration.

### Redundancy

Avoid making the learner process the same complete instructional path twice
when the duplication has no useful role. Do not apply this mechanically.

Useful overlap can reduce mapping/search cost. Labels, identifiers, numbered
callouts, positional anchors, exact values, or accessibility equivalents may be
necessary in more than one representation.

Accessibility-equivalent content is not gratuitous redundancy. Presentation can
still minimise competing parallel paths for sighted readers while preserving a
complete equivalent route for assistive technology or on-demand access.

**S — visible-prose value test:** Coherence and Minimalism support removing
goal-irrelevant detail while retaining information needed to act, understand,
recover, orient, and access the material. Linguistic-feature evidence also
shows that clarity and elaboration can help, while reducing complexity alone
does not reliably improve STEM-text learning. Together, these sources support
reviewing whether a visible sentence changes understanding, a decision, the
next action, causal interpretation, error recovery, useful orientation, or
accessibility. Obvious UI narration with no such role is a deletion candidate;
this is not a mechanical brevity rule. Assistive-technology status messages
serve a separate purpose and should not be forced into visible prose when that
adds noise. This is a cross-source review synthesis, not a directly tested
sentence-level deletion instrument (Strohmaier et al., 2023,
https://doi.org/10.1016/j.edurev.2023.100533; van der Meij & Carroll, 1995;
WCAG 2.2 SC 4.1.3,
https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html).

A 2026 software-video experiment (Désiron, Endres & Schneider) found that more
spatially integrated task-relevant signaling overlap improved retention/transfer
and reduced extraneous load in that specific medium. Treat this as a boundary-
condition example, not as proof that more redundancy is universally better.

### Segmenting

The research principle is to present complex material in meaningful,
learner-manageable segments rather than one continuous unit. It does **not**
define a universal “one screen = one segment” law.

Rey et al. (2019) meta-analyzed 56 investigations and 88 comparisons. Meaningful
segmentation showed small-to-medium effects for retention and transfer, reduced
cognitive load, and increased learning time. Segment by semantic/causal
boundaries rather than screen count; separate simultaneous changes when that
helps learners observe each causal contribution, but do not split when
integration cost would rise. Preserving a meaningful “no visible change yet”
state is a local design application, not a directly tested universal rule.

For software tutorials, screen/state transitions are useful candidate boundaries,
but semantic sub-goals are stronger. Coding or conceptual tasks can require
segmentation without any screen transition.

### Cumulative presentation and re-entry

Ito and Ichikawa (2026) compared cumulative visual disclosure with whole-slide
presentation in one narrated biology lesson with 40 Japanese university
students. Learning outcomes favored cumulative presentation (*d* = .49), with
earlier/longer attention to congruent visual material. Treat this as promising
direct evidence for that presentation and population, not enough to establish a
universal R rule or a Course Docs interaction pattern.

Chen et al. (2026) provide a review of the relationship between cognitive
offloading and the transient information effect. Their synthesis relates
external availability/permanence to reduced working-memory demands, while
emphasizing task and learner moderators and the distinction between the two
literatures. Combined with meaningful segmenting and the
cumulative-presentation study, the **S — bounded Course Docs synthesis** is:
when later understanding requires comparison or integration, keep earlier
relevant information available or easy to revisit. Forward-guided novice
progression can coexist with review access; this does not establish complete
free navigation as beneficial. Tabs, accordions, collapsing, precise layout,
and post-completion references remain local/experimental choices; a compact
reference is useful only when later quick re-entry is likely.

### Dynamic change awareness and meaningful sequence

Baudisch et al. (2006) demonstrated that users may miss display changes and
evaluated persistent afterglow cues that show transitions while leaving the
result immediately available. This supports attention to change awareness; it
does not determine an educational effect or a universally correct cue, style,
or duration.

**S — bounded Course Docs synthesis:** When a sequential dynamic tutorial
reveals new instruction after an action, place it at or after that trigger in
meaningful reading/focus order so the learner can follow the action and its
result without searching earlier prose. This applies coherence/change
awareness principles while respecting WCAG meaningful-sequence and focus-order
guidance. Keep semantic, visual, programmatic reading, and keyboard focus order
aligned when order affects meaning. W3C techniques such as inserting dynamic
content after its trigger and exposing status messages are examples that may
apply; they are not universal mandates. A major step change should be clear near
the current attention locus, with a remote progress indicator only as a
secondary orientation cue. Normally top-to-bottom reading flow is a local
default for this tutorial context; source/result cue combinations and other
dynamic-flow details are local design conventions, not directly tested
universal tutorial laws.

Choosing persistent source/target/result cue combinations and their duration is
an L product/accessibility decision informed by this HCI evidence and WCAG
contracts; it is not a demonstrated educational effect or a universal visual
pattern.

### Signaling

Use cues to direct attention toward structure and task-relevant information.
Signals may include visual callouts, a concise goal, an exact value, or a key
UI identity. Signaling density must be scaled to the task and learner; do not
turn a numeric bold-count threshold into a learning-science law.

### Pre-training

Before a complex task, teach the names and key characteristics of unfamiliar
parts that the learner needs to coordinate. In a minimalist static tutorial,
this often means a short Concept placed near first meaningful use rather than a
large theory chapter at page start.

### Personalization

Conversational/direct wording can help under some conditions, but effects vary
by medium, task, and population. Do not translate the principle into a rigid
Japanese second-person template. Japanese zero-subject prose can be direct and
learner-facing.

The local prohibition on phrases such as 「受講者は〜」「初学者向け」 in the
lesson body is a **quality convention**, not a direct scientific consequence of
the personalization principle.

### Video and other multimedia principles

Video is within scope; see [`video.md`](video.md) for practical authoring and
accessibility guidance. Apply multimedia evidence with attention to the
specific medium, goal, learner, and outcome.

### Modality, voice, image, embodiment, immersion

These principles require audio, speaker imagery/voice, embodiment, or immersive
media. They are outside the default scope of this skill. Consult the primary
source when working with those media.

## Split attention

Split attention occurs when learning requires mental integration of multiple
sources that are difficult to coordinate. Physical separation is a common
cause, but the underlying problem is the **integration requirement**, not mere
pixel distance.

Authoring implication: integrate or closely coordinate mutually dependent
sources. Do not force scrolling between a screenshot and a required settings
list when the information can be combined or kept adjacent.

## Worked examples, scaffolding, and expertise reversal

Worked examples are especially useful when relevant prior knowledge is low.
Assistance can become redundant or harmful as expertise increases.

Tetzlaff et al. (2025) meta-analysed 176 effect sizes from 60 experimental
studies with 5,924 participants. Low-prior-knowledge learners benefited from
higher-assistance instruction, while high-prior-knowledge learners benefited
from lower-assistance instruction. This supports adaptive fading, but **not** a
fixed repetition schedule such as “second occurrence = guided, third =
independent”.

Do not generalise expertise reversal as “every multimedia principle reverses for
experts”. Scale the specific assistance whose relevance has changed.

A useful progression when it matches the task is:

1. complete worked example;
2. completion/guided variation;
3. independent application.

The objective is appropriate assistance, not minimizing guidance. Starting
later is appropriate when relevant prior knowledge is already
established. Restoring guidance is appropriate when performance shows that
fading was premature.

## Activation

Merrill's activation principle concerns recalling **existing relevant
knowledge**, not teaching unfamiliar terms. Useful bridges include a prior task,
comparison with a known concept, an earlier lesson, or a sound analogy.

Do not manufacture an analogy where no helpful bridge exists.

## Retrieval practice and generation effect: pre-attempt conditions

When a learning event intentionally targets unaided retrieval or learner generation
(e.g., a retrieval-practice QuickCheck or problem-solving task), learner-visible
prompt material and default pre-attempt content should not reveal the target
response or provide a decisive cue that removes the intended retrieval or
generation opportunity before the learner's first attempt.

**Evidence — Retrieval Practice:**

Agarwal, Nunes & Blunt (2021) synthesized 50 classroom experiments investigating
retrieval practice across diverse learners, materials, and settings. The review
included 49 effect sizes across *n* = 5,374 students. Retrieval practice showed
consistent benefits for long-term learning: 57% of the observed effect sizes
indicated medium or large benefits, with an overall trend toward positive outcomes.

**Boundary / what this does NOT prove:**

- The review itself reports that only 6% of the reviewed experiments were conducted
  in non-WEIRD countries, indicating substantial geographic/cultural concentration
  in the evidence base.
- This evidence is drawn from classroom contexts and may not generalise uniformly
  to all digital or self-paced environments; keep generalization appropriately cautious
  if retained beyond classroom settings.
- The review notes heterogeneity in effect magnitudes and calls for continued
  study of moderator variables.
- Consistent benefits does not mean retrieval practice is universally superior for
  every learning context; initial performance, transfer, and other goals may have
  different demand profiles.

**Evidence — Generation Effect:**

Bertsch, Pesta, Wiscott & McDaniel (2007) meta-analyzed 86 studies spanning 445
effect sizes. The generation effect (learning gains from producing or generating
information vs. passive reading) showed an average effect size of .40. The
meta-analysis identified substantial moderator variability, indicating that
conditions and presentation context shape the magnitude of the advantage.

**Boundary / what this does NOT prove:**

- Bertsch et al. compares generation with reading and does not by itself establish
  whether unsupported generation outperforms guided generation or worked examples,
  or justify unguided struggle.
- Generation advantage varies with learner characteristics, task type, and retention
  interval.
- This evidence supports generation as beneficial when conditions are suited; it
  does not mandate unguided struggle or eliminate the role of guided practice and
  scaffolding.
- Separate evidence on scaffolding, expertise, and the conditions governing
  instructional support is needed to guide assistance choices.

**Authoring implication:**

If a task is intentionally designed to elicit unaided retrieval (e.g., a
QuickCheck testing memory for previously taught material) or learner generation
(e.g., a task that requires the learner to produce or generate the target response),
avoid presenting the target response, complete worked solutions, or decisive cues
in the learner-visible prompt or default pre-attempt state. Doing so removes the
retrieval or generation opportunity before the learner's first attempt.

If the response is deliberately supplied as worked instruction, guided modeling,
or scaffolded support (e.g., a worked example, completion task, or faded support),
that design choice serves a different instructional purpose. The learner's
interaction is then guided practice or verification, not unaided retrieval or
generation evidence. This is compatible with retrieval-practice and generation
principles; it reflects a deliberate choice about the form of support.

This does NOT imply that all exercises must hide answers, that guidance should
always be minimized, or that every learning event must maximize generative
difficulty. Choose task design to fit the instructional goal, learner knowledge,
and evidence for the tactic being applied.

## Retrieval, generative activity, feedback, and durable learning

These constructs overlap in practice but are not interchangeable.

- **Retrieval practice** asks the learner to recall information from memory.
- **Generative activity** asks the learner to select, organise, integrate,
  explain, predict, or apply information.
- **Feedback** gives information about performance or understanding.
- **Aligned evidence** connects an assessment surface to a Unit outcome at a
  suitable Event/progression point; it is not a Section-local ending contract.

A visual Verify can provide useful feedback without being a generative-learning
activity. A QuickCheck that requires retrieval or explanation can be generative.
An Exercise may or may not be generative depending on its design.

Immediate success is not durable mastery. Classroom meta-analytic evidence
supports later retrieval and distributed practice, with moderators such as
feedback and timing. Immediate evidence can show current performance; later
curriculum encounters are needed when retention/transfer matters.

## Minimalism

Use the four broad Minimalism principles as design directions:

1. **Action orientation** — let learners begin meaningful action early.
2. **Task anchoring** — organise around real learner goals rather than feature
   inventories.
3. **Error support** — support prevention, detection, diagnosis, and recovery.
4. **Flexible use** — support scanning, re-entry, and non-linear consultation
   within the limits of a sequential tutorial.

Do not read Minimalism as “remove all explanation”. Remove information that is
not needed now; retain complementary information needed to act, understand,
recover, or verify.

## Mayer 3rd edition date and principle set

Do not force a single year onto Mayer's *Multimedia Learning, Third Edition*
without qualification. Cambridge's current product metadata lists digital and
print publication dates in **2020**, while Cambridge's own frontmatter states
`© 2021`, `First published 2021`, and `Third edition 2021`; the same frontmatter
also reproduces Library of Congress cataloguing data that names 2020. Treat the
2020/2021 difference as a bibliographic metadata issue, not a pedagogical fact.

The principle set is clearer: the third edition presents 15 multimedia-design
principles, with **Embodiment**, **Immersion**, and **Generative Activity** as
the final three principle chapters. Do not describe Split-attention and
Transient Information as those three additions. Split-attention and
transient-information research belong to the broader multimedia/CLT literature,
including the *Cambridge Handbook of Multimedia Learning*.

Keep Mayer's *Multimedia Learning* distinct from Mayer & Fiorella's edited
*Cambridge Handbook of Multimedia Learning* (3rd ed., 2021).

## Research does not currently determine

Keep the following as **U** unless newer, directly applicable evidence resolves
them or a clearly labelled local evaluation chooses among alternatives:

- exact Course Docs colours, tint strength, border widths, radii, and spacing;
- an exact relative salience value for a KeyPoint-like signal;
- a fixed number of visual component families;
- a universal "one functional unit = one border" rule;
- exact Japanese technical-prose line length and typography values for this
  platform;
- CodePreview minimum editor height and toolbar density;
- tabs versus vertically stacked code/result panes on mobile.

A local prototype or usability test may select among these alternatives. Record
that choice as **L/experimental** rather than retrofitting a research rationale.

## Boundary conditions

Cromley & Chen (2025) synthesised Mayer's multimedia-learning research across
92 articles, 181 studies, and 591 effects. Effects varied meaningfully by
principle, medium, outcome, age, domain, and other study characteristics.

Therefore:

- treat principles as evidence-informed defaults, not universal formatting
  laws;
- state medium/population limits when they matter;
- avoid converting effect averages into arbitrary structural thresholds;
- keep local Course Docs contracts explicitly labelled as local contracts.

## Sources

- Schneider, S., Beege, M., Nebel, S., & Rey, G. D. (2018).
  *A meta-analysis of how signaling affects learning with media*.
  https://doi.org/10.1016/j.edurev.2017.11.001
- Lorch, R. F., Lorch, E. P., & Klusewitz, M. A. (1995).
  *Effects of Typographical Cues on Reading and Recall of Text*.
  https://doi.org/10.1006/ceps.1995.1003
- Palmer, S. E. (1992). *Common region: A new principle of perceptual grouping*.
  https://doi.org/10.1016/0010-0277(92)90014-S
- Bae, J., & Watson, B. (2014).
  *Reinforcing Visual Grouping Cues to Communicate Complex Informational Structure*.
  https://doi.org/10.1109/TVCG.2014.2346998
- Tuch, A. N., Bargas-Avila, J. A., Opwis, K., & Wilhelm, F. H. (2009).
  *Visual complexity of websites: Effects on users' experience, physiology,
  performance, and memory*. https://doi.org/10.1016/j.ijhcs.2009.04.002
- Barnard, P. J., Hammond, N. V., Morton, J., Long, J. B., & Clark, I. A. (1981). *Consistency and compatibility in
  human-computer dialogue*. https://doi.org/10.1016/S0020-7373(81)80024-7
- Tanaka, T., Eberts, R. E., & Salvendy, G. (1991).
  *Consistency of Human-Computer Interface Design: Quantification and Validation*.
  https://doi.org/10.1177/001872089103300604
- Howes, A. (1996). *Learning Consistent, Interactive, and Meaningful
  Task-Action Mappings: A Computational Model*.
  https://doi.org/10.1207/s15516709cog2003_1
- Camacho-Morles, J., Slemp, G. R., Pekrun, R., Loderer, K., Hou, H., &
  Oades, L. G. (2021). *Activity Achievement Emotions and Academic Performance:
  A Meta-analysis*. https://doi.org/10.1007/s10648-020-09585-3
- Agarwal, P. K., Nunes, L. D., & Blunt, J. R. (2021). *Retrieval Practice
  Consistently Benefits Student Learning: A Systematic Review of Applied Research
  in Schools and Classrooms*. https://doi.org/10.1007/s10648-021-09595-9
- Bertsch, S., Pesta, B. J., Wiscott, R., & McDaniel, M. A. (2007). *The
  generation effect: A meta-analytic review*. https://doi.org/10.3758/BF03193441
- Mammadov, S., & Schroeder, K. (2023). *A meta-analytic review of the
  relationships between autonomy support and positive learning outcomes*.
  https://doi.org/10.1016/j.cedpsych.2023.102235
- Patall, E. A., Cooper, H., & Robinson, J. C. (2008). *The effects of choice
  on intrinsic motivation and related outcomes: A meta-analysis of research
  findings*. https://doi.org/10.1037/0033-2909.134.2.270
- Hulleman, C. S., & Harackiewicz, J. M. (2009). *Promoting interest and
  performance in high school science classes*.
  https://doi.org/10.1126/science.1177067
- Deslauriers, L., McCarty, L. S., Miller, K., Callaghan, K., & Kestin, G.
  (2019). *Measuring actual learning versus feeling of learning in response to
  being actively engaged in the classroom*. https://doi.org/10.1073/pnas.1821936116
- Strohmaier, A. R., Ehmke, T., Härtig, H., & Leiss, D. (2023). *On the role
  of linguistic features for comprehension and learning from STEM texts.
  A meta-analysis*. https://doi.org/10.1016/j.edurev.2023.100533
- Breakall, J., Randles, C., & Tasker, R. (2019). *Development and use of a
  multiple-choice item writing flaws evaluation instrument in the context of
  general chemistry*. *Chemistry Education Research and Practice, 20*, 369–382.
  https://doi.org/10.1039/C8RP00262B
- St. Hilaire, J. R., Chan, J. C. K., & Ahn, D. (2024). *Guessing as a
  learning intervention: A meta-analytic review of the prequestion effect*.
  https://doi.org/10.3758/s13423-023-02353-8
- Tucker, M. C., Wang, X. (W.), Son, J. Y., & Stigler, J. W. (2024).
  *Prediction versus production for teaching computer programming*.
  https://doi.org/10.1016/j.learninstruc.2023.101871
- Zhang, Q., & Fiorella, L. (2024). *Effects of self-explaining feedback on
  learning from problem-solving errors*. *Contemporary Educational Psychology,
  79*, 102326.
  https://doi.org/10.1016/j.cedpsych.2024.102326
- Rey, G. D., Beege, M., Nebel, S., Wirzberger, M., Schmitt, T. H., &
  Schneider, S. (2019). *A meta-analysis of the segmenting effect*.
  https://doi.org/10.1007/s10648-018-9456-4
- Ito, H., & Ichikawa, H. (2026). *Cumulative presentation enhances learning
  outcomes by directing learners' visual attention*. *Journal of Computer
  Assisted Learning, 42*(4), e70286. https://doi.org/10.1002/jcal.70286
- Chen, O., Allen, R., Waterman, A., & Sweller, J. (2026). *The relationship
  between cognitive offloading and the transient information effect*.
  *Educational Psychology Review, 38*, 35.
  https://doi.org/10.1007/s10648-026-10132-9
- Baudisch, P., Tan, D., Collomb, M., Robbins, D., Hinckley, K., Agrawala, M.,
  Zhao, S., & Ramos, G. (2006). *Phosphor: Explaining transitions in the user
  interface using afterglow effects*. *Proceedings of UIST '06*, 169–178.
  https://doi.org/10.1145/1166253.1166280
- Ritchey, K., Schuster, J., & Allen, J. (2008). *How the relationship between
  text and headings influences readers’ memory*. *Contemporary Educational
  Psychology, 33*(4), 859–874. https://doi.org/10.1016/j.cedpsych.2007.11.001
- Lorch, R. F., Lemarié, J., & Chen, H. T. (2013). *Signaling topic structure
  via headings or preview sentences*. https://doi.org/10.1016/S1135-755X(13)70011-3
- Klauer, K. J. (1984). *Intentional and Incidental Learning with Instructional
  Texts: A Meta-Analysis for 1970–1980*. https://doi.org/10.3102/00028312021002323
- Hamilton, R. J. (1985). *A Framework for the Evaluation of the Effectiveness
  of Adjunct Questions and Objectives*.
  [https://doi.org/10.3102/00346543055001047](https://doi.org/10.3102/00346543055001047)
- Luiten, J. W., Ames, W. S., & Ackerson, G. (1980). *A Meta-analysis of the
  Effects of Advance Organizers on Learning and Retention*.
  [https://doi.org/10.3102/00028312017002211](https://doi.org/10.3102/00028312017002211)
- McNamara, D. S., Kintsch, E., Songer, N. B., & Kintsch, W. (1996). *Are
  Good Texts Always Better? Interactions of Text Coherence, Background
  Knowledge, and Levels of Understanding in Learning From Text*.
  [DOI](https://doi.org/10.1207/s1532690xci1401_1)
- McNamara, D. S., & Kintsch, W. (1996). *Learning from texts: Effects of
  prior knowledge and text coherence*. *Discourse Processes, 22*(3), 247–288.
  [DOI](https://doi.org/10.1080/01638539609544975)
- Renkl, A. (2014). *Toward an Instructionally Oriented Theory of
  Example-Based Learning*. *Cognitive Science, 38*(1), 1–37.
  [DOI](https://doi.org/10.1111/cogs.12086)
- Cheng, C., Wu, Y., Wang, R., & Wang, Z. (2026). *Seductive Details,
  Cognitive Load, and Learning Outcomes: A Multi-level Meta-analysis and MASEM*.
  https://doi.org/10.1007/s10648-025-10099-z

- Biggs, J. (1996). *Enhancing teaching through constructive alignment*.
  https://doi.org/10.1007/BF00138871
- Sinha, T., & Kapur, M. (2021). *When Problem Solving Followed by Instruction
  Works: Evidence for Productive Failure*.
  https://doi.org/10.3102/00346543211019105
- Lazonder, A. W., & Harmsen, R. (2016). *Meta-Analysis of Inquiry-Based
  Learning: Effects of Guidance*. *Review of Educational Research, 86*(3),
  681–718. https://doi.org/10.3102/0034654315627366
- Yang, C., Luo, L., Vadillo, M. A., Yu, R., & Shanks, D. R. (2021).
  *Testing (quizzing) boosts classroom learning: A systematic and
  meta-analytic review*. https://doi.org/10.1037/bul0000309
- Mawson, R. D., & Kang, S. H. K. (2025). *The Distributed Practice Effect
  on Classroom Learning: A Meta-Analytic Review of Applied Research*.
  https://doi.org/10.3390/bs15060771
- Brunmair, M., & Richter, T. (2019). *Similarity matters: A meta-analysis of
  interleaved learning and its moderators*. https://doi.org/10.1037/bul0000209
- Freeman, S., et al. (2014). *Active learning increases student performance in
  science, engineering, and mathematics*. https://doi.org/10.1073/pnas.1319030111
- Wong, R. M., & Adesope, O. O. (2021). *Meta-Analysis of Emotional Designs in
  Multimedia Learning: A Replication and Extension Study*.
  https://doi.org/10.1007/s10648-020-09545-x
- Brame, C. J. (2016). *Effective Educational Videos: Principles and
  Guidelines for Maximizing Student Learning from Video Content*.
  https://doi.org/10.1187/cbe.16-03-0125
- Mayer, R. E. *Multimedia Learning* (3rd ed.). Cambridge University Press.
  Cambridge product metadata lists 2020 publication dates, while the official
  frontmatter states first published / third edition 2021.
  https://doi.org/10.1017/9781316941355
  Product metadata: https://www.cambridge.org/highereducation/books/multimedia-learning/FB7E79A165D24D47CEACEB4D2C426ECD/frontmatter/7E943DC693864D29EAFD709969EE629F
  Official frontmatter: https://assets.cambridge.org/97813166/38088/frontmatter/9781316638088_frontmatter.pdf
- Mayer, R. E., & Fiorella, L. (Eds.). (2021). *The Cambridge Handbook of
  Multimedia Learning* (3rd ed.). Cambridge University Press.
- Sweller, J., van Merriënboer, J. J. G., & Paas, F. (2019).
  *Cognitive Architecture and Instructional Design: 20 Years Later*.
  https://doi.org/10.1007/s10648-019-09465-5
- Kalyuga, S., & Plass, J. L. (2025). *Rethinking Cognitive Load Theory*.
  Oxford University Press. https://doi.org/10.1093/9780190078539.001.0001
- Eiriksdottir, E., & Catrambone, R. (2011). *Procedural Instructions,
  Principles, and Examples: How to Structure Instructions for Procedural Tasks
  to Enhance Performance, Learning, and Transfer*.
  https://doi.org/10.1177/0018720811419154
- Lemarié, J., Castillan, L., & Eyrolle, H. (2016). *Effects of expertise and
  multimedia presentation on the enactment and recall of procedural
  instructions*. https://doi.org/10.1016/j.psfr.2016.07.002
- Cromley, J. G., & Chen, R. (2025). *A meta-analysis of Richard Mayer's
  multimedia learning research: Searching for boundary conditions of design
  principles across multiple media types*.
  https://doi.org/10.1016/j.edurev.2025.100730
- Tetzlaff, L., Simonsmeier, B. A., Peters, T., & Brod, G. (2025).
  *A cornerstone of adaptivity – A meta-analysis of the expertise reversal
  effect*. https://doi.org/10.1016/j.learninstruc.2025.102142
- Kalyuga, S. (2007). *Expertise reversal effect and its implications for
  learner-tailored instruction*.
- van der Meij, H., & Carroll, J. M. (1995). Principles and heuristics for
  designing minimalist instruction.
- Carroll, J. M. (1990). *The Nurnberg Funnel*.
- Shute, V. J. (2008). *Focus on formative feedback*. Review of Educational
  Research, 78(1), 153–189. https://doi.org/10.3102/0034654307313795
- Van der Kleij, F. M., Feskens, R. C. W., & Eggen, T. J. H. M. (2015).
  *Effects of feedback in a computer-based learning environment on students'
  learning outcomes: A meta-analysis*. Review of Educational Research, 85(4),
  475–511. https://doi.org/10.3102/0034654314564881
- Merrill, M. D. (2002). First principles of instruction.
- Désiron, J. C., Endres, T., & Schneider, S. (2026). *Is it not too
  redundant? When signaling overlap reduces extraneous load and enhances
  retention in a software video tutorial*.
  https://doi.org/10.3389/fpsyg.2026.1795142
- W3C. *Web Content Accessibility Guidelines (WCAG) 2.2*.
  https://www.w3.org/TR/WCAG22/
