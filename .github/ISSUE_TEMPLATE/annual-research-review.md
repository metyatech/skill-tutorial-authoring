---
name: Annual research review
about: Yearly sweep of learning-science literature feeding the tutorial-authoring skill
title: 'Annual learning-science review — YYYY'
labels: ['maintenance', 'research-review']
assignees: []
---

# Annual research review

This skill's **evidence-backed principles** and their scope boundaries draw
from the Mayer / Sweller / Kalyuga line of research, including the current
two-basic-category CLT formulation and multimedia boundary-condition evidence.
Concrete rules may instead be local quality conventions, platform contracts,
or context-dependent heuristics, and must be labelled accordingly.

New meta-analyses and primary studies appear every year, so the research basis
must be reviewed annually. Lint severity is reviewed separately: stronger
research does not automatically promote a rule to `warn` or `error`; severity
depends on artefact impact and confidence that the condition can be detected
mechanically without unacceptable false positives.

This issue is the canonical tracker for that review.

## Scope

Review only work that materially affects this skill:

- Multimedia learning principles (Mayer et al.) — especially boundary conditions and moderator evidence for Multimedia, Redundancy, Signaling, Personalization, Pre-training, and active-learning interventions.
- Cognitive Load Theory (Sweller et al.) — current intrinsic / extraneous formulation, germane processing/resource-allocation interpretation, worked-example, and expertise-reversal effects.
- Minimalism in instructional design (Carroll line).
- Feedback / retrieval-practice literature insofar as it affects aligned closure choices, corrective feedback, and the distinction between immediate performance and durable learning.
- Distributed / spaced practice literature insofar as it affects what belongs at page level versus curriculum level.
- Expertise-reversal / adaptive-assistance evidence, including whether support should be retained, faded, or restored based on prior knowledge and performance.
- Accessibility guidance relevant to tutorial representations, especially text alternatives for complex annotated visuals.
- Culture- or language-specific findings for Japanese learners,
  especially around Personalization and tense/voice conventions.

## Checklist

### 1. New or updated sources

- [ ] Check for a new edition of Mayer's *Multimedia Learning* (3rd ed.
      was 2021). If a later edition exists, compare the principles
      table and adjust `SKILL.md` Scope & limits accordingly.
- [ ] Re-check Sweller, van Merriënboer & Paas (2019), "Cognitive Architecture and Instructional Design: 20 Years Later", for any superseding CLT formulation.
- [ ] Re-check Cromley & Chen (2025), "A meta-analysis of Richard Mayer's multimedia learning research", for later corrections or successor syntheses.
- [ ] Re-check Tetzlaff et al. (2025), "A cornerstone of adaptivity – A meta-analysis of the expertise reversal effect", for successor work on adaptive assistance.
- [ ] Re-check classroom retrieval / distributed-practice syntheses for evidence that changes the boundary between immediate page closure and curriculum-level retention practice.
- [ ] Scan the last 12 months on Google Scholar for:
  - [ ] `author:"Richard Mayer" multimedia learning`
  - [ ] `"cognitive load theory" meta-analysis`
  - [ ] `"expertise reversal" meta-analysis OR adaptive assistance`
  - [ ] `"retrieval practice" classroom meta-analysis`
  - [ ] `"distributed practice" classroom meta-analysis`
  - [ ] `"signaling principle" OR "pre-training principle"`
  - [ ] `multimedia learning Japanese`
- [ ] Record newly relevant DOIs / citations in this issue as
      comments, with a one-sentence takeaway each.

### 2. Skill artefact review

- [ ] Reclassify each affected rule if necessary as evidence-backed principle,
      quality convention, platform contract, or context-dependent heuristic.
      Do not present a local convention as a scientific mandate.
- [ ] Review lint severity independently from research provenance. Promote or
      demote only when artefact impact and machine-detection confidence justify
      the build effect; stronger evidence alone is not a severity upgrade.
- [ ] Review advisory numeric thresholds such as `ACTION_BOLD_MAX` and the
      Concept-length note. Keep them advisory unless both the authoring need
      and machine-detection reliability justify a harder gate.
- [ ] Update the principle table's *Scope & limits* column for any
      principle whose applicability changed.
- [ ] Update *Limits of principled authoring* if the research
      generalisation picture has changed, including media/outcome moderators,
      expertise effects, and immediate-performance versus durable-learning
      boundaries.
- [ ] Sync `REVIEW-CHECKLIST.md` if any rule moved between tiers.

### 3. Downstream propagation

- [ ] If rule severity, rule ID, or threshold changed, update `metyatech/course-docs-site/packages/platform/src/mdx/tutorial/remark-tutorial-lint.ts` and its tests in the same repository.
- [ ] If Course Docs authoring behavior changed, update `metyatech/agent-rules/rules/domains/course-docs/authoring.md`, then regenerate consuming repositories with `compose-agentsmd`; do not hand-edit generated `AGENTS.md`.

### 4. Closeout

- [ ] Summarise the year's changes in a closing comment.
- [ ] Link the closing comment to the `SKILL.md` commit that reflects
      the review.
- [ ] Close this issue. The scheduled workflow will open next year's
      issue automatically on January 1st.

## Notes

- Absence of new findings is a valid outcome; closing the issue with
  "no material change; rules retained as-is" is fine and worth
  recording so the review is not repeated mid-year.
- If a whole new principle emerges (e.g. a substantiated "immersion
  principle" finding that overlaps with existing tutorials), raise
  a follow-up Issue before closing this one.
