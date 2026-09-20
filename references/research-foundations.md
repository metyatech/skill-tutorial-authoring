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

Classify concrete rules separately from the research principles motivating
them:

| Class | Meaning | Example |
|---|---|---|
| Evidence-backed principle | Direction supported by research within boundary conditions | coherence, worked examples, retrieval |
| Quality convention | Local standard chosen for learner-facing quality | no author-facing audience meta prose |
| Platform contract | Rendering/component-system requirement | Course Docs task-block structure |
| Context-dependent heuristic | Useful review signal, not a scientific threshold | Concept sentence-count advisory |

Evidence strength does not determine lint severity. Machine confidence and cost
of an artefact defect are separate concerns.

## Instructional goal: performance, retention, and transfer

Procedural instructions do not have one universal objective. Eiriksdottir &
Catrambone (2011) distinguish **initial performance**, **learning/retention**,
and **transfer** and review trade-offs among them. Highly specific procedural
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

For software tutorials, the **Primary Representation** model in `SKILL.md` is a
local instructional-design heuristic derived from several principles at once:
multimedia, contiguity, split attention, redundancy, signaling, and minimalism.
Treat that model as a useful synthesis, not as the literal statement of Mayer's
multimedia principle.

### Spatial contiguity

Place corresponding words and visuals close enough that the learner does not
have to search or remember one source while locating the other. This applies
when two sources genuinely correspond; it is not a reason to create a visual
for an otherwise clear text/code action.

### Temporal contiguity

Synchronise corresponding words and visuals in media with a time axis, such as
narrated video or animation. For a static page, spatial contiguity is the more
relevant principle.

### Coherence

Remove information, decoration, media, or digressions that do not serve the
learning objective. “Decorative” is not a property of a visual format by itself:
a sidebar, image, or callout is appropriate when it carries task, warning,
reference, accessibility, or feedback information.

### Redundancy

Avoid making the learner process the same complete instructional path twice
when the duplication has no useful role. Do not apply this mechanically.

Useful overlap can reduce mapping/search cost. Labels, identifiers, numbered
callouts, positional anchors, exact values, or accessibility equivalents may be
necessary in more than one representation.

Accessibility-equivalent content is not gratuitous redundancy. Presentation can
still minimise competing parallel paths for sighted readers while preserving a
complete equivalent route for assistive technology or on-demand access.

A 2026 software-video experiment (Désiron, Endres & Schneider) found that more
spatially integrated task-relevant signaling overlap improved retention/transfer
and reduced extraneous load in that specific medium. Treat this as a boundary-
condition example, not as proof that more redundancy is universally better.

### Segmenting

The research principle is to present complex material in meaningful,
learner-manageable segments rather than one continuous unit. It does **not**
define a universal “one screen = one segment” law.

For software tutorials, screen/state transitions are useful candidate boundaries,
but semantic sub-goals are stronger. Coding or conceptual tasks can require
segmentation without any screen transition.

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

### Modality, voice, image, embodiment, immersion

These principles require audio, speaker imagery/voice, embodiment, or immersive
media. They are outside the default static-page scope of this skill. Consult the
primary source when working with those media.

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

Starting later is appropriate when relevant prior knowledge is already
established. Restoring guidance is appropriate when performance shows that
fading was premature.

## Activation

Merrill's activation principle concerns recalling **existing relevant
knowledge**, not teaching unfamiliar terms. Useful bridges include a prior task,
comparison with a known concept, an earlier lesson, or a sound analogy.

Do not manufacture an analogy where no helpful bridge exists.

## Retrieval, generative activity, feedback, and durable learning

These constructs overlap in practice but are not interchangeable.

- **Retrieval practice** asks the learner to recall information from memory.
- **Generative activity** asks the learner to select, organise, integrate,
  explain, predict, or apply information.
- **Feedback** gives information about performance or understanding.
- **Aligned closure** is this skill's local quality convention: a substantive
  goal should end with evidence capable of testing that goal.

A visual Verify can provide useful feedback without being a generative-learning
activity. A QuickCheck that requires retrieval or explanation can be generative.
An Exercise may or may not be generative depending on its design.

Immediate success is not durable mastery. Classroom meta-analytic evidence
supports later retrieval and distributed practice, with moderators such as
feedback and timing. Page-local closure can show current performance; later
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
- Shute, V. J. (2008). Focus on formative feedback.
- Merrill, M. D. (2002). First principles of instruction.
- Yang, C., Luo, L., Vadillo, M. A., Yu, R., & Shanks, D. R. (2021).
  *Testing (quizzing) boosts classroom learning: A systematic and
  meta-analytic review*. https://pubmed.ncbi.nlm.nih.gov/33683913/
- Mawson, R. D., & Kang, S. H. K. (2025). *The Distributed Practice Effect
  on Classroom Learning: A Meta-Analytic Review of Applied Research*.
  https://doi.org/10.3390/bs15060771
- Désiron, J. C., Endres, T., & Schneider, S. (2026). *Is it not too
  redundant? When signaling overlap reduces extraneous load and enhances
  retention in a software video tutorial*.
  https://doi.org/10.3389/fpsyg.2026.1795142
- W3C. *Web Content Accessibility Guidelines (WCAG) 2.2*.
  https://www.w3.org/TR/WCAG22/
