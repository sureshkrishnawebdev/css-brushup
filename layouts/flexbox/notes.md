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

**Pros:**

- Simplifies responsive design and complex layouts.
- Provides better control over alignment and space distribution.

**Cons:**

- Not ideal for complex two-dimensional layouts (use CSS Grid instead)
- Not fully supported in older browsers.