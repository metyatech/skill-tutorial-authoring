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
- [ ] Exactly one `<Checkpoint>` per Step, placed last *(auto)*
- [ ] No `---` horizontal rules inside a Section *(auto)*
- [ ] Every `<Action>` has at most one image *(auto)*
- [ ] No `<Action>` body begins with a positional prefix that
      the image already conveys *(auto)*
- [ ] `<Verify>` body does not start with a literal `→` *(auto)*
- [ ] No `<Reference>` whose only content is an image *(auto)*

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

## Minimalism *(judgement)*

- [ ] The first Action appears early; no long front-loaded
      prose
- [ ] No reference tables or long Concepts appear before the
      first Action of the Step

## Signaling *(judgement)*

- [ ] Bold emphasis is used only on learning-objective elements
      (UI names not in image, typed values, key gestures)
- [ ] No sentence contains three or more bold spans
- [ ] Numbered callouts in images are matched by ①②③ in text
      (complementary, not redundant)
- [ ] No decorative bold/highlight for emotional emphasis

## Pre-training *(judgement)*

- [ ] Each Concept sits immediately before the Procedure that
      first uses the term
- [ ] No Concept introduces a term that appears much later on
      the page
- [ ] Each Concept is ≤ 5 sentences and answers both "what is
      it?" and "why need to know now?"

## Personalization *(judgement)*

- [ ] Prose addresses the reader in second person (「〜しましょう」
      「確認してください」)
- [ ] No third-person description of the reader ("受講者が〜",
      "学習者は〜", "初学者向け")
- [ ] No page opens by describing what the document is or who
      it is for
- [ ] Friendliness stays at "senior peer teaching next to you"
      level (no emoji spam, no 余談, no 感情過剰)

## Generative activity *(judgement)*

- [ ] Every Procedure ends with a Verify stating an observable
      state (not internal mechanics)
- [ ] Every Step ends with a Checkpoint of observable
      behaviours the learner can self-confirm
- [ ] Exercises (if any) tie directly to the Step's goal
- [ ] Optional prediction prompts appear at most once per Step

## Feedback *(judgement)*

- [ ] Verify tells the learner what success looks like, not
      what the engine did
- [ ] Recovery is present after every action that can
      plausibly fail, and names the failure symptom before the
      fix
- [ ] Checkpoint allows the learner to confirm Step-level
      success independently

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

## Out-of-scope principles (video / audio / VR)

- [ ] If the artefact is narrated video, Voice / Image /
      Embodiment principles have been applied from primary
      sources (this skill does NOT cover them)
- [ ] If the artefact is VR/immersive, Immersion principle is
      addressed separately

## Limits acknowledgement

- [ ] The author has reviewed "Limits of principled authoring"
      in `SKILL.md` and understands that this checklist
      catches known failure modes, not pedagogical correctness
