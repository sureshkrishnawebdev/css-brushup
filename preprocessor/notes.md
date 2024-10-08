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
=======================================================
### Sass: Features

**1. nesting**
  - we can nest the selectors inside one another
  - we could also specify respective media queries inside the selector there by code is organized in single place. If we need to have media queries with specific width to be grouped we could use postprocessing tools.
  - Recommendation: single level of nesting, using media queries in here for dev

**2. mixin**
  - Used for reusing/encapsulating the styles(copy styles into the current style rule)
  - It helps us to be DRY
  - mixins works well with maps(i.e. arrays)
  - Recommendation: media query, content
  - Link: https://sass-lang.com/documentation/at-rules/mixin/

**3. partials**
  - Partials in Sass helps us to break our files into small files without affecting performance which makes development easy and while compiling it turns into single file
  - an Sass file preceded by an underscore(_color)
  - Link: https://sass-guidelin.es/#architecture

**4. extend**
  - Used to inherit styles(updates style rules that contain the extended selector)
  - Combine selectors in the output CSS, creating a comma-separated list of selectors sharing the same properties.
  - Link: https://sass-lang.com/documentation/at-rules/extend/

**5. others**
  - build-in modules: maps, math, color, list
  - at-rules: use, mixin, include, extend, forward, content, function, error, debug
  - flow-control: @each, @for