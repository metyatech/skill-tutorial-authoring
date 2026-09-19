# Tutorial self-review checklist

Use this list when auditing a draft tutorial against every
principle encoded in `SKILL.md`. Items marked *(auto)* are
already enforced by `remarkTutorialLint` at build time; items
marked *(judgement)* require human review.

Work top-down: structural items first, then each principle in
the order it appears in the Scientific foundations table.

## Structure *(auto where marked)*

- [ ] Every top-level `<Section>` declares a `goal` *(auto)*
- [ ] Nested `<Section>` goals are present only when they improve orientation *(judgement)*
- [ ] Goal is written in future-declarative form *(auto advisory)*
- [ ] Components are used where the local task needs them; the page does not depend on a page-wide tutorial/non-tutorial classification *(judgement)*
- [ ] Explanation, Action, Verify, QuickCheck, Exercise, Reference, and other task components may be mixed locally without forcing a fixed page-wide flow *(judgement)*
- [ ] No `---` horizontal rules inside a Section *(auto)*
- [ ] Multiple images inside one `<Action>` have been reviewed as a possible split/composite opportunity *(auto note)*
- [ ] `<Verify>` body does not start with a literal `→` *(auto)*
- [ ] No `<Reference>` whose only content is an image *(auto note)*
- [ ] No `authoringMode` frontmatter or separate Solution block appears; QuickCheck and Exercise use problem content → Hint+ → Answer *(judgement)*

## Prerequisites *(judgement)*

- [ ] A Prerequisites section exists at the page top (or is
      intentionally omitted because none are needed)
- [ ] Each prerequisite is concrete and verifiable (software
      version, completed prior tutorial, specific prior
      knowledge)
- [ ] No vague prerequisites ("基本的な知識があること")

## Target learner *(judgement)*

- [ ] The intended learner expertise level is stated or
      reliably implied by context
- [ ] Signaling, Concept density, and narrative depth match
      that level (no over-scaffolding for experts, no
      under-scaffolding for novices)

## Primary representation / Multimedia *(judgement)*

- [ ] Each Action deliberately chooses the most efficient primary representation: visual, code/CodePreview, text, diagram, or motion media
- [ ] Images are used when spatial position, appearance, or visual relation matters; they are not added merely because the step is operational
- [ ] Code changes use code/CodePreview as primary when that is clearer than a screenshot
- [ ] Secondary prose contains only complementary information or mapping cues, not a second copy of the complete procedure
- [ ] Typed values, user-specific paths, and distinctions such as hover vs click remain available in text or another accessible equivalent
- [ ] Short identity cues may appear in both representations when they help bind them together

## Spatial / Temporal contiguity *(judgement)*

- [ ] Corresponding visual/text or code/explanation pairs are directly adjacent rather than separated by unrelated content
- [ ] (Video only) Narration and image changes are synchronised

## Split-attention *(judgement)*

- [ ] No screenshot is explained by a table or text block
      placed far away on the page (requiring scroll to compare)
- [ ] Numbered callout explanations appear immediately adjacent
      to the screenshot, not in a separate section

## Coherence *(judgement)*

- [ ] No decorative images, sidebars, emoji spam, or余談
- [ ] Every retained element traces to a learning objective

## Modality *(judgement; video-only)*

- [ ] (Video only) Narration does not duplicate on-screen text
- [ ] Static pages: mark this row N/A

## Redundancy *(judgement)*

- [ ] The same complete instruction or explanation is not repeated across two representations
- [ ] Identity cues, labels, or numbers are retained when they reduce mapping/search cost instead of being removed mechanically
- [ ] No settings table duplicates a primary visual or CodePreview row-for-row without adding a distinct lookup purpose

## Segmenting *(judgement)*

- [ ] Each Section closes one semantically coherent sub-goal
- [ ] Within a single screen or dialog, operations are grouped
      into one Action (not mechanically split per field)
- [ ] Section boundaries align with screen/state transitions

## Minimalism P1: Action orientation *(judgement)*

- [ ] The first Action appears early; no long front-loaded
      prose
- [ ] No reference tables or long Concepts appear before the
      first Action of the top-level Section

## Minimalism P2: Task anchoring *(judgement)*

- [ ] Top-level and nested Sections are organised around the
      learner's task goals, not around software features or
      menu structure
- [ ] Each nested Section's `goal` (when present) explains the
      task-domain reason for that sub-step, not just the
      technical operation

## Minimalism P3: Error support *(judgement)*

- [ ] Recovery is present at common or high-impact novice failure
      points where diagnosis/recovery materially helps
- [ ] Recovery follows "symptom → cause → fix" structure
- [ ] Preventive notes appear before high-failure-probability
      actions where appropriate
- [ ] No Recovery says "やり直してください" without diagnosis

## Minimalism P4: Flexible use *(judgement)*

- [ ] Each top-level Section's goal is self-explanatory enough
      for a reader arriving mid-tutorial to decide if they
      need this Section
