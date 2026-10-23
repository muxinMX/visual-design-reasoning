# Composition and Motion

Use this module for framing, camera, spatial organization, poses, group scenes, lighting, and image-to-video action planning.

## Composition and camera

Reason from intended visual effect to spatial choices:

- frame ratio and subject occupancy;
- camera height, angle, distance, and plausible focal-length range;
- horizon, vanishing directions, depth layers, and scale cues;
- visual path, balance, asymmetry, negative space, and focal hierarchy;
- overlap, cropping, foreground framing, and separation;
- pose direction and force lines relative to the frame.

Treat exact lens and camera values inferred from an image as estimates unless metadata is available.

## Group composition

Assign every subject a position, scale, depth layer, pose, gaze, and interaction. Use overlap and body orientation to express relationships while retaining recognition. Avoid evenly spaced lineups unless that is the intended graphic device.

## Pose and physical logic

Define action purpose, contact points, center of mass, support, force, counterbalance, joint range, silhouette, gaze, and secondary motion. Check whether body proportions, clothing, props, or product mechanics restrict the requested action.

## Lighting and atmosphere

Specify only layers that matter:

- key-light direction, size, softness, and color;
- fill level, environment contribution, rim or practical lights;
- value grouping, contrast, focal emphasis, and material readability;
- temperature relationships, haze, volume, reflection, and mood.

When the user asks only for lighting changes, preserve subject identity, geometry, layout, camera, and untouched areas.

## Animation or image-to-video

Build a short action with a readable arc:

1. preparation or anticipation;
2. initiation and force;
3. main action;
4. follow-through or recovery;
5. final hold.

Describe timing, center-of-mass change, arcs, inertia, facial and gaze response, hands or contact, camera behavior, and continuity constraints. Prefer one coherent action over a list of simultaneous gestures.

Do not produce a final prompt unless the current stage permits it; pass confirmed specifications to `prompt-generation.md`.
