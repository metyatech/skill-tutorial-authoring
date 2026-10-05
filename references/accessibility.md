# Accessibility reference for tutorial authoring

Load this reference when a tutorial contains informative images, annotated
screenshots, diagrams, charts, video/GIF, or interactive examples.

The default authoring target for this skill is **WCAG 2.2 Level AA**.
U.S. Section 508 E205 is relevant when the content falls within U.S. federal
ICT scope; it is not a universal legal requirement for every private or public
tutorial.

## Non-text content

WCAG 2.2 SC 1.1.1 applies to informative non-text content generally, not only
images placed inside a particular component.

For every informative visual, ask:

> If the learner could not perceive this visual, what information or function
> would they still need in order to complete or understand the task?

Provide that equivalent through `alt`, surrounding text, a long description,
structured data, or another programmatically associated mechanism as
appropriate.

Decorative visuals should use the platform's decorative-image treatment, such
as `alt=""` when HTML `<img>` semantics apply.

## Short versus complex alternatives

### Simple informative image

Use concise alt text that communicates the image's purpose or essential
information rather than describing irrelevant appearance.

Examples:

- Better: `alt="Settings menu with Network selected"`
- Poor: `alt="screenshot"`
- Poor: `alt="image of a computer screen"`

### Complex annotated screenshot, diagram, or chart

Do **not** cram a complete procedure, graph dataset, or multi-part relationship
into one oversized alt string.

Use a two-part approach:

1. a concise short alternative identifying purpose/subject;
2. a detailed equivalent in adjacent learner-visible content or another long
   description mechanism.

W3C's Complex Images tutorial explicitly recommends this short + long model for
content whose essential information cannot fit in a short phrase or sentence.

The detailed description may be learner-visible. This is often preferable
because it helps more than only screen-reader users.

## Accessibility equivalents and redundancy

An accessibility-equivalent path is **not** gratuitous redundancy merely because
the same essential procedure also appears visually.

The redundancy concern in tutorial design is forcing learners to process two
competing complete instructional paths without benefit. Accessibility sometimes
requires the same essential information to exist in another modality or text
form.

Design goal:

- preserve a complete equivalent route;
- avoid making every learner repeatedly process two full parallel procedures
  when the platform can expose the equivalent programmatically or on demand;
- retain short labels/cues in both representations when they improve mapping.

## Annotated screenshots

When a screenshot uses numbered circles, arrows, boxes, or highlights:

- do not rely on colour alone for sequence or state (WCAG SC 1.4.1);
- pair colour with number, shape, label, line style, or another cue;
- ensure annotation text meets text contrast requirements;
- ensure meaningful non-text graphical objects meet non-text contrast where
  applicable;
- provide a text-equivalent route for the information encoded only by the
  annotation layout.

A visual-primary ①→②→③→④ interaction path may therefore need a textual
procedure for accessibility even when duplicating it visibly in body prose
would be unnecessary for the primary sighted path.

## Contrast

For WCAG 2.2 AA:

- normal text and images of text: at least **4.5:1** (SC 1.4.3);
- large text: at least **3:1**;
- meaningful non-text UI components and graphical objects: **3:1** where
  SC 1.4.11 applies.

Do not incorrectly use the 3:1 non-text threshold for ordinary annotation text.

## Images of text

Prefer real text to images of text when equivalent visual presentation can be
achieved with real text (WCAG SC 1.4.5), subject to its exceptions.

This does not ban screenshots containing UI text. A screenshot of software is
not automatically an avoidable “image of text” merely because the UI contains
labels.

## Code and diagrams

For code-primary instruction, keep the code available as real text rather than
using a screenshot of source code when possible.

For structural diagrams:

- expose the nodes/relationships textually when they are essential;
- preserve meaningful ordering/hierarchy in the detailed description;
- do not rely on spatial position or colour alone to communicate semantics.

## Motion media

Video is within the tutorial-authoring scope. For detailed guidance on when
motion helps, learner control, signaling, segmenting, synchronization, captions,
transcripts, audio description, and keyboard-accessible controls, load
[`video.md`](video.md). Keep exact values/commands in accessible text and
provide an equivalent explanation of the essential action/outcome.

