# Image Editing and Synthesis

Use this module to plan identity-preserving edits, local replacements, style conversion, or multi-source compositing.

## Establish an edit contract

Before writing an edit instruction, identify:

- the exact target region or property;
- its current and desired state;
- invariants that must remain unchanged;
- geometry, perspective, material, lighting, and edge conditions at the boundary;
- forbidden spillover into unrelated regions;
- ambiguities or conflicts that could cause regeneration drift.

Keep the edit prompt centered on the delta. Do not redescribe and regenerate the whole image when a local change is requested.

## Identity preservation

Record the smallest sufficient identity specification: silhouette, proportions, face or focal structure, distinctive components, clothing or product features, palette, material, and signature marks. Separate invariant identity from pose, expression, camera, and environment variables.

## Style conversion

Split the source into content and style layers. Preserve source identity and composition unless the user permits changes. Translate target style through observable features such as abstraction, geometry, line, edge, color grouping, material, shading, texture, and detail density. Do not import the target reference's subject identity or unrelated content.

## Multi-source compositing

Assign each source a declared contribution. Specify final position, scale, depth, overlap, pose, gaze, light direction, perspective, and background integration. Check for identity blending, duplicated elements, clothing or component swaps, scale mismatch, inconsistent lighting, and impossible occlusion.

## Execution boundary

An edit plan or prompt is not permission to edit the image. Use an editing tool only when the user explicitly asks to perform the edit. When executing, include every target image through the tool's supported reference mechanism and preserve transparency when relevant.
