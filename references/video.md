# Video authoring reference

Load this reference when video or animation is a primary teaching
representation. Video is appropriate when motion, timing, or continuous change
is important to understanding or performing the task. Prefer text, code, still
images, or diagrams when they communicate the same operation with less effort
or more precision. There is no fixed minimum or maximum video length; choose
boundaries around meaningful sub-goals and learner-managed chunks.

## Instructional design

- Preserve learner control: provide usable play/pause, seek, replay, and volume
  controls; offer playback-speed control when the player supports it. Avoid
  requiring a learner to keep pace with a one-pass demonstration.
- Signal the goal-relevant object, action, or change with a concise label,
  highlight, or narration. Keep signals tied to the task and visually distinct
  from decoration.
- Segment a complex or extended process at meaningful state or sub-goal
  boundaries. Use chapter markers or separate clips where useful; do not split
  mechanically at a fixed duration.
- Synchronize narration with corresponding visual changes when learners need
  to integrate both. Keep on-screen labels near the item or action they explain.
- Remove motion, music, sound effects, and visual effects that do not support
  the objective. Motion should explain a dynamic process, state transition,
  timing, or gesture rather than decorate the page.
- Keep exact commands, code, paths, settings, and other values in accessible
  text so learners can scan, copy, compare, and use them without replaying the
  video. Provide a text explanation of the essential action and outcome.

## Accessibility

- For prerecorded synchronized media with audio, provide synchronized captions
  for speech and meaningful sounds. A transcript is useful for scanning and
  reference, but does not replace captions when synchronized captions are
  required.
- Make a transcript or audio description available when essential visual
  information is not conveyed by the audio. WCAG 2.2 requires a descriptive
  transcript or audio description for prerecorded video-only content at Level
  A, a media alternative or audio description for synchronized media at Level
  A, and audio description for prerecorded synchronized media at Level AA.
  If the audio already conveys all essential visual information, additional
  description is not needed for that purpose.
- Ensure player controls and interactive captions/transcripts can be operated
  with a keyboard and expose understandable names and states. Check that focus
  order is usable and keyboard users can leave the player.
- Give learners control of automatically moving media. WCAG 2.2 SC 2.2.2
  requires a pause/stop/hide mechanism for automatically moving content that
  lasts more than five seconds while presented alongside other content, unless
  the movement is essential. This skill's learner-control convention is
  broader: make instructional video controllable even where a specific WCAG
  threshold does not apply.
- Do not rely on colour, sound, or motion alone to communicate a necessary
  distinction. Respect reduced-motion preferences in the player/page when
  applicable, and avoid gratuitous motion.

These are content-authoring requirements and accessibility review prompts. The
player implementation and its conformance remain platform responsibilities.

## Evidence and sources

Brame's review of educational-video research organizes guidance around managing
cognitive load, supporting engagement, and promoting active learning. Signaling
and meaningful segmenting can help learners attend to and process complex video
material; they are design supports, not requirements for every clip. Apply
multimedia principles within their stated boundary conditions rather than
assuming a video format guarantees learning.

- Brame, C. J. (2016). *Effective Educational Videos: Principles and
  Guidelines for Maximizing Student Learning from Video Content*.
  https://doi.org/10.1187/cbe.16-03-0125
- W3C, *Web Content Accessibility Guidelines (WCAG) 2.2*:
  https://www.w3.org/TR/WCAG22/
- W3C WAI, *Captions/Subtitles*:
  https://www.w3.org/WAI/media/av/captions/
- W3C WAI, *Description of Visual Information*:
  https://www.w3.org/WAI/media/av/description/
- W3C WAI, *Keyboard Accessibility*:
  https://www.w3.org/WAI/fundamentals/accessibility-principles/keyboard/
