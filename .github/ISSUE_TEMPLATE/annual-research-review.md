---
name: Annual research review
about: Yearly sweep of learning-science literature feeding the tutorial-authoring skill
title: 'Annual learning-science review — YYYY'
labels: ['maintenance', 'research-review']
assignees: []
---

# Annual research review

This skill's principles, scope boundaries, and severity thresholds are
grounded in the Mayer / Sweller / Kalyuga line of research. New meta-
analyses and primary studies appear every year, so the skill must be
reviewed annually to stay current. Heuristic advisories that have
since gained empirical support can be promoted; stale assumptions can
be retired.

This issue is the canonical tracker for that review.

## Scope

Review only work that materially affects this skill:

- Multimedia learning principles (Mayer et al.) — especially new or
  revised effect sizes for Multimedia, Redundancy, Signaling,
  Personalization, Pre-training.
- Cognitive Load Theory (Sweller et al.) — intrinsic / extraneous /
  germane load, worked-example / expertise reversal effects.
- Minimalism in instructional design (Carroll line).
- Feedback / retrieval-practice literature (Shute, Karpicke) insofar
  as it touches the Verify / Recovery / Checkpoint triad.
- Culture- or language-specific findings for Japanese learners,
  especially around Personalization and tense/voice conventions.

## Checklist

### 1. New or updated sources

- [ ] Check for a new edition of Mayer's *Multimedia Learning* (3rd ed.
      was 2021). If a later edition exists, compare the principles
      table and adjust `SKILL.md` Scope & limits accordingly.
- [ ] Scan the last 12 months on Google Scholar for:
  - [ ] `author:"Richard Mayer" multimedia learning`
  - [ ] `"cognitive load theory" meta-analysis`
  - [ ] `"signaling principle" OR "pre-training principle"`
  - [ ] `multimedia learning Japanese`
- [ ] Record newly relevant DOIs / citations in this issue as
      comments, with a one-sentence takeaway each.

### 2. Skill artefact review

- [ ] Decide whether any advisory rule (note tier in remarkTutorialLint)
      now has direct empirical support, and should be promoted to
      warn. Document the supporting citation in-line.
- [ ] Decide whether any warning should be relaxed to note because
      the effect size turned out smaller than assumed.
- [ ] Adjust `ACTION_BOLD_MAX`, `CONCEPT_SENTENCE_MAX`, or any other
      numeric threshold if new evidence provides a defensible number.
- [ ] Update the principle table's *Scope & limits* column for any
      principle whose applicability changed.
- [ ] Update *Limits of principled authoring* if the research
      generalisation picture has changed (currently notes that
      Mayer's results are mostly short-form video evidence).
- [ ] Sync `REVIEW-CHECKLIST.md` if any rule moved between tiers.

### 3. Downstream propagation

- [ ] If rule severity or threshold changed, open a matching PR on
      `metyatech/course-docs-platform` to update `remark-tutorial-lint.ts`.
- [ ] If the platform changes, bump the pin in
      `metyatech/course-docs-site` package.json.

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
