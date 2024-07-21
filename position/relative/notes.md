#### Info
- creating a **positioning context** for its children.
- **it remains in the document flow**, so space is still allocated for it as if it were in its default static position. However, you can use the `top`, `right`, `bottom`, and `left` properties to adjust the element's position relative to where it would have been in the normal flow.
- This means the element is still **part of the layout**, and other elements around it are not affected by its position adjustments.

#### Usecases
- Slight adjustments to element position
- Creating a positioning context for absolute children
- Animating element movement
- Layering elements with z-index
- Offsetting text or images
