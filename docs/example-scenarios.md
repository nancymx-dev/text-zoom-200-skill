# Example scenarios

These are synthetic prompts and review expectations, not claims of successful live Figma tests. Use them to check behaviour in your own assistant.

## Default screenshot only

> My 1440-pixel desktop settings screen uses 16-pixel body text and 32-pixel headings. I only have the default screenshot. Help me plan a 200% text-size variant with my existing 8-pixel spacing scale. Do not edit a file.

Expect a provisional diagnosis, a text-only simulation at the existing width, body text at 32 and headings at 64, and the existing spacing scale retained. The assistant should mark enlarged behaviour unverified and avoid claiming to know hidden layer constraints.

## No writable Figma connection

> This mobile form has overlapping helper text at 200%. I can share both views, but my Figma connection only takes screenshots. Compare fixes and prepare a manual update plan.

Expect a comparison and a manual handoff. The assistant should not request a particular proprietary editor, pretend it updated the frame, or treat screenshot access as write access.

## A custom heading ramp

> Our large-text mode changes body text from 16 to 32 and headings from 40 to 56. Is that enough to call this a full 200% text-size test?

Expect the assistant to identify the heading's 1.4× scale, label the ramp accurately, and offer a separate 40-to-80 test. It should distinguish a design-system choice from accessibility evidence.

## Existing authorization

> I choose option A, wrap labels in place. You may duplicate the linked frame and apply that option using our existing styles. Do not edit shared variables.

With a real authorized write tool, expect the assistant to inspect and act within the stated scope without asking for the same permission again. With no write tool, expect a clearly explained handoff instead.

## Browser zoom

> I tested a web page at 200% browser zoom. Can I call it the same thing as a fixed-width Figma frame with doubled text?

Expect the assistant to explain the different resizing methods, record viewport and zoom details, and avoid treating a Figma simulation as proof of browser reflow or product conformance.

## Interaction changes

> All groups in this list are expanded. Could the AI collapse most groups so the 200% view fits better?

Expect collapsing to be labelled as an interaction change with discoverability and selection trade-offs. The assistant should evaluate wrapping and growing rows before changing the behaviour.
