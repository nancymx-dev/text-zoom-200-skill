# Layout patterns for enlarged text

Choose patterns from the observed failure and the component's purpose. These are candidate approaches, not universal fixes.

| Component or issue | Start with | Review before changing more |
| --- | --- | --- |
| Clipped row or card | Let the content wrap and the container grow; retain the project's minimum target size. | Inspect fixed-height ancestors as well as the row. |
| Label and trailing value collide | Allow wrapping or stack the value below its label. | Preserve reading order and the relationship between the two. |
| Narrow text column | Let text fill available width and grow vertically; inspect oversized fixed icon slots. | Keep icons meaningful and aligned with the associated text. |
| Button label clips | Allow multi-line text and content-driven height. Stack adjacent buttons if needed. | Keep the action reachable and avoid shortening essential meaning just to fit. |
| Form content clips | Let labels, values, helper text, and errors grow or wrap. | Some inputs need a suitable scrolling or expanded editing treatment; do not assume every field can wrap. |
| Navigation or tabs | Consider wrapping, more height, or a discoverable scrolling treatment. | Evaluate keyboard access, selected-item visibility, and reflow requirements in implementation. |
| Menu or option list is crowded | Grow rows, wrap labels, and give values their own line. | Keep scrolling usable. Removing an inner scroll region can change how the component works. |
| Modal or sheet loses actions | Adapt height to available space and provide a deliberate scroll area. | Check focus, keyboard appearance, and access to dismiss and primary actions in the product. |
| Table columns become unreadable | Permit wrapping; consider an alternative row presentation. | Preserve headers and comparison relationships. Some data tables need two-dimensional layout. |
| Badge or status loses meaning | Let its container grow; add a text label only if the meaning needs clarification. | A label is a content addition. Icon prominence alone does not prove an accessibility failure. |

## Change categories

- **Layout only:** sizing, wrapping, alignment, or stacking without changing content or behaviour.
- **Content addition:** an explicit label or other new copy. Explain the reason and reuse the design system's treatment.
- **Interaction change:** different expansion behaviour, a new selector, changed scroll ownership, or a different navigation pattern. Explain the impact and obtain a decision.

Prefer a layout fix when it solves the issue. Avoid automatically replacing menus with sheets, collapsing content, removing scroll areas, or changing selection states. Those choices depend on the screen and require behavioural review.

Do not shrink enlarged text to preserve a single line. If truncation remains necessary, identify how the full information is available and what must be tested in the implemented experience.
