# Updates for general use

The public edition keeps the original idea: an AI skill guides a designer from an enlarged-text problem through options, a decision, and a reviewable update.

## Changes

| Area | Change | Why |
| --- | --- | --- |
| Scope | Use any screen and design system. | The workflow should not require workplace context. |
| Guidance | Replace the internal reference with public W3C sources and optional user-provided project guidance. | Anyone can access the baseline. |
| Text sizing | Default to full 2× text, including headings. Identify custom ramps separately. | A large-text mode name does not establish its actual scale. |
| Dimensions | Use the actual viewport, spacing tokens, and component minimums. | Device widths and design grids vary. |
| Tools | Make artifacts, structured questions, and Figma editing optional capabilities. | Assistants and connectors differ. |
| Editing | Confirm scope, duplicate by default, and reuse authorization already given. | Keep changes controlled without repeating completed decisions. |
| Figma mechanics | Replace connector-specific scripts with an outcome-based playbook. | Avoid assuming an API helper, font, layer structure, or rollback behaviour. |
| Patterns | Treat scrolling and expansion changes as contextual decisions. | Removing scrolling or collapsing content can change usability. |
| Evidence | Separate screenshot observations, suspected causes, and verified implementation behaviour. | Prevent claims that the available evidence cannot support. |
| Packaging | Add installation instructions, examples, and an MIT license. | Make the skill usable and shareable from GitHub. |

## What remains

- A designer chooses the variant.
- Options focus on preserving content and function at larger text sizes.
- Layout changes are preferred when sufficient.
- An agreed update is applied to a copy when authorized tools permit it.
- Results and unresolved questions are reviewable.

## File changes

- Rewrite `SKILL.md` as a tool-independent workflow.
- Replace the project guidance file with `references/accessibility-guidance.md`.
- Rewrite the component patterns as `references/layout-patterns.md`.
- Rewrite the optional Figma notes as `references/figma-playbook.md`.
- Add a repository README, example scenarios, and a license.

No internal document export, private image, or original workplace reference is included in this repository.

## Research behind the packaging

- [Agent Skills specification](https://agentskills.io/specification): use a named folder containing `SKILL.md`, with optional references loaded when needed.
- [Anthropic skills](https://github.com/anthropics/skills): keep each skill self-contained and explain its use in repository documentation.
- [Vercel agent skills](https://github.com/vercel-labs/agent-skills): offer a short installation path and a clear account of each skill's purpose.

The earlier [OpenAI skills catalog](https://github.com/openai/skills) now points readers to [OpenAI plugins](https://github.com/openai/plugins) for current examples. This release uses the portable skill format rather than claiming to be a fully packaged plugin for every assistant.
