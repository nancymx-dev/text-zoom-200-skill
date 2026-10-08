# Text Zoom 200 Skill

An AI skill for turning 200% text-size design work into a repeatable workflow.

Give your AI assistant default and enlarged views of a screen. The skill guides it to identify layout issues, compare relevant variants, help you choose one, and update a copy in Figma when an authorized editing connection is available. Without editing access, it produces a manual handoff.

**Collect → Compare → Choose → Update and review**

It works with your own design system and uses public accessibility guidance as a baseline. It contains no company-specific guidance, private document links, customer screenshots, or required commercial design-system assets.

## What you need

**Start with the [setup and usage guide](skills/text-zoom-200-skill/GETTING-STARTED.md). It is also included in the downloadable skill ZIP.**

- An AI assistant that can load Agent Skills, or read the skill and its references as context.
- Default and enlarged screenshots, a precise frame link, or a written description of the problem.
- Your own 200% text zoom guide and product design best practices, attached to the assistant, if you want project-specific recommendations. Otherwise the skill uses the [built-in defaults](skills/text-zoom-200-skill/references/accessibility-guidance.md).
- A connected Figma MCP server for direct frame updates. It must expose editing tools, and your account must have edit access to the file. Without that connection, you can still compare screenshots and receive a manual handoff.

Image review requires an assistant with vision. Rendering mockups and editing Figma depend on your environment. This release does not bundle a Figma plugin or executable editor.

## Install

### Using the Skills CLI

If you use the [Skills CLI](https://github.com/vercel-labs/skills), run:

```sh
npx skills add nancymx-dev/text-zoom-200-skill
```

Select `text-zoom-200-skill` and your assistant when prompted. Follow the installer's guidance about reloading the assistant.

### Manual installation

1. Download the [single-skill ZIP](https://github.com/nancymx-dev/text-zoom-200-skill/releases/latest/download/text-zoom-200-skill.zip), or download this repository using GitHub's **Code → Download ZIP**.
2. Extract the single-skill ZIP to get `text-zoom-200-skill/`. In the repository download, locate `skills/text-zoom-200-skill/` instead.
3. Copy that entire folder, including `references/`, to your assistant's documented skill directory. If your client supports ZIP import, import the single-skill ZIP directly.
4. Reload skills or restart the assistant if required by that product.

The skill uses the [Agent Skills format](https://agentskills.io/specification). Installation locations and ZIP import support vary by assistant. Do not upload the entire repository when a client asks for a single skill folder.

If your assistant has no skill installer, attach `SKILL.md` and the files in `references/` to the conversation and ask it to use them. That supplies the instructions for the conversation; it does not install automatic skill discovery.

## Try it

Start with:

> Use text-zoom-200-skill to help me create a 200% text-size variant. Here are the default and enlarged views of the same screen. Identify what breaks, compare layout options, and let me choose before editing a copy.

With only a default view:

> Use text-zoom-200-skill with this default screenshot. Help me plan a full 2× text-size variant. Mark assumptions and anything that needs checking in the enlarged design.

For a manual Figma handoff:

> Use text-zoom-200-skill to compare options for these overlapping labels. I have no Figma editing connection, so give me the chosen option as step-by-step layout instructions.

If automatic selection does not trigger, explicitly name the skill using your assistant's supported syntax.

Use test data or redact private information before sharing screenshots. See [example scenarios](docs/example-scenarios.md) for ways to try the workflow.

## What to expect

| Stage | Result |
| --- | --- |
| Collect | A diagnosis separating visible problems from likely causes, with the test method recorded. |
| Compare | Relevant layout options, a recommendation, and clear trade-offs. |
| Choose | Your selected option, exact target, and agreed edit scope. |
| Update and review | A reviewed design copy when tools permit, or a clearly labelled manual specification. |

The skill preserves the existing content and visual identity where possible. It does not require a specific device width, type scale, spacing grid, font, or design tool.

## Accessibility scope

This is a design-assistance workflow, not an accessibility certification or automated audit. A full 2× text simulation is its default. Browser zoom, reflow, native text settings, and the implemented product need their own checks. See [the accessibility reference](skills/text-zoom-200-skill/references/accessibility-guidance.md) for the public sources and test distinctions.

## Repository structure

```text
skills/text-zoom-200-skill/
  SKILL.md
  GETTING-STARTED.md
  LICENSE.txt
  references/
    accessibility-guidance.md
    layout-patterns.md
    figma-playbook.md
    project-guidance-template.md
docs/
  update-notes.md
  example-scenarios.md
README.md
LICENSE
```

The skill folder is the installable unit. The README and docs explain setup and usage for people browsing GitHub. This follows the self-contained skill pattern used in [Anthropic's skills](https://github.com/anthropics/skills) and [Vercel's agent skills](https://github.com/vercel-labs/agent-skills). Instructions here are written for this workflow; those repositories' skill implementations are not bundled.

## Contributing

Open an issue or pull request with a reproducible layout problem, expected behaviour, and a synthetic or redacted example. Include platform, frame width, and resizing method. Keep project-specific rules in your own project context rather than adding them as universal defaults.

## License

[MIT](LICENSE). Created by [Nancy](https://github.com/nancymx-dev).
