# Tutorial self-review checklist

Use this list when auditing a draft tutorial against `SKILL.md`. The checklist
separates generic tutorial-quality judgements from Course Docs-only platform
contracts.

## Scope and learner

- [ ] The target learner and relevant prior knowledge are stated or reliably implied.
- [ ] The intended instructional horizon is identified: immediate performance, retention, transfer, or a deliberate combination.
- [ ] First-attempt speed is not treated as the sole quality metric when retention or transfer is an explicit goal.
- [ ] The page is organised around learner goals rather than software features/menu structure.
- [ ] Assistance, signaling, Concept density, and narrative depth match the target learner.
- [ ] Expert or already-trained readers are not forced through redundant novice guidance.

## Primary representation / multimedia

- [ ] Each learner action deliberately chooses the most efficient primary representation for both the task and intended instructional horizon: visual, code/CodePreview, text, diagram, or motion media.
- [ ] Images are used when spatial position, appearance, or visual relationships matter; they are not added merely because a step is operational.
- [ ] Code changes use real code/CodePreview rather than screenshots when that is clearer and more accessible.
- [ ] Secondary prose adds complementary information or mapping cues rather than restating the complete procedure.
- [ ] Exact values, user-specific paths, and distinctions such as hover vs click remain available in text or another accessible equivalent.
- [ ] Short identity cues may appear in both representations when they reduce mapping/search cost.
- [ ] Accessibility-equivalent content is retained even when it repeats essential visual information; it is not removed as “redundancy”.
- [ ] A visual-primary Action is executable as a whole without requiring visible prose to restate the complete visual path; a complete accessible equivalent exists separately when needed.

## Action unit and segmenting

- [ ] Each Action is one coherent learner action episode or short locally unified sequence toward an immediate sub-goal.
- [ ] Actions are not split mechanically per click, field, or callout number.
- [ ] A multi-step UI navigation sequence remains one Action when it is cognitively one coherent episode.
- [ ] An Action is split when a meaningful state/sub-goal boundary, recovery point, or verification boundary makes the split useful.
- [ ] Segments are learner-manageable semantic chunks; “one screen = one segment” is not applied as a universal law.
- [ ] Screen/state transitions are treated as useful boundary candidates, not mandatory boundaries.

## Contiguity / split attention

- [ ] Mutually dependent visual/text or code/explanation sources are close enough to integrate without unnecessary search.
- [ ] The learner is not forced to scroll repeatedly between a screenshot and a required settings/value list.
- [ ] Split attention is judged by the need for mental integration, not physical distance alone.
- [ ] Video-only: corresponding narration and visual changes are synchronised.

## Coherence and redundancy

- [ ] Every retained element has a task, warning, reference, accessibility, explanation, or feedback role.
- [ ] Irrelevant decorative images, sidebars, audio, animation, emoji, and digressions are removed.
- [ ] The same complete instructional path is not presented twice as competing primary routes without benefit.
- [ ] Mapping cues, labels, numbers, exact values, and accessibility equivalents are not removed mechanically as duplicate content.
- [ ] A settings table does not duplicate a primary visual/code example row-for-row unless it has a distinct lookup/accessibility purpose.

## Concepts and pre-training

- [ ] Each Concept focuses on one new idea and only information needed for imminent use.
- [ ] The Concept is near the first meaningful use in an Action, Section, Verify, QuickCheck, Exercise, or equivalent task surface.
- [ ] No Concept introduces terminology that appears much later without current need.
- [ ] Each Concept answers “what is it?” and “why does it matter now?”.
- [ ] Roughly 2–5 sentences or one short table is preferred; 6+ sentences triggers review rather than automatic failure.

## Activation

- [ ] When a useful prior-knowledge anchor exists, the lesson activates it through recall, comparison, an earlier task/lesson, or a sound analogy.
- [ ] No analogy/metaphor is invented merely to satisfy an Activation checklist item.
- [ ] Activation recalls established knowledge; it is not used as a substitute for teaching an unfamiliar term.

## Scaffolding / progressive independence

- [ ] Learners with low or unestablished relevant prior knowledge receive enough worked/guided support before substantial independent construction.
- [ ] Learners with established prior knowledge may start at guided or independent application when appropriate.
- [ ] Guidance is faded, retained, or restored according to prior knowledge/performance rather than a fixed repetition count.
- [ ] Guided variation makes the learner's decision points clear without unnecessarily re-teaching everything.
- [ ] The page is not forced to contain worked, guided, and independent phases when its scope does not require all three.

