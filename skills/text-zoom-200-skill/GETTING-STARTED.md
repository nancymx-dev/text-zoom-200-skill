# Start here: Text Zoom 200 Skill

This skill helps your AI assistant compare and apply design variants for enlarged text. Installing it supplies instructions. Connecting Figma MCP gives the assistant access to your design file.

## 1. Install the skill

Use the installation instructions in the [GitHub README](https://github.com/nancymx-dev/text-zoom-200-skill#install), or import the downloaded single-skill ZIP if your assistant supports ZIP import. Keep `SKILL.md` and the `references/` folder together.

## 2. Connect Figma MCP

**To have the AI update a Figma frame, connect Figma MCP in the same assistant where you use the skill.**

1. Open your assistant's integrations, connectors, plugins, or MCP settings.
2. Add its supported Figma connection. If your client supports a custom remote MCP URL, Figma's hosted endpoint is `https://mcp.figma.com/mcp`.
3. Complete Figma sign-in and grant access through the supported connection flow.
4. Check that your Figma account has permission to edit the intended file.
5. Copy the link to the exact frame or selection and share it with the assistant.
6. Ask: “Confirm you can read this frame and tell me whether your Figma tools can edit a duplicate. Do not make changes yet.”

Figma recommends the remote server. Follow [Figma's setup guide](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/) for your client. Its [write-to-canvas documentation](https://developers.figma.com/docs/figma-mcp-server/write-to-canvas/) explains editing support. Available tools and access depend on the client and account, so confirm capabilities rather than assuming a successful connection includes writing.

If your assistant uses a managed Figma plugin, use that supported setup flow. You do not need to configure a second connection just to match these steps.

**No connection or read-only tools?** You can still use screenshots to compare options. The skill will give you a manual Figma update plan instead of editing the file.

## 3. Supply your own guidance, or use the defaults

**Upload or attach your own 200% text zoom guide and product design best practices to the assistant if you want it to follow your project's rules.** An accessible project document link also works when the assistant can read it. A link it cannot open is not usable context.

Useful inputs include:

- Your type sizes, line heights, and how the large-text mode resolves.
- Component rules for wrapping, minimum sizes, scrolling, and selected states.
- Your spacing tokens and approved layout or interaction patterns.
- Platforms, screen widths, and required text-size settings.

Use [the project guidance template](references/project-guidance-template.md) if you do not have a complete guide. Keep confidential guidance in your own assistant or approved project workspace. Do not submit it to this public GitHub repository.

**If you supply no guidance, the skill uses its built-in defaults.** It should tell you which guidance is in use. Project rules inform the design, but do not turn a custom scale into evidence of accessibility conformance. Conflicts with public requirements should be called out.

## 4. Prepare your screen

Share a default view and a 200% text view of the same screen, using the same width, content, and state. The enlarged view can be broken. Use test data or redact private information.

Tell the assistant whether you are testing text-only enlargement, browser zoom, or native text settings. If you only have the default view, it can propose a variant and mark the enlarged behaviour as unverified.

For a Figma text-only simulation, keep the frame width unchanged. Use a verified full 2× text mode or adjust sizes in a copy. Scaling the entire frame does not create the same test.

## 5. Run the workflow

With your own guide:

> Use text-zoom-200-skill. I have attached our 200% text zoom guide and product design best practices, plus default and enlarged screenshots. Read the guidance, identify what breaks, and compare options. Let me choose before updating a duplicate of the linked Figma frame. Confirm your editing access first.

With the defaults:

> Use text-zoom-200-skill with its built-in design practices. This is a text-only 200% test. Here are my default and enlarged screenshots. Compare fixes at the same width, then help me choose and review a variant.

The assistant should diagnose, compare, confirm your choice and target, then update and review a copy when authorized tools permit it.

## Built-in design practices at a glance

- Use full 2× text sizing, including headings, for the default text-only simulation.
- Let text wrap and containers grow; inspect constraints in parent frames too.
- Keep all essential content and controls available, with a clear reading order.
- Grow or stack buttons as needed while retaining the project's minimum target sizes.
- Let helper and error messages remain readable; check long content and translated copy.
- Preserve existing components, styles, and spacing tokens where possible.
- Treat changed scrolling, navigation, or expansion behaviour as a design decision.
- Review the chosen variant visually and test actual behaviour in the implemented product.

See [the default practices and public sources](references/accessibility-guidance.md) and [component layout patterns](references/layout-patterns.md) for details.

## Troubleshooting

| Problem | What to do |
| --- | --- |
| The assistant cannot see the skill | Reload skills or explicitly attach `SKILL.md` and its references. |
| It cannot read the guidance document | Attach a readable copy or use the defaults; do not assume it read the link. |
| Figma tools are missing | Check the connection in the same assistant, sign-in, and the client's supported Figma setup. |
| It can read but cannot edit | Check file permissions and write-tool support; use the manual handoff meanwhile. |
| It used the wrong frame | Share a link to the specific selection and confirm the frame before editing. |
| Your large-text mode does not double every text size | Label it as a custom ramp and request a separate full 2× simulation. |
