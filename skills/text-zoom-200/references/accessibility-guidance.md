# Accessibility baseline

Use this reference to establish the resizing method and the limits of a design review. These notes paraphrase public guidance; they do not replace the linked criteria or platform requirements.

## Three distinct checks

| Check | What to simulate or test | What the result can tell you |
| --- | --- | --- |
| Text-only enlargement | Increase text while retaining the viewport width. | Whether text containers and controls accommodate larger text. |
| Browser zoom and reflow | Use a real browser and record zoom and viewport dimensions. | How the rendered page adapts when the visible CSS viewport changes. |
| Native accessibility text settings | Use the target platform's supported text settings in the implemented app. | Whether the app respects platform scaling and remains usable at those settings. |

Do not infer the latter two from a text-only Figma variant. Use current platform documentation when a platform-specific test is needed; do not equate a named native setting with exactly 200% without measuring it.

## Public web guidance

- [WCAG 2.2, Understanding SC 1.4.4: Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html): text must support enlargement up to 200% without losing content or functionality, with exceptions for captions and images of text. Headings have no general exemption. Where incremental resizing is supported, inspect intermediate sizes too. A screenshot does not demonstrate compliance. Truncation needs an indicated, usable route to the full information where that exception applies; ellipsis alone is insufficient.
- [F69: clipping or obscuring content when resizing](https://www.w3.org/WAI/WCAG22/Techniques/failures/F69): use this when enlarged content disappears or overlaps.
- [F80: text controls that fail to resize](https://www.w3.org/WAI/WCAG22/Techniques/failures/F80): use this when text-based controls cannot accommodate their text.
- [SC 1.4.10: Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html): review narrow-viewport adaptation separately. For horizontally written web content, the criterion uses a width equivalent to 320 CSS pixels, subject to its exceptions. A 200% text-size frame is not that test.
- [SC 1.4.12: Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html): check that supported user spacing overrides do not lose content or function. This does not prescribe the design's default spacing.

## Design simulation defaults

When no project ramp is provided, use full 2× text sizing for the proposed variant and preserve readable line-height proportions. Keep the frame width fixed for this simulation. Preserve the existing spacing scale and visual identity, adjusting layout constraints as needed. Do not invent a universal row height, spacing unit, or device width.

When a project supplies a custom ramp, inspect what it does, identify differences from full 2×, and show the appropriate separate test. Visual prominence of a large heading is not evidence that it can reach twice its original size.

Keep the public baseline, project preferences, and observed test results distinct. If project guidance conflicts with a criterion, describe the conflict rather than declaring compliance.