- [ ] Concepts and References are collapsible so experienced
      readers can skip them
- [ ] The tutorial does not require reading every prior
      top-level Section to understand the current one (within
      reasonable limits of sequential tutorials)

## Signaling *(judgement)*

- [ ] Bold emphasis is used only on learning-objective elements
      (UI identities when useful for mapping, typed values, key gestures)
- [ ] No sentence contains three or more bold spans
- [ ] Numbered callouts, labels, or short identity cues are repeated in text only when they materially improve mapping between representations
- [ ] No decorative bold/highlight for emotional emphasis

## Pre-training *(judgement)*

- [ ] Each Concept sits immediately before first use of the term or idea
- [ ] No Concept introduces a term that appears much later on the page
- [ ] Each Concept focuses on one new concept and only the information needed now
- [ ] Roughly 2–5 sentences is preferred; 6+ sentences triggers review for multiple concepts or Reference material rather than automatic failure
- [ ] Each Concept answers both "what is it?" and "why need to know now?"

## Activation *(judgement)*

- [ ] New concepts include an analogy or bridge to something
      the learner already knows (where a plausible prior-
      knowledge anchor exists)
- [ ] Activation is distinct from Pre-training: it recalls
      existing knowledge, not introduces new terms

## Personalization / learner-facing prose *(judgement)*

- [ ] Prose is natural, direct, and active; Japanese zero-subject sentences are acceptable
- [ ] The lesson body does not contain author-facing audience meta prose such as "受講者が〜", "学習者は〜", or "初学者向け"
- [ ] Ordinary domain uses of 「ユーザー」 remain allowed when they refer to an actual app/product end user rather than the tutorial reader
- [ ] No page opens by describing what the document is or who it is for when that information does not help perform the task
- [ ] Friendliness stays restrained (no emoji spam, 余談, or emotional decoration)

## Accessibility *(judgement)*

- [ ] Every informative Action/Verify image has an `alt` prop that preserves the information needed to follow or verify the step
- [ ] Callouts and highlights use shape/labels in addition to colour where colour alone would carry meaning
- [ ] Image-only meaning is recovered in nearby text or another text equivalent
- [ ] Normal text / images of text in screenshot annotations meet 4.5:1 contrast; large text meets 3:1
- [ ] Meaningful non-text callout shapes / UI-state indicators meet the applicable 3:1 non-text contrast requirement
- [ ] Real text is preferred to images of text when the same presentation can be achieved with text
- [ ] Heading hierarchy remains semantic (`h2` → `h3`)

## Generative activity / aligned closure *(judgement)*

- [ ] Every substantive learning goal has a closure that can actually test that goal
- [ ] Observable behavior/state goals use Verify where appropriate
- [ ] Retrieval/understanding goals use QuickCheck where appropriate
- [ ] Multi-condition milestones use Checkpoint only when a checklist is useful
- [ ] Transfer/application goals use Exercise after sufficient worked/guided support
- [ ] Recovery is treated as error support, not as goal closure
- [ ] QuickCheck and Exercise use problem content first, then one or more Hints, then an Answer
- [ ] No closure component is added mechanically just because a Section exists

## Scaffolding / Progressive independence *(judgement)*

- [ ] The tutorial begins with Phase 1 (complete worked
      example) before asking for independent work
- [ ] When the same operation pattern repeats, later
      occurrences reduce guidance (Phase 2 → Phase 3)
- [ ] Phase 2 exercises specify only the variation points, not
      full re-instruction
- [ ] No Phase 3 (independent exercise) appears before a Phase
      1 example of the same pattern

## Feedback *(judgement)*

- [ ] Verify tells the learner what observable success looks like, not what the engine internally did
- [ ] Recovery follows a plausible failure point and names symptom → cause → fix
- [ ] The selected closure matches the evidence needed by the Section goal instead of forcing Verify + Checkpoint everywhere

## Worked example *(judgement)*

- [ ] New procedures or concepts are introduced with a complete
      worked example before the learner is asked to vary it
- [ ] Exercises modify the worked example at specific points
      (rather than asking the learner to produce from scratch)

## Expertise reversal *(judgement)*

- [ ] Signaling density, Concept presence, and narrative depth
      are scaled appropriately for the declared target learner
- [ ] Expert-facing sections (if any) use compact Reference
      tables instead of full Action sequences

## Next steps *(judgement)*

- [ ] The final top-level Section (or page end) includes
      concrete next actions with links
- [ ] No vague pointers ("公式ドキュメントを参照" without URL)

## Principles not applicable to static tutorials (video / audio / VR)

- [ ] If the artefact is narrated video, Voice / Image /
      Embodiment principles have been applied from primary
      sources (this skill does NOT cover them)
- [ ] If the artefact is VR/immersive, Immersion principle is
      addressed separately

## Limits acknowledgement

- [ ] The author has reviewed the research-limit / boundary-condition section in `SKILL.md` and understands that this checklist catches known failure modes, not universal pedagogical correctness
