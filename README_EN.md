# Visual Design Reasoning

**20 visual reasoning methods · 5 flexible creative stages · An open-source Skill for OpenAI Codex**

**Language:** [English](README_EN.md) | [简体中文](README.md)

Visual Design Reasoning is a general-purpose design reasoning Skill for OpenAI Codex. It helps creators analyze visual references, explore and refine design directions, identify conflicting constraints, plan image edits, and turn creative briefs into actionable image or video prompts.

It is designed to support better design decisions while respecting the user's current stage and confirmed requirements.

**[Download V1.0.0](https://github.com/muxinMX/visual-design-reasoning/releases/tag/v1.0.0)** · **[View the source](https://github.com/muxinMX/visual-design-reasoning)** · **[Report an issue](https://github.com/muxinMX/visual-design-reasoning/issues)**

## Why this Skill exists

Visual design tasks often blend observation, critique, ideation, iteration, prompt writing, and media generation into one conversation. That can lead to avoidable problems:

- Jumping into solutions when the user asked only for analysis.
- Reopening design choices that have already been approved.
- Producing many superficial variations instead of meaningful alternatives.
- Writing prompts before establishing the subject, constraints, and intended output.
- Agreeing with contradictory requirements without discussing feasibility.
- Treating a prompt request as permission to generate or edit an image.

Visual Design Reasoning first identifies the user's immediate goal, selects only the relevant methods, and respects the boundaries of the requested stage.

## Who it is for

The Skill can assist character designers, illustrators, concept artists, 3D artists, animators, product designers, graphic and brand designers, packaging designers, environment and architectural designers, and anyone using AI to support visual creation.

It can help with character and subject design, visual systems, worldbuilding, products, environments, composition, camera choices, poses, motion, lighting, image editing, multi-reference synthesis, and prompts for still images or animation.

It does **not** impose a signature style, a particular image-generation platform, a fixed aspect ratio, or a default 3D/cartoon aesthetic. The requirements of the current brief come first.

## Key capabilities

- **Reference analysis:** Examine shape, structure, palette, materials, composition, lighting, and observable stylistic patterns.
- **Design reasoning:** Develop a single coherent direction or compare genuinely different approaches when requested.
- **Concept refinement:** Preserve confirmed identities, relationships, and design decisions while improving selected elements.
- **Critical evaluation:** Identify contradictions, physical limitations, and production risks, and propose practical adjustments.
- **Editing and synthesis planning:** Distinguish invariants from allowed changes when preparing local edits, style transfers, or multi-image composites.
- **Prompt writing:** Produce detailed, concise, tool-neutral, or tool-specific prompts as the task requires.
- **Stage control:** Keep analysis, exploration, refinement, prompt creation, and media execution distinct.

## The five-stage workflow

These are **flexible work modes**, not mandatory sequential steps. A user can start at any appropriate stage.

| Stage | Purpose | Boundary |
| --- | --- | --- |
| **Analyze** | Inspect references, diagnose design problems, and discuss constraints. | Do not proceed to a full solution exploration or prompt unless requested. Necessary risks and minimal practical fixes may be discussed. |
| **Explore** | Develop one or more unconfirmed creative directions. | Provide the number of options the user requested. Do not treat a proposal as approved. |
| **Refine** | Improve a chosen direction. | Preserve confirmed decisions and modify only what the task allows. |
| **Prompt** | Turn an existing brief or selected direction into an executable creative prompt. | No prerequisite analysis or exploration is required when the user requests a prompt directly. |
| **Execute** | Generate or edit media. | Requires explicit user authorization and an appropriate tool in the current environment. |

## The 20-method framework

The original 20 methods are preserved as a reference map, organized into maintained modules. In everyday use, users usually describe the goal and let the Skill choose the relevant module rather than memorizing method numbers.

| No. | Method | Primary module |
| --- | --- | --- |
| 01 | Image reverse analysis | Visual Analysis |
| 02 | Style DNA extraction | Visual Analysis |
| 03 | Multi-reference style synthesis | Visual Analysis |
| 04 | Character visual structure | Visual Analysis |
| 05 | Concept-to-character design | Design Reasoning |
| 06 | Base-form IP extension | Design Reasoning |
| 07 | Character variants | Design Reasoning |
| 08 | Worldbuilding | Design Reasoning |
| 09 | Multi-character relationships | Design Reasoning |
| 10 | Scene ideation from subject | Design Reasoning |
| 11 | Composition and camera analysis | Composition and Motion |
| 12 | Multi-subject composition | Composition and Motion |
| 13 | Pose and action design | Composition and Motion |
| 14 | Lighting and atmosphere | Composition and Motion |
| 15 | Identity-preserving extension | Image Editing and Synthesis |
| 16 | Local modification | Image Editing and Synthesis |
| 17 | Style transfer | Image Editing and Synthesis |
| 18 | Multi-image extraction and composite | Image Editing and Synthesis |
| 19 | Static-to-animation planning | Composition and Motion |
| 20 | Prompt optimization | Prompt Generation |

Cross-cutting quality checks review stage boundaries, evidence versus inference, consistency, feasibility, tool permissions, and practical executability. For the full internal mapping, see [`references/method-map.md`](references/method-map.md).

## Versions, download, and installation

### V1.0.0 Release

The [V1.0.0 Release](https://github.com/muxinMX/visual-design-reasoning/releases/tag/v1.0.0) is the formal stable package. Users can download its packaged Skill ZIP and install it directly. It is a historical snapshot from the time of release and should not be assumed to include the English documentation or metadata changes added later on `main`. Use the packaged Skill asset rather than GitHub's automatically generated source archives when following the release installation steps.

### main branch

The [`main` branch](https://github.com/muxinMX/visual-design-reasoning) is the currently maintained repository source. It includes internationalized documentation and metadata changes added after V1.0.0, and it can be used to read the latest documentation or install the Skill manually. It is not a new Release, and documentation updates on `main` should not be interpreted as a fully retested formal release.

Whether you use the release package or install manually from `main`, you should obtain a folder named `visual-design-reasoning` with `SKILL.md` directly inside it. If the downloaded `main` source folder includes a branch suffix, rename the folder to `visual-design-reasoning` before installation.

### Windows (user-level installation)

1. Open File Explorer.
2. Enter `%USERPROFILE%\.codex\skills\` in the address bar. Create the directory if necessary.
3. Copy the entire `visual-design-reasoning` folder into that directory.
4. Verify the resulting path:

   ```text
   %USERPROFILE%\.codex\skills\visual-design-reasoning\SKILL.md
   ```

### macOS (user-level installation)

1. Open `~/.codex/skills/`. If the folder does not exist, create it:

   ```bash
   mkdir -p ~/.codex/skills
   ```

2. Place the entire `visual-design-reasoning` folder inside it.
3. Verify the resulting path:

   ```text
   ~/.codex/skills/visual-design-reasoning/SKILL.md
   ```

Restart Codex after installation. Avoid accidentally nesting two folders with the same name. The `SKILL.md` file must be at the root of the installed Skill folder.

## How to use it

### Automatic invocation

In a Codex environment that supports implicit Skill selection, describe the visual design task naturally. For example:

> Analyze this character concept's silhouette, proportions, costume hierarchy, and identifiable features. Separate visible observations from assumptions. Stay in the Analyze stage, and do not write prompts or generate images.

Automatic selection depends on the environment and task. A plausible answer alone does not prove the Skill was activated.

### Explicit invocation

To request the Skill directly, include its name:

```text
$visual-design-reasoning Analyze this visual brief and recommend one practical design direction. Explain the tradeoffs and do not generate an image.
```

## Case study: feasibility of a two-heads-tall character

The following is an **example workflow** illustrating stage control and analysis capability. It does not claim to reproduce a specific model run, test output, or pass rate.

| Item | Description |
| --- | --- |
| Input request | A stylized 3D character is only two heads tall and has very short limbs, yet must run, climb, and hold props. Analyze the structural conflicts first; do not generate images or prompts. |
| Stage identified by the Skill | **Analyze** |
| Main analysis dimensions | Silhouette readability, range of motion, joint clearance, and 3D production feasibility |
| Output type | Design-conflict analysis, risk explanation, and minimum viable adjustment recommendations |
| Stage control | Remain in Analyze without proceeding unprompted to Prompt or Execute |

## Example tasks

**1. Product exploration with one direction (Explore)**

```text
$visual-design-reasoning Develop one low-visual-noise design direction for a compact desktop speaker suitable for a small apartment. Explain form, materials, controls, and manufacturing tradeoffs. Do not add alternative directions.
```

**2. Multiple environment concepts (Explore)**

```text
$visual-design-reasoning Propose three structurally distinct concepts for a railway station in this fictional world. Compare spatial layout, narrative focus, lighting, and production complexity. Do not choose a final direction for me.
```

**3. Local image-edit prompt (Prompt)**

```text
$visual-design-reasoning Write an image-editing prompt that changes only the character's red jacket to dark-blue waterproof fabric. Preserve the face, body proportions, pose, framing, background, light direction, and all other garments. Output the prompt only. Do not edit the image.
```

**4. Feasibility critique (Analyze)**

```text
$visual-design-reasoning Analyze a concept involving an extremely thin unsupported cantilever made from heavy natural stone for permanent outdoor use. Explain the visual and engineering conflicts and propose minimal viable adjustments. Stay in Analyze.
```

**5. Direct image prompt (Prompt)**

```text
$visual-design-reasoning Write a tool-neutral hero-image prompt for a foldable travel lantern. Skip concept exploration and do not generate the image.
```

**6. Image-to-video prompt (Prompt)**

```text
$visual-design-reasoning Turn this confirmed character action into a six-second image-to-video prompt with anticipation, acceleration, main action, follow-through, and a final hold. Preserve character identity, costume, and background continuity. Do not generate video.
```

## Language behavior

The core instructions are written primarily in English and ask the model to match the user's language and requested level of detail. A user may submit tasks in English or Chinese. Actual invocation and response-language consistency depend on the Codex environment and should be validated there; the existence of English instructions alone does not establish successful multilingual testing.

## Important limitations

- **Reasoning and prompting:** The Skill can independently provide reference analysis, design reasoning, critique, editing plans, and creative prompts.
- **Media generation:** Actual image or video generation and editing require a suitable media tool and explicit user permission.
- **End-to-end status:** Imagegen has been tested separately for image generation and local editing, but the combined Visual Design Reasoning-to-Imagegen Execute workflow has **not** completed full end-to-end validation in V1.0.0.
- **Automatic selection:** Codex may choose another path or tool for a task. Not every media request needs this Skill.
- **Outputs:** Better prompt structure cannot guarantee deterministic media results.
- **Personalization:** V1.0.0 does not store individual design preferences, personal project histories, or custom user workflows.

## Project structure

```text
visual-design-reasoning/
├── SKILL.md
├── README.md
├── README_EN.md                # English repository documentation
├── LICENSE
├── agents/
│   └── openai.yaml
├── references/
│   ├── visual-analysis.md
│   ├── design-reasoning.md
│   ├── composition-motion.md
│   ├── image-editing.md
│   ├── prompt-generation.md
│   ├── quality-check.md
│   └── method-map.md
└── templates/
    ├── visual-analysis.md
    ├── image-prompt.md
    └── video-prompt.md
```

Note: This tree describes the repository after adding `README_EN.md`. The previously published V1.0.0 release archive is a historical snapshot and may not include this newly added documentation.

## Feedback and contributions

Found a confusing installation step, an activation issue, a design-stage failure, or a useful improvement? Please [open an issue](https://github.com/muxinMX/visual-design-reasoning/issues), including the Codex environment, a reproducible task, the expected behavior, and the observed result when possible.

## License and version

Released under the [MIT License](LICENSE). The original public release is **V1.0.0**. The five-stage workflow, maintained method modules, critical design checks, style neutrality, and explicit media-execution boundaries are the core of this version.