## Practice, retrieval, feedback, and aligned closure

- [ ] Every substantive learning goal has evidence capable of testing that goal and its intended instructional horizon.
- [ ] Observable behavior/state goals use a Verify-like check when appropriate.
- [ ] Retrieval/understanding goals use a QuickCheck-like retrieval task when appropriate.
- [ ] Multi-condition milestones use a checklist only when several conditions genuinely define the milestone.
- [ ] Transfer/application goals use an applied task after sufficient support.
- [ ] Passive result verification is not mislabeled as generative learning.
- [ ] Generative activities require learners to retrieve, explain, predict, organise, integrate, or apply information.
- [ ] Immediate success is described as current performance, not proof of durable mastery.
- [ ] Important knowledge is revisited later through retrieval/distributed practice when curriculum scope owns that scheduling.
- [ ] Error recovery is not counted as learning-goal closure.
- [ ] No closure surface is added mechanically just because a Section exists.

## Error prevention and recovery

- [ ] Common/high-impact failure points receive useful prevention and/or diagnosis support.
- [ ] Preventive warnings appear before the risky action when appropriate.
- [ ] Reactive recovery appears after the plausible failure point.
- [ ] Recovery follows symptom → likely cause → concrete fix.
- [ ] No recovery advice merely says “try again” or “redo it” without diagnosis.

## Signaling

- [ ] Bold/callouts/highlights are tied to task-relevant identities, exact values, sequence, or gestures.
- [ ] Competing emphasis is limited so the important signal remains visually distinctive.
- [ ] Any numeric bold-density lint threshold is treated as an advisory heuristic, not a scientific boundary.
- [ ] Decorative/emotional emphasis is removed.

## Learner-facing prose

- [ ] Prose is natural, direct, and active; Japanese zero-subject sentences are acceptable.
- [ ] The body does not contain author-facing audience meta prose such as 「受講者は〜」「学習者は〜」「初学者向け」 when it does not help the task.
- [ ] Ordinary domain uses of 「ユーザー」 remain allowed when they refer to a real app/product end user.
- [ ] The page does not open with authoring rationale or document-description prose when task context would be more useful.

## Accessibility

- [ ] Every informative non-text visual has a text alternative that serves the same purpose or conveys the essential information.
- [ ] Complex annotated screenshots/diagrams/charts use a concise short alternative plus a detailed equivalent rather than one oversized alt string.
- [ ] Accessibility-equivalent instructions are retained even when the essential information also appears visually.
- [ ] Callouts/highlights do not rely on colour alone.
- [ ] Normal text/images of text meet 4.5:1 contrast; large text may use 3:1.
- [ ] Meaningful non-text UI/graphical indicators meet the applicable 3:1 non-text contrast requirement.
- [ ] Real text is preferred to images of text when equivalent presentation is practical.
- [ ] Interactive examples are keyboard operable in a logical order.
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

- [ ] Every top-level `<Section>` has a non-empty future-declarative `goal`; nested goals are optional.
- [ ] No `---` horizontal rule appears inside a Section.
- [ ] `<Verify>` source does not include the leading `→` rendered by the component.
- [ ] Course Docs QuickCheck/Exercise tasks use problem content → one or more `<Hint>` blocks → exactly one final `<Answer>`.
- [ ] Each `<Answer>` gives instructive feedback beyond a bare final token/value; it explains correctness and addresses a plausible misconception when one exists without inventing one.
- [ ] No `authoringMode` or legacy Solution block is present.
- [ ] `<Prerequisites>` appears before the first Section when prerequisites exist.
- [ ] `<NextSteps>` is optional; when used, it is at the document end.
- [ ] Multiple images, Concept length, bold density, learner-meta prose, and similar note-tier findings are reviewed as heuristics rather than treated as automatic pedagogical failures.

## Evidence and boundary conditions

- [ ] The author has loaded `references/research-foundations.md` when a disputed or high-impact pedagogical rule needs evidence review.
- [ ] Research principles are not presented as universal formatting laws when medium, expertise, outcome, or population changes the boundary conditions.
- [ ] Course Docs contracts and local quality conventions are not misrepresented as direct scientific findings.
- [ ] Real learner evidence takes priority over an assumed heuristic when the heuristic demonstrably harms task performance or learning.
