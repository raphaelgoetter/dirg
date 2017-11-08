# DIRG
DIRG is a pure CSS ultra-light Grid Framework

Demo : https://codepen.io/raphaelgoetter/pen/XzdeRe?editors=1100

# Install

<del>nodeJS</del> <del>jQuery</del> <del>JavaScript</del> <del>Sass</del>

Just use `dirg.css` (few octets)

# Howto?

# FAQ

- Compatibility
- Licence

# Example

```
<div class="dirg" style="--grid-number: 3; --grid-gutter: 1rem;">
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

```
:root {
  --grid-number: auto;
  --grid-gutter: 0;
  --grid-col: 1;
  --grid-row: 1;
}

.dirg {
  display: grid;
  grid-gap: var(--grid-gutter);
  grid-auto-flow: row dense;
}

@media (min-width: 576px) {
  .dirg {
    grid-template-columns: repeat(var(--grid-number), 1fr);
  }
  .dirg > * {
    grid-column: auto / span var(--grid-col);
    grid-row: auto / span var(--grid-row);
  }
}
```
