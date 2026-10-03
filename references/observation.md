# Reference observation

Use a two-resolution viewing method: a sparse map for the whole piece, then dense evidence only where motion cannot be inferred safely.

## 1. Establish source truth

Record duration, resolution, frame rate, frame count, audio presence, and the exact segment in scope. Use timestamps or presentation timestamps rather than assuming file order equals time.

## 2. Build a 0.5-second overview

Create timestamped contact sheets sampled every 0.5 seconds. Use roughly 6–12 cells per sheet and thumbnails large enough to read the dominant composition. The overview should identify:

- shot boundaries and background changes;
- the dominant subject and attention path;
- major text states and result landings;
- candidate transitions that need dense inspection.

This pass is a scene map. It cannot reveal the path, acceleration, overlap, or ordering between two samples.

## 3. Inspect dense intervals

Review consecutive frames at the source frame rate around:

- morphing or internal topology changes;
- occlusion, masking, or layer swaps;
- flashes, flips, fast zooms, impacts, and cuts;
- digits or labels changing out of sync with the scene;
- any interval whose order or amplitude is uncertain.

Example: ten seconds at 23.976 fps contains about 240 frames. A compact review can use 20 contact sheets with 12 consecutive frames each, so every sheet covers about 0.5 seconds while retaining the actual frame sequence.

Use native-resolution crops for small text, thin lines, edges, or control-point questions. Continuous playback and slow playback remain necessary for perceived smoothness and audio rhythm.

## 4. Record layers and extrema

Track background, main subject, support graphics, text, occlusion, camera, and sound separately. For each important element record:

- start, maximum amplitude, turning point, and endpoint;
- bounding box and position as percentages of the frame;
- rotation, scale, opacity, shape controls, and layer order;
- what was measured directly and what was inferred.

Do not force asynchronous events into one scene index. Text, background, numbers, and shapes often change on different frames.

## 5. Spend context deliberately

Keep source media, sheets, measurements, and notes on disk. Load only the sheet or crop needed for the current decision. Local frame-difference scans can suggest candidate intervals, but they favor flashes and color changes and cannot identify meaning or prove that every important transition was found.

Combining images into sheets reduces image count and comparison overhead. Do not claim a token-saving percentage without actual measurement.
