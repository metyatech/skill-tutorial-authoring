# skill-tutorial-authoring

An [Agent Skills](https://agentskills.io/specification) skill for authoring step-by-step tutorials that minimize cognitive load and maximize first-attempt success rate.

## What it does

Provides authoring rules and component guidance derived from:

- **Mayer's multimedia learning principles** (2009): multimedia, spatial contiguity, temporal contiguity, coherence, modality, redundancy, segmenting
- **Carroll's minimalism** (1990): start with action, learn by doing

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

- Scientific foundations table with all 8 authoring principles
- Information hierarchy: Step → Procedure → Action
- Five information types with display rules
- Atomic unit rules (one image per action, spatial proximity, no redundancy)
- Anti-patterns table keyed to violated principles
- MDX component system for [`@metyatech/course-docs-platform`](https://github.com/metyatech/course-docs-platform)
- Plain Markdown equivalents for non-component environments

## License

MIT © metyatech
