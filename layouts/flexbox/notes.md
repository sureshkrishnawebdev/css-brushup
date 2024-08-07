### Flexbox

**What:**

- It's one-dimensional "layout system" that provides efficient way to distribute the space and align-content within a container, "even when the size of items is unknown or dynamic".

**Why:**

- It provides efficient and predictable way to layout, align, and distribute space among items in a container
- It allows for easier alignment of elements, responsive design.

**When:**

- Responsive layouts without relying heavily on floats or positioning.
- Align items vertically and horizontally with ease.
- Distribute space among items proportionally

**How:**

- First define a container element as a flexbox with "display: flex". This leads to flex-items(child) of the flex container
- Then, you can align flex items in both axis by specifying below declarations on flex container
  - main axis(horizontal): justify-content: center;
  - cross axis(vertical): align-items: center;
- By default, flex container always tries to shrink down elements(flex-items) to smallest as they get.

**Pros:**

- Simplifies responsive design and complex layouts.
- Provides better control over alignment and space distribution.

**Cons:**

- Not ideal for complex two-dimensional layouts (use CSS Grid instead)
- Not fully supported in older browsers.

### CONCEPTS


**1. Units**

  - px, %, rem, em

**2. Positioning**

  - main axis(horizontal): justify-content: center; //flex-start(D),flex-end, space-*(* - between, around, evenly), reverse
  - cross axis(vertical): align-items: center; //stretch(D), flex-start, flex-end
  - changing the main axis: flex-direction: row(D), //column

**3. Alignment**

  - viewport: [width, height]
  - flex-container: [row, column]
  - align = vertical = column
  - justify = horizontal = row

1 - To align items inside the flex container
  - "align-items" -> vertical alignment
  - "justify-content" -> horizontal alignment
  - if main axis: row

2 - For individual items to override the alignment specified for flex container
  - "align-self" -> vertical alignment[override - align-items]

3 - Alignment of flex tracks
  - In general,  if the flex container is smaller than the viewport, then [align-items*, align-self*] props won't provide the flexibility to align flex container.
  - "align-content" -> vertical alignment -> well observed when we have flex property as wrap(i.e. when we have multiple rows)

**4. shorthands**

  1 - flex: [flex-grow flex-shrink flex-basis]
    -> when we set the value of [flex: 1] -> it changes default values as follows [grow(0 -> 1) shrink(1 -> NA) basis(auto -> 0%)]

  2 - flex-flow: [flex-direction flex-wrap]


### Doubts
  - How does the flex works?. How it manages the space?