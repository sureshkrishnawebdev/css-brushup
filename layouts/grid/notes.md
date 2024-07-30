### Grid

**What:**

- It's two-dimensional "layout system" that allows you to create complex web layouts with rows and columns.

**Why:**

- To create complex layouts with less code.
- It allows for easier alignment of elements, responsive design.

**When:**

- To create multi-column or multi-row layout.
- It's particularly useful for overall page layouts, card layouts, image galleries, and dashboard interfaces.

**How:**

- First define a container element as a grid with "display: grid".
- Then, you can set the number and size of rows and columns using properties like "grid-template-rows" and "grid-template-columns".
- Child elements can be placed within the grid using properties like grid-column and grid-row.

**Pros:**

- Simplifies responsive design.
- Reduces the need for media queries.
- Allows for easy alignment of elements.

**Cons:**

- Not fully supported in older browsers.

====================================
CONCEPTS
====================================
**1. Units**

- fr = fractional unit
- min-content
- max-content
- px, %, rem, em


**2. Positioning**

- By default grid cells will be positioned based on normal document flow.
- If we need to change their position then we can do as follows
  -  shorthand: grid-row: 2 / 3;
  (or)
  -  defining start and end grid line: grid-row-start: 2, grid-row-end: 3
  (or)
  - for most readable and scalable way: we use grid cell names
    - We need to make changes at the “grid-template-*”
    - We need to use them declare them instead of line/track numbers
    - grid-template-rows: [header-start] 150px [header-end box-start] 200px [box-end];

