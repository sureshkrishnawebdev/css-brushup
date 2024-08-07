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


### CONCEPTS


**1. Units**

    1 - px, %, rem, em
    2 - fr = fractional unit
      -> it fills up the entire remaining space but it is never smaller than the minimum content of the row or column.
        * "normal": [repeat(3, 1fr), width: 600px] => 1fr = 200px[all 3 columns]
        * "min-content > 1fr value": [repeat(3, 1fr), width: 600px, width of content in 3rd column is 300px] => 1fr = 150px(1st 2 columns), 3rd column = 300px
    3 - min-content
    4 - max-content
    5 - minmax(200px, 50%) -> by default the column will have max value on shrinking it will try to not to go beyond the min value


**2. Positioning/ Spanning**

- By default grid cells will be positioned based on normal document flow.
- If we need to change their position then we can do as follows
  1-  shorthand: (grid-row: 2 / 3)
  (or)
  2-  defining start and end grid line: (grid-row-start: 2, grid-row-end: 3)
  (or)
  3- for most readable and scalable way: we use grid cell names
    - We need to make changes at the “grid-template-*”
    - We need to use them declare them instead of line/track numbers
    - (grid-template-rows: [header-start] 150px [header-end box-start] 200px [box-end])

  - Based on our boundary, positioning can be differentiated
    1- positioning: Involves explicitly defining the start and end.
      eg: (gird-row-start: 1, grid-row-end: 3) == (grid-row: 1 / 3)

    2- spanning: For dynamic usage, with the help of key "span"
      eg: (grid-row: 1/ span 2);

**3. Types of grid**

- _Explicit Grid:_ Defined by properties like "grid-template-rows" and "grid-template-columns".

- _Implicit Grid:_ Automatically generated when items are placed outside the explicitly defined grid.
  - Control Implicit Grid: we use below properties to control the size of implicitly created tracks.
    1. "grid-auto-rows" -> to set the row width.
    2. "grid-auto-columns" -> to set the column width.
    3. "grid-auto-flow"
      1-> [row(default), column  dense] -> how do we need to add the implicit grid.
      2-> [dense] -> By default, grid algorithm tries to align items in normal document flow. There by when it encounters there may be scenario, a space(whole) will be created based on element spacing.

**4. Alignment**
- grid container: [width, height]
- grid area: [grid-template-*]
- align = vertical = column
- justify = horizontal = row

1 - To align items inside the grid area
  - "align-items" -> vertical alignment
  - "justify-items" -> horizontal alignment

2 - For individual items to override the alignment specified for grid area
  - "align-self" -> vertical alignment[override - align-items]
  - "justify-self" -> horizontal alignment[override - justify-items]

3 - Alignment of grid tracks
  - In general,  if the grid area is smaller than the grid container, then [align-items*, align-self*] props won't provide the flexibility to align grid area.
  - "align-content" -> vertical alignment
  - "justify-content" -> horizontal alignment