## Interactive examples

Interactive examples must be usable with a keyboard in a logical order and must
not require pointer-only gestures without an equivalent method.

### Dynamic reading, focus, and status

When content order affects meaning, keep a meaningful programmatic reading
sequence. When keyboard focus order affects meaning or operation, preserve a
logical focus sequence. Keep those orders aligned with the visual sequence
where their relationship carries meaning; they do not have to be identical
when more than one sequence remains understandable and operable. See WCAG 2.2
SC 1.3.2 Meaningful Sequence and SC 2.4.3 Focus Order.
W3C technique [C27](https://www.w3.org/WAI/WCAG21/Techniques/css/C27)
describes matching DOM and visual order when needed; documented techniques are
examples of ways to meet WCAG, not mandatory layouts.

For sequential dynamic tutorials, place newly revealed instructional content
at or after its triggering action in the meaningful reading/focus order when
that helps the learner follow the transition. W3C technique SCR26 describes
inserting dynamic content immediately after its trigger as one technique; it is
an example, not a universal WCAG requirement. If an action updates a status
message without moving focus, ensure applicable status is programmatically
available to assistive technology under WCAG 2.2 SC 4.1.3. W3C's `role=status`
technique is one example, not the only conforming implementation.

### Native response semantics and motion

For an interactive single-line response with one primary submit/confirm action,
prefer native form/submit semantics where applicable so Enter and the visible
submit control invoke identical validation and state transitions. The HTML
Standard describes implicit form submission and strongly encourages user-agent
support. This is platform and usability guidance, not a learning-science
finding. Do not apply it to multiline inputs or controls whose standard
keyboard behavior differs. Avoid
custom Enter handlers that submit during IME composition unless composition is
explicitly handled.

Respect reduced-motion preferences. W3C Technique SCR40 describes using the CSS
`prefers-reduced-motion` query to prevent motion; this is an example technique,
not a blanket WCAG requirement. Keep a state/result cue available without
motion, and do not reduce text or UI contrast during a transition.

The platform, not the tutorial author alone, owns many implementation details
such as focus states and semantics. The author remains responsible for choosing
content and labels that make the interaction understandable.

## Course Docs image props

When Course Docs components expose `img` and `alt` props, treat them as one
implementation route for the general accessibility obligations above. Do not
infer that Action/Verify are the only places where informative visuals need text
alternatives.

For a simple Action/Verify image, concise `alt` may be sufficient. For a complex
annotated visual, keep `alt` short and put the detailed equivalent in learner-
visible prose or another supported long-description mechanism.

## References

- W3C, WCAG 2.2: https://www.w3.org/TR/WCAG22/
- W3C WAI, Understanding SC 1.1.1 Non-text Content:
  https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html
- W3C WAI, Complex Images:
  https://www.w3.org/WAI/tutorials/images/complex/
- W3C WAI, Understanding SC 1.3.2 Meaningful Sequence:
  https://www.w3.org/WAI/WCAG22/Understanding/meaningful-sequence.html
- W3C WAI, Understanding SC 2.4.3 Focus Order:
  https://www.w3.org/WAI/WCAG22/Understanding/focus-order.html
- W3C WAI, Understanding SC 4.1.3 Status Messages:
  https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html
- W3C WAI Technique SCR26 (dynamic content after its trigger):
  https://www.w3.org/WAI/WCAG22/Techniques/client-side-script/SCR26
- W3C WAI Technique ARIA22 (status messages):
  https://www.w3.org/WAI/WCAG22/Techniques/aria/ARIA22
- W3C WAI Technique SCR40 (reduced motion):
  https://www.w3.org/WAI/WCAG22/Techniques/client-side-script/SCR40
- WHATWG, HTML Standard, implicit form submission:
  https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#implicit-submission
- W3C WAI, Technique G94 (short text alternative serving the same purpose):
  https://www.w3.org/WAI/WCAG22/Techniques/general/G94
- U.S. Access Board, Revised 508 Standards:
  https://www.access-board.gov/ict/
