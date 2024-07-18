### What:
- SVG is an XML-based vector image format for two-dimensional graphics.

### Why:
- Scalability: Must scale to different sizes without losing quality(responsive design).
- Accessibility:
  - Manipulated with just css and js code.
  - Can be indexed by search engines and supports accessibility features.
- Performance: Vector graphics are often smaller in file size compared to raster images.

### When:
- For graphics that scale without losing quality(creating logos, icons, and illustrations) that need to be displayed at various sizes.
- When you want to animate or interact with graphics.
- For accessible and SEO-friendly graphics.

### How:
1. Inline in HTML
2. As an image source
3. As a background image in CSS
4. Embedded using an <object> or <embed> tag

### Doubts:
1. properties of svg [viewBox, width, height, canvas, viewport]

### Jargons:
- SVG (Scalable Vector Graphics)
- XML (Xtensible Markup Language)


CONCEPTS
------------------------------------
### 1. Viewport
- It's the visible part(viewable area) of the svg.
- It's defined with the help of **width** and **height**


### 2. ViewBox
- It controls what shows up inside the viewport(viewable area).
- It has 4 values
  - [min-x, min-y, width, and height]
  - 1st 2 values - [min-x, min-y] - used for **panning**
    - where viewport's position is moved
  - 2nd 2 values - [width and height] - used for **zooming**[like a thread]
    - larger values -> zoomed out
    - smaller values -> zoomed in

### 3. canvas
- It's the infinite plan where svg elements exists devoid of the viewport