### Selectors

**What:**

- They're patterns used to select and style HTML elements on a web page. They are the bridge between your HTML structure and the CSS styles you want to apply.

**Why:**

- It allow you to target specific elements or groups of elements for styling without modifying the HTML directly.
- This separation of concerns keeps your code clean, maintainable, and efficient.

**When:**

- Use whenever you need to apply styles to HTML elements. They're essential in every CSS file or style block.

**How:**

- They are used in your stylesheet or style tag, followed by a block of CSS properties.
- The basic syntax is:
```
selector {
  property: value;
}
```

**Commonly used selectors**
1. element(div, main, h*, p, span...)
2. id(#)
3. class(.)
4. descendant(space)
5. child(>)
6. sibling(~)
7. adjacent sibling(+)
8. pseudo
  8.1. class(:)
  8.2. element(::)