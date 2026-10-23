# Prompt Generation

Use this module when the user directly requests a prompt, asks to convert an established design into a prompt, asks to optimize an existing prompt, or the current stage explicitly permits prompt output. A prior analysis, exploration, or approval stage is not required.

## Build from the available brief

Use the user's current brief first, then any confirmed decisions and project constraints. When important details are absent but a useful prompt is still possible, make restrained, style-neutral assumptions and proceed. Ask only when the missing choice would materially change the result.

For a sparse brief, keep unspecified theme, genre, era, mood, and world premise neutral. Do not silently lock the work into ecological futurism, cyberpunk, post-apocalyptic, retro, or another specific direction. If a key creative assumption is needed to make the prompt usable, label it briefly and ensure it supplements rather than replaces or narrows the user's stated requirements. This does not add a required discussion step: when the user asks directly for a prompt, deliver the prompt from the available information.

Prefer concrete, controllable visual information. Include only relevant fields:

- output type and intended use;
- subject identity and invariants;
- action, pose, interaction, or functional state;
- composition, viewpoint, camera, and spatial relationships;
- environment and supporting elements;
- shape, style, color, material, lighting, and atmosphere;
- edit delta or motion timeline when applicable;
- exclusions and preservation constraints;
- tool-specific syntax or parameters that are known and requested.

Do not invent unsupported parameters, imply deterministic control, or add unrequested tool syntax. If the target tool is unspecified, produce a tool-neutral prompt. Offer tool adaptation only when it would materially help.

## Prompt forms

Choose the smallest form that serves the request:

- **Direct prompt:** one ready-to-use prompt.
- **Detailed specification:** structured prompt for complex control.
- **Compact prompt:** reduced wording with the same essential controls.
- **Edit prompt:** target change plus preservation constraints.
- **Video prompt:** shot continuity and timed action arc.
- **Optimized prompt:** a corrected or compressed version of an existing prompt that preserves its intent.

When optimizing an existing prompt, first identify contradictions, vague language, missing spatial relationships, redundant detail, and conflicts among style, material, lighting, or motion. Preserve confirmed creative intent.

Use [../templates/image-prompt.md](../templates/image-prompt.md) for complex image generation or edit prompts and [../templates/video-prompt.md](../templates/video-prompt.md) for complex motion prompts. Do not load or reproduce a template when a short direct prompt is sufficient.

## Ordering

Put the dominant subject and action early, then composition and environment, then visual treatment and constraints. Keep related information together. Avoid adjective piles, duplicated modifiers, and exhaustive camera jargon that does not change the image.

Never silently change confirmed characters, environments, relationships, composition, or preservation constraints. Do not add new elements merely to fill a template field.

## Prompt versus execution

Delivering a prompt does not authorize image or video generation. Conversely, when the user explicitly asks for generation or editing, use the appropriate media tool and treat the prompt as an internal or reviewable specification as the workflow requires.
