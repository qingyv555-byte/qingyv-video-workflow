# Production and validation

## Implement deterministic time

Drive every visual state from frame number or an equivalent deterministic timeline. In Remotion, derive local scene time from `useCurrentFrame()` and composition metadata. Avoid wall-clock timers, CSS autoplay animation, playback-position side effects, or randomness without a fixed seed.

Build each shot from explicit states. Keep reusable interpolation, easing, and layer primitives small. Preserve previous versions when a new motion pass changes timing or structure materially.

## Treat sound as a motion layer

Plan sound with the picture. Mark preparation, impact, transition, and result moments. Verify that the soundtrack belongs to the project and do not present synthetic or illustrative audio as a product's real output.

## Validate in increasing cost

1. **Representative stills:** render the start, maximum extent, operation, result, and transition of each shot. Check cropping, text, overlap, hierarchy, and composition.
2. **Dense transition strips:** inspect consecutive output frames around fast motion, morphs, occlusion, cuts, and handoffs. A few attractive stills do not prove continuous motion.
3. **Same-time comparison:** for recreation, compare source and output at identical timestamps for boundaries, extrema, turning points, and complex intervals.
4. **Full playback:** watch at normal speed with audio, then slow down suspicious passages. Judge rhythm, reading windows, and continuity.
5. **Media verification:** check resolution, duration, frame rate, frame count, audio streams, and full decode. Run the project's type and build checks.
6. **Integration verification:** if the video belongs in an app or site, verify the actual path, metadata, cover, chapters, controls, responsive layout, and reduced-motion behavior in the real surface.

Frame difference, bounding boxes, centroids, MAE, or SSIM can locate problems. They cannot prove aesthetic quality or faithful motion, and their meaning depends on correct segmentation.

## Report status precisely

Track these states separately:

- implemented in source;
- rendered to media;
- technically verified;
- visually compared;
- integrated into the destination;
- accepted by the user.

Document remaining differences in assets, fonts, topology, perspective, material, timing, or motion. Do not describe a successful render as a precise recreation.
