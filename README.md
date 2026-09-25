# skill-tutorial-authoring

An [Agent Skills](https://agentskills.io/specification) skill for authoring step-by-step tutorials that reduce avoidable instructional overhead, manage task complexity for the target learner, and deliberately distinguish **initial performance**, **learning (including retention)**, and **transfer**. Optimised for **beginner-to-intermediate** learners.

## What it does

Research foundations used by the skill include:

- **Mayer's Cognitive Theory of Multimedia Learning** (3rd ed.; Cambridge metadata spans 2020/2021): multimedia, coherence, signaling, redundancy, spatial contiguity, temporal contiguity, segmenting, pre-training, modality, personalization, voice, image, embodiment, immersion, and generative activity
- **Cognitive Load Theory**: Sweller, van Merriënboer & Paas (2019) as the operational baseline, plus Kalyuga & Plass' 2025 goal-driven revision proposal integrating instructional goals, prior knowledge, motivation, and affect
- **Procedural instruction goals** (Eiriksdottir & Catrambone, 2011): distinguish initial performance, learning (including retention), and transfer before choosing instruction structure
- **van der Meij & Carroll's Minimalism** (1995; Carroll, 1990): action orientation, task anchoring, error support, and flexible use
- **Cromley & Chen's multimedia-learning meta-analysis** (2025): boundary conditions across principle, medium, learning outcome, age, and domain
- **Expertise reversal / adaptive assistance** (Kalyuga, 2007; Tetzlaff et al., 2025)
- **Feedback, retrieval, and distributed-practice evidence**: initial performance is not durable learning or transfer
- **Generative learning, worked examples, activation, and scaffolding**
- **WCAG 2.2** accessibility requirements relevant to tutorial content

## Progressive disclosure

The executable core is kept in `SKILL.md`. Detailed material is loaded only when needed:

- `references/research-foundations.md` — evidence, boundary conditions, citations
- `references/course-docs-platform.md` — metyatech Course Docs MDX contracts and lint
- `references/accessibility.md` — visual/text-alternative and accessibility details
- `references/video.md` — motion-based instruction and accessible video
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
- 2019 CLT operational baseline plus the 2025 goal-driven revision proposal, with boundary-condition-aware conflict resolution
- Explicit instructional horizon: initial performance, learning (including retention), transfer, or a deliberate combination
- Curriculum-level distinction among stable Learning Units, recurring Learning Events, aligned evidence, and presentation-only pages
- Initial-learning order Patterns (I-PS / PS-I) distinguished from optional Strategies and smaller teaching techniques
- Primary Representation: choose visual, code/CodePreview, text, diagram, or motion media by task and instructional horizon rather than forcing screenshots
- Meaningful segmenting and split-attention control rather than “one screen = one segment” rules
- Prior-knowledge/performance-adaptive scaffolding and worked examples
- Retrieval/generative activity separated conceptually from feedback and aligned closure
- Initial performance distinguished from durable learning and transfer
- Accessibility equivalents treated as necessary access paths, not gratuitous redundancy
- Course Docs-specific task/component contracts kept in an on-demand reference rather than generalized as learning science
- Reviewer checklist and annual research-maintenance process

## License

MIT © metyatech
