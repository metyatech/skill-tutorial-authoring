---
name: Annual research review
about: Yearly sweep of learning-science literature feeding the tutorial-authoring skill
title: 'Annual learning-science review — YYYY'
labels: ['maintenance', 'research-review']
assignees: []
---

# Annual research review

This issue is the canonical yearly tracker for reviewing the evidence-backed
principles, boundary conditions, and downstream authoring rules used by the
`tutorial-authoring` skill.

Concrete rules may be evidence-backed principles, local quality conventions,
platform contracts, or context-dependent heuristics. Reclassify them when
needed; do not present local conventions as scientific mandates.

Lint severity is reviewed independently from research provenance. Stronger
research does not automatically promote a rule to `warn` or `error`; severity
depends on artefact impact and confidence that the condition can be detected
mechanically without unacceptable false positives.

## Scope

Review only work that materially affects this skill:

- multimedia-learning principles and boundary conditions;
- Cognitive Load Theory, including goal-driven revisions, worked examples, motivation/affect, and expertise reversal;
- procedural-instruction trade-offs among initial performance, learning (including retention), and transfer;
- Learning Unit / Learning Event distinctions, constructive alignment, and course-progression evidence for recurrence over time;
- Minimalism / task-oriented instructional design;
- feedback, retrieval practice, generative learning, and durable learning;
- distributed/spaced practice where it affects page-vs-curriculum scope;
- adaptive assistance / scaffolding and fading;
- accessibility guidance relevant to tutorial representations;
- instructional-video design and accessible time-based media;
- culture/language-specific evidence relevant to Japanese learner-facing prose.

## 1. New or updated sources

- [ ] Check for a new edition of Mayer's *Multimedia Learning*. For the 3rd edition, preserve the Cambridge 2020/2021 bibliographic ambiguity rather than forcing one year unless the citation style has a defined source of record.
- [ ] Keep Mayer's *Multimedia Learning* distinct from Mayer & Fiorella's *Cambridge Handbook of Multimedia Learning* (3rd ed., 2021).
- [ ] Re-check Sweller, van Merriënboer & Paas (2019) and Kalyuga & Plass (2025) for later CLT formulations or evidence affecting the goal-driven account.
- [ ] Re-check procedural-instruction evidence on initial performance versus retention/transfer, including whether representation or fading guidance should change.
- [ ] Re-check Cromley & Chen (2025) for corrections or successor multimedia-learning syntheses.
- [ ] Re-check Tetzlaff et al. (2025) for successor expertise-reversal/adaptive-assistance evidence.
- [ ] Re-check classroom retrieval/distributed-practice syntheses for evidence that changes the boundary between page-level closure and curriculum-level learning/retention practice.
- [ ] Re-check research on PS-I/I-PS patterns, productive failure, interleaving, active learning, and transfer before changing course-progression guidance.
- [ ] Re-check educational-video design guidance and applicable WCAG time-based-media criteria.
- [ ] Re-check W3C WCAG guidance for informative and complex non-text content.
- [ ] Scan the last 12 months for relevant meta-analyses or systematic reviews on signaling, pre-training, worked examples, scaffolding, retrieval, generative activity, and software/tutorial media.
- [ ] Record newly relevant DOIs/citations in this issue with a one-sentence takeaway and population/medium limits.

## 2. Skill architecture review

Agent Skills uses progressive disclosure: the full `SKILL.md` is loaded when
the skill activates, while `references/` files are loaded only as needed.

- [ ] Keep `SKILL.md` comfortably below the Agent Skills recommendation of 500 lines / about 5,000 instruction tokens where practical.
- [ ] Keep the activation-time skill focused on executable authoring decisions rather than full literature review or platform API documentation.
- [ ] Keep reference files focused and one level deep from `SKILL.md`.
- [ ] Move detailed research rationale to `references/research-foundations.md`.
- [ ] Move Course Docs-specific component/lint contracts to `references/course-docs-platform.md`.
- [ ] Move detailed accessibility patterns to `references/accessibility.md`.
- [ ] Keep progressive-disclosure video guidance in `references/video.md`.
- [ ] Confirm every reference linked by `SKILL.md` exists and is still needed.

## 3. Skill artefact review

- [ ] Reclassify each affected rule as evidence-backed principle, quality convention, platform contract, or context-dependent heuristic.
- [ ] Review lint severity independently from research provenance.
- [ ] Review advisory numeric thresholds such as bold density and Concept length; keep them advisory unless both impact and machine confidence justify a harder gate.
- [ ] Check for accidental conversion of a software-tutorial heuristic into the literal statement of a research principle (for example, “one screen = one segment”).
- [ ] Check that expertise reversal is applied to forms of assistance rather than claimed as a universal reversal of every multimedia principle.
- [ ] Check that retrieval, generative activity, feedback, and aligned closure remain conceptually distinct.
- [ ] Check that the skill distinguishes initial performance, learning (including retention), and transfer before selecting representation, support, or closure.
- [ ] Check that Learning Units, Learning Events, aligned evidence, and pages-as-presentation are still distinct and do not imply an unimplemented platform API.
- [ ] Check that initial performance is not described as durable learning or transfer.
- [ ] Check that visual-primary Actions are judged as a complete action unit rather than requiring visible prose to duplicate the full visual procedure.
- [ ] Check that accessibility-equivalent content is not removed as gratuitous redundancy.
- [ ] Check that Section 508 language is limited to applicable U.S. federal ICT scope rather than presented as universal law.
- [ ] Update `REVIEW-CHECKLIST.md` when the executable core or reviewer-facing semantics change.
- [ ] Update `README.md` when the skill architecture, scope, or primary research framing changes.

## 4. Course Docs downstream propagation

- [ ] Compare `references/course-docs-platform.md` against the live `metyatech/course-docs-site/packages/platform` source/tests so copied lint IDs and severities do not drift.
- [ ] If a Course Docs platform contract, lint rule ID, severity, threshold, or parser structure changes, update `metyatech/course-docs-site/packages/platform` and its tests.
- [ ] If Course Docs authoring behavior changes, update `metyatech/agent-rules/rules/domains/course-docs/authoring.md`.
- [ ] Regenerate consuming repositories with `compose-agentsmd --refresh`; do not hand-edit generated `AGENTS.md`.
- [ ] If only generic research rationale changes and Course Docs behavior does not, do not create unnecessary downstream churn.

## 5. Validation

- [ ] Verify `SKILL.md` frontmatter still satisfies the Agent Skills specification.
- [ ] Verify the installed skill directory name matches `name: tutorial-authoring` (the package/repository name may differ from the installed skill directory name).
- [ ] Verify all relative reference links resolve.
- [ ] Run available skill validation tooling when practical; if `skills-ref` is unavailable, record that and perform equivalent structural checks.
- [ ] Run `git diff --check` before delivery.

## 6. Closeout

- [ ] Summarise the year's material changes and “no change” findings in a closing comment.
- [ ] Link the closing comment to the `SKILL.md` commit that reflects the review.
- [ ] Link any downstream Course Docs/agent-rules commits if behavior changed.
- [ ] Close this issue. The scheduled workflow will open next year's issue automatically on January 1st.

## Notes

- Absence of new findings is a valid outcome. Record “no material change; rules retained as-is” rather than silently skipping review.
- When new evidence conflicts with an existing heuristic, update the heuristic and its provenance instead of preserving it for consistency alone.
