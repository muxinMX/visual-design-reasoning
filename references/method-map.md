# Legacy Method Map

Use this reference for maintenance, debugging, or when the user explicitly invokes a legacy method number. The public workflow should normally route by user goal rather than expose this catalog.

| Legacy | Method | Primary module | Modernized boundary |
|---:|---|---|---|
| 01 | Image reverse analysis | visual-analysis | Prompt output is optional and stage-gated. |
| 02 | Style DNA extraction | visual-analysis | Separate content from transferable visual traits. |
| 03 | Multi-reference style synthesis | visual-analysis | Assign source roles and resolve conflicts before synthesis. |
| 04 | Character visual structure | visual-analysis | Generalize to subject or system structure where appropriate. |
| 05 | Concept-to-character design | design-reasoning | Do not default to Midjourney or prompt output. |
| 06 | Base-form IP extension | design-reasoning | Treat invariants and variables as a general series system. |
| 07 | Character variants | design-reasoning | Preserve identity; keep variants structurally distinct. |
| 08 | Worldbuilding | design-reasoning | Remain at world level until character work is requested. |
| 09 | Multi-character relationships | design-reasoning | Connect narrative roles to visible contrast and interaction. |
| 10 | Scene ideation from subject | design-reasoning | Define a key moment before composition or prompting. |
| 11 | Composition and camera analysis | composition-motion | Treat exact optics as estimates. |
| 12 | Multi-subject composition | composition-motion | Specify depth, overlap, gaze, and interaction. |
| 13 | Pose and action design | composition-motion | Validate center of mass, contacts, range, and silhouette. |
| 14 | Lighting and atmosphere | composition-motion | Preserve non-lighting invariants for lighting-only edits. |
| 15 | Identity-preserving extension | image-editing | Record invariants separately from allowed variables. |
| 16 | Local modification | image-editing | Describe the delta and prevent spillover. |
| 17 | Style transfer | image-editing | Preserve content identity; translate observable style traits. |
| 18 | Multi-image extraction and composite | image-editing | Assign each source a contribution and prevent identity mixing. |
| 19 | Static-to-animation planning | composition-motion | Use a timed action arc and continuity constraints. |
| 20 | Prompt optimization | prompt-generation | Offer only the form and tool adaptation the user needs. |

## Consolidation rationale

- Methods 01–04 share visual evidence extraction and belong together.
- Methods 05–10 share concept development and system design.
- Methods 11–14 and 19 share spatial, temporal, and presentation logic.
- Methods 15–18 share preservation-aware transformation.
- Method 20 is the output adapter used after any module when the stage permits.
- Quality checking is cross-cutting rather than a separate user-facing method.

## Coverage verification

- **01–04:** `visual-analysis.md` implements reconstruction analysis, style/content separation, multi-reference role assignment and conflict resolution, and subject structure analysis.
- **05–10:** `design-reasoning.md` implements concept-to-form reasoning, character or subject design, series invariants and variables, worldbuilding, team relationships, and scene ideation.
- **11–14 and 19:** `composition-motion.md` implements framing and camera analysis, group composition, physical pose logic, lighting and atmosphere, and timed animation arcs.
- **15–18:** `image-editing.md` implements identity invariants, edit deltas, style conversion, source-role assignment, composite integration, and spillover prevention.
- **20:** `prompt-generation.md` implements direct, detailed, compact, edit, video, and optimized prompt outputs without requiring earlier stages.

The map preserves every legacy capability while shared execution steps remain consolidated in the five maintained modules.
