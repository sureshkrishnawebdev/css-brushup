### What:
- It's a property - used to specify how an element is positioned in a document.
- It determines the "layout" and "placement" of elements on a web page.

### Why:
- Fine-grained control over element placement.
- More dynamic and complex layouts that aren't possible with standard document flow.

### When:
- Create overlapping elements.
- Build sticky headers or sidebars.
- Create pop-ups or modals.

### How:
- position: X;
- X = 5 values
    1. **static (default)** -> Used for the main content and most elements.
    2. **relative** -> creating a **positioning context** for its children.
    3. **absolute** -> positioning it relative to its **nearest positioned ancestor**.
    4. **fixed** -> keeping elements in a **fixed position regardless of scrolling**(i.e. It may hide while scrolling).
    5. **sticky** -> keeping elements **visible while scrolling**.

### Tools:
- top, right, bottom, left
    - When position value is static(default) for an element then we won't be able to access their coordinates
-
    

### Doubts:
1. "layout" vs "placement"
2. fixed vs sticky