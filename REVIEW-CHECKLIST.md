# Tutorial self-review checklist

Use this list when auditing a draft tutorial against every
principle encoded in `SKILL.md`. Items marked *(auto)* are
already enforced by `remarkTutorialLint` at build time; items
marked *(judgement)* require human review.

Work top-down: structural items first, then each principle in
the order it appears in the Scientific foundations table.

## Structure *(auto where marked)*

- [ ] Every `<Section>` declares a `goal` *(auto)*
- [ ] Goal is written in future-declarative form *(auto)*
- [ ] Exactly one `<Checkpoint>` per top-level Section, placed last *(auto)*
- [ ] Page frontmatter declares `authoringMode: 'tutorial'` for tutorial pages *(auto)*
- [ ] No `---` horizontal rules inside a Section *(auto)*
- [ ] Every `<Action>` has at most one image *(auto)*
- [ ] No `<Action>` body begins with a positional prefix that
      the image already conveys *(auto)*
- [ ] `<Verify>` body does not start with a literal `→` *(auto)*
- [ ] No `<Reference>` whose only content is an image *(auto)*

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

## Multimedia / Channel separation *(judgement)*

- [ ] Every operational step has a corresponding image
- [ ] Image carries WHERE (position, sequence, callouts)
- [ ] Text carries WHAT (imperative verb + values the image
      cannot convey)
- [ ] Typed values, user-specific paths, and gestures/motions
      are present in text
- [ ] UI labels clearly visible in the shot are NOT repeated in
      bold in the text

## Spatial / Temporal contiguity *(judgement)*

- [ ] Each image is directly adjacent to its corresponding
      text, not batched upstream
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

- [ ] No text restates information the image already shows
- [ ] No settings table duplicates numbered-callout pairs
      row-for-row
- [ ] No micro-interaction description that an arrow already
      conveys (unless motion cannot be encoded in a still)

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

- [ ] Recovery is present after every action that can plausibly
      fail
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
      (UI names not in image, typed values, key gestures)
- [ ] No sentence contains three or more bold spans
- [ ] Numbered callouts in images are matched by ①②③ in text
      (complementary, not redundant)
- [ ] No decorative bold/highlight for emotional emphasis

## Pre-training *(judgement)*

- [ ] Each Concept sits immediately before the Section that
      first uses the term
- [ ] No Concept introduces a term that appears much later on
      the page
- [ ] Each Concept is ≤ 5 sentences and answers both "what is
      it?" and "why need to know now?"

## Activation *(judgement)*

- [ ] New concepts include an analogy or bridge to something
      the learner already knows (where a plausible prior-
      knowledge anchor exists)
- [ ] Activation is distinct from Pre-training: it recalls
      existing knowledge, not introduces new terms

## Personalization *(judgement)*

- [ ] Prose addresses the reader in second person (「〜しましょう」
      「確認してください」)
- [ ] No third-person description of the reader ("受講者が〜",
      "学習者は〜", "初学者向け")
- [ ] No page opens by describing what the document is or who
      it is for
- [ ] Friendliness stays at "senior peer teaching next to you"
      level (no emoji spam, no 余談, no 感情過剰)

## Accessibility *(judgement)*

- [ ] Every `<Action>` image has an `alt` prop describing the
      WHERE information (panel, button, area)
- [ ] Callouts and highlights use shape + colour, not colour
      alone
- [ ] Image-only meaning is recovered in nearby text
- [ ] Text annotations on screenshots meet 3:1 contrast ratio
- [ ] Heading hierarchy is semantic (`h2` → `h3`)

## Generative activity *(judgement)*

- [ ] Every Section containing Actions ends with a Verify
      stating an observable state (not internal mechanics)
- [ ] Every top-level Section ends with a Checkpoint of
      observable behaviours the learner can self-confirm
- [ ] Exercises (if any) tie directly to the containing
      top-level Section's goal
- [ ] Optional prediction prompts appear at most once per
      top-level Section

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

- [ ] Verify tells the learner what success looks like, not
      what the engine did
- [ ] Recovery is present after every action that can
      plausibly fail, and names the failure symptom before the
      fix
- [ ] Checkpoint allows the learner to confirm top-level
      Section success independently

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

- [ ] The author has reviewed "Limits of principled authoring"
      in `SKILL.md` and understands that this checklist
      catches known failure modes, not pedagogical correctness
