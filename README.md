# skill-tutorial-authoring

An [Agent Skills](https://agentskills.io/specification) skill for authoring step-by-step tutorials that reduce avoidable instructional overhead, manage task complexity for the target learner, support successful task completion, and promote durable learning and transfer. Optimised for **beginner-to-intermediate** learners.

## What it does

Research foundations used by the skill include:

- **Mayer's Cognitive Theory of Multimedia Learning** (2009; 3rd ed. 2020): multimedia, contiguity, coherence, modality, redundancy, segmenting, signaling, pre-training, personalization, embodiment, immersion, and generative activity
- **Sweller, van Merriënboer & Paas' Cognitive Load Theory update** (2019): intrinsic and extraneous load as the basic categories, with germane processing treated as working-memory resource allocation toward learning-relevant intrinsic processing
- **van der Meij & Carroll's Minimalism** (1995; Carroll, 1990): action orientation, task anchoring, error support, and flexible use
- **Cromley & Chen's multimedia-learning meta-analysis** (2025): boundary conditions across principle, medium, learning outcome, age, and domain
- **Expertise reversal / adaptive assistance** (Kalyuga, 2007; Tetzlaff et al., 2025)
- **Feedback, retrieval, and distributed-practice evidence**: immediate performance is not durable mastery
- **Generative learning, worked examples, activation, and scaffolding**
- **WCAG 2.2** accessibility requirements relevant to tutorial content

## Progressive disclosure

The executable core is kept in `SKILL.md`. Detailed material is loaded only when needed:

- `references/research-foundations.md` — evidence, boundary conditions, citations
- `references/course-docs-platform.md` — metyatech Course Docs MDX contracts and lint
- `references/accessibility.md` — visual/text-alternative and accessibility details
- `REVIEW-CHECKLIST.md` — full reviewer-facing audit

This follows the Agent Skills specification's progressive-disclosure model rather than loading every research and platform detail into the activation-time skill body.

## Installation

```sh
npx skills add metyatech/skill-tutorial-authoring --yes --global
```

The installer places the skill under the `tutorial-authoring` skill name used by the `SKILL.md` frontmatter.

## Usage

The skill activates automatically when working on:

- writing new step-by-step guides or tutorials;
- reorganizing or revising existing tutorials;
- auditing tutorial quality against evidence-informed instructional design;
- procedural guides where a learner follows steps to build, configure, understand, or practice something.

## Key guidance

- Explicit separation of evidence-backed principles, local quality conventions, platform contracts, and context-dependent heuristics
- Current CLT framing and boundary-condition-aware conflict resolution
- Primary Representation: choose visual, code/CodePreview, text, diagram, or motion media by task rather than forcing screenshots
- Meaningful segmenting and split-attention control rather than “one screen = one segment” rules
- Prior-knowledge/performance-adaptive scaffolding and worked examples
- Retrieval/generative activity separated conceptually from feedback and aligned closure
- Immediate performance distinguished from durable mastery
- Accessibility equivalents treated as necessary access paths, not gratuitous redundancy
- Course Docs-specific task/component contracts kept in an on-demand reference rather than generalized as learning science
- Reviewer checklist and annual research-maintenance process

## License

MIT © metyatech
