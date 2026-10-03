---
name: qingyv-video-workflow
description: Analyze reference videos and turn product ideas into expressive, frame-driven motion films with evidence-based observation, motion direction, implementation, and validation. Use for reference recreation, style transfer, product reels, UI motion films, or diagnosing animation that feels static, slow, or unclear.
---

# Qingyv Video Workflow

Build motion that explains something. Treat the reference as evidence, the product as truth, and animation as a sequence of meaningful state changes.

## Choose the mode

- **Reference recreation:** preserve the source timing, composition, amplitude, morphing, occlusion, and rhythm as closely as editable assets allow.
- **Style transfer or original film:** preserve the product's real function and borrow only the reference's motion language. Redesign the shots for the new content.

Do not mix the two standards. Pixel similarity is useful for recreation and usually irrelevant to an original product film.

## Use the core chain

Define each shot as:

`purpose -> expression verb -> initial state -> motion process -> result -> handoff`

The motion must make the purpose visible. A caption cannot rescue an unrelated abstract animation.

## Route the work

1. Establish the target, audience, duration, delivery surface, source truth, and exclusions.
2. If a reference exists, read [reference observation](references/observation.md). Build a sparse scene map, then inspect fast or ambiguous passages at source frame rate.
3. For shot design, amplitude, morphing, timing, or rhythm, read [motion direction](references/motion-direction.md).
4. Implement with deterministic frame-driven state. Keep position, scale, opacity, shape, camera, and text on independent tracks when the expression needs it.
5. Before delivery, read [production and validation](references/production-and-validation.md). Check representative states, dense transitions, the complete encode, and the real integration surface.
6. Use [working templates](references/templates.md) for shot cards, observation notes, and validation reports. For long or interruption-prone work, use [project memory](references/project-memory.md).

## Preserve these invariants

- A 0.5-second contact sheet is an overview, not proof of what happens between samples.
- Inspect morphs, occlusions, flashes, flips, fast zooms, cuts, and uncertain order with consecutive source frames.
- Separate internal deformation, whole-object motion, and camera motion.
- Use measured values for boundaries and extrema; label creative inference as inference.
- A still-looking interval may be a deliberate reading window. Unmotivated jitter does not replace meaningful change.
- Do not use the source video or full-frame captures as the reconstructed output.
- Distinguish implemented, rendered, technically verified, visually compared, and user accepted.
- Preserve user scope and authorization. Research or analysis does not authorize publishing, deployment, or other external writes.

The methods borrow useful concepts from timeline, SVG, curve-editing, and shape-animation tools without requiring those libraries. See [method sources](references/sources.md) when attribution or engine selection matters.
