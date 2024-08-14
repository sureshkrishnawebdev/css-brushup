**What**
  - It's a scripting language that extends CSS and gets compiled into regular CSS syntax.
  - It allows you to use variables, nested rules, mixins, functions, and other programming constructs in your stylesheets.

**Why**
  - Enhances code organization, efficient and maintainability(eg: DRY).
  - Provides advanced features not available in plain CSS.

**When**
  - For large-scale projects with complex stylesheets.
  - When you need to maintain consistent styles across multiple pages or components.

**How**
  - Choose a preprocessor (e.g., Sass, Less, Stylus).
  - Add it in dev environment, compile and link to HTML.
  - eg: Using Sass

  ```
  // Variables
    $primary-color: #3498db;
    $font-stack: Helvetica, sans-serif;

  // Mixin
    @mixin border-radius($radius) {
      -webkit-border-radius: $radius;
        -moz-border-radius: $radius;
              border-radius: $radius;
    }

  // Nesting and parent selector
    .button {
      font: 100% $font-stack;
      padding: 10px 20px;
      color: white;
      background-color: $primary-color;
      @include border-radius(5px);

      &:hover {
        background-color: darken($primary-color, 10%); //Color functions
      }
    }
  ```