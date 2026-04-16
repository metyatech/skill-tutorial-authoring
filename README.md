# skill-tutorial-authoring

An [Agent Skills](https://agentskills.io/specification) skill for authoring step-by-step tutorials that minimize cognitive load and maximize first-attempt success rate. Optimised for **beginner-to-intermediate** learners following static text-and-image tutorials.

## What it does

Provides authoring rules and component guidance derived from:

- **Mayer's Cognitive Theory of Multimedia Learning** (2009; 3rd ed. 2021): multimedia, spatial contiguity, temporal contiguity, coherence, modality, redundancy, segmenting, signaling, pre-training, personalization, split-attention
- **Sweller's Cognitive Load Theory** (1988): intrinsic, extraneous, and germane load model used as the meta-framework for resolving principle conflicts
- **van der Meij & Carroll's Minimalism** (1995; Carroll, 1990): four principles — action orientation, task anchoring, error support, flexible use
- **Kalyuga's Expertise Reversal Effect** (2007)
- **Shute's Feedback principle** (2008)
- **Mayer's Generative Activity** (2014) and **Sweller's Worked Example Effect** (1985)
- **Merrill's Activation principle** (2002)
- **Scaffolding / backward fading** (Van de Pol et al., 2010; Renkl et al., 2002)
- **WCAG 2.2 / Section 508 E205** accessibility requirements for educational materials

## Installation

```sh
npx skills add metyatech/skill-tutorial-authoring --yes --global
```

## Usage

The skill activates automatically when working on:

- Writing new step-by-step guides or tutorials
- Reorganizing or revising existing tutorials
- Auditing tutorial quality against multimedia learning theory
- Any procedural guide where a learner follows steps to build or achieve something

## Key guidance provided

- Scientific foundations table with 20 authoring principles (11 Mayer/CTML + 1 split-attention + 4 minimalism + 4 additional) and 4 noted-but-not-applicable principles
- Underlying CLT load model with conflict resolution rules
- Information hierarchy: Prerequisites → Step → Procedure → Action → Next steps
- Seven information types with display rules
- Atomic unit rules (one image per action, spatial proximity, channel separation, no redundancy)
- Accessibility authoring obligations (alt text, colour independence, contrast, semantic headings)
- Progressive independence / scaffolding (Phase 1–3 fading)
- Anti-patterns table keyed to violated principles
- Evidence-tiered mechanised lint checks (error / warn / note)
- MDX component system for [`@metyatech/course-docs-platform`](https://github.com/metyatech/course-docs-platform)
- Plain Markdown equivalents for non-component environments
- Self-review checklist (`REVIEW-CHECKLIST.md`)

## License

MIT © metyatech
