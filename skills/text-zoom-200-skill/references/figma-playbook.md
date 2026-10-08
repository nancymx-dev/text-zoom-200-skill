# Optional Figma update playbook

Read when an authorized Figma update is possible. This playbook describes outcomes rather than assuming a particular plugin or connector API.

## Inspect

1. Resolve the exact frame, parent page or section, and nearby content.
2. Inspect the relevant visible layers and one representative repeated item first. Expand the inspection only where needed; avoid dumping an entire large file.
3. Record frame width, text sizes, line heights, layout constraints, clipping, spacing variables, component instances, and font availability.
4. Check relevant hidden states if the agreed change affects them. Hidden error text may matter even though it is absent from the screenshot.

Do not infer editable access from a tool's name. If access is read-only, produce a manual handoff. If a required font or locked instance prevents the edit, report the precise limitation instead of substituting a font or detaching components silently.

## Make a scoped variant

- Duplicate the confirmed frame and place it in clear space. Preserve its width for a text-only comparison.
- Use a descriptive name such as `Checkout - 200% text - Wrap labels`.
- Apply text scaling to the copy using a verified existing mode, local overrides, or an agreed isolated setup. Avoid changing shared styles or global variables.
- Use auto layout where appropriate; let containers grow vertically and text wrap within the available width.
- Inspect nested constraints if the result does not change. A fixed-height ancestor or a fixed-width icon slot can still restrict content.
- Preserve variable bindings and component instances. Reuse an existing text treatment for an agreed addition.
- Use the file's spacing scale and component minimum dimensions. Do not impose a new grid or fixed row height.

## Verify after edits

Inspect the actual result after every meaningful batch. Do not assume a failed operation rolled back; re-read the frame before retrying and avoid making duplicate variants on uncertain retries.

Check text clipping, overlap, actual text sizes, container bounds, long copy, selected states, and action reachability. Scrollable prototypes need behaviour checks; screenshots show only the visible state.

Compare the original and variant at the same width. Record any content, style, or interaction changes that go beyond wrapping and sizing. Stop and ask if they exceed the agreed scope.

## Manual handoff format

When editing is unavailable, provide:

1. Target frame and test method, including known dimensions and assumptions.
2. Selected option and an ordered list of frame, row, and text changes.
3. Existing tokens or styles to reuse, where identifiable.
4. A review checklist tied to the observed failures.
5. Remaining implementation checks and any missing information.

Clearly label this as a specification awaiting implementation.
