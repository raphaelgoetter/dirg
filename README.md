# DIRG
DIRG is a pure CSS ultra-light Grid Framework

Demo : https://codepen.io/raphaelgoetter/pen/XzdeRe?editors=1100

# Install

<del>nodeJS</del> <del>jQuery</del> <del>JavaScript</del> <del>Sass</del>

Just use `dirg.css` (few octets)

# Howto?

Add a `.DIRG` class on a parent to create a new grid.

Then, use the `style=` HTML attribute just to change the variables values either on parent or some children.

Example :
```
<div class="DIRG" style="--grid-number: 3; --grid-gutter: 1rem;">
```
will design a 3 columns grid with a 1rem gutter between children.

# Variables

- `--grid-number`: number of columns inside the grid. (apply on parent) (default value: `auto`)
- `--grid-gutter` gutter size between children. (apply on parent) (default value: `0`)
- `--grid-col` column spanning (apply on child). (default value: `1`)
- `--grid-row` row spanning (apply o n child). (default value: `1`)

# FAQ

## But inline `style=` is bad!

Nah. Inline *styles* are bad. Here, you just change the value of a variable. No real properties will be hurt.

## Compatibility

- Grid Layout : Edge 16 https://caniuse.com/#feat=css-grid
- CSS custom properties (variables) : Edge 16 https://caniuse.com/#feat=css-variables

## Licence

WTFPL http://www.wtfpl.net/

# Full Example

```
<div class="DIRG" style="--grid-number: 3; --grid-gutter: 1rem;">
  <div>1</div>
  <div>2</div>
  <div style="--grid-col: 2;">3</div>
  <div>4</div>
  <div style="--grid-row: 2;">5</div>
  <div>6</div>
  <div>7</div>
</div>
```

![result](https://raw.githubusercontent.com/raphaelgoetter/dirg/master/dirg.png)
