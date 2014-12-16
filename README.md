# sass.type

> A glob of functions and mixins for typographic rhythm.

## Usage

Store your type settings inside a variable and create a fall-back `$font-default`

```scss
$font-helvetica: (
  font-family: 'Helvetica, sans-serif',

  base: (
    font-size: 18,
    line-height: 22
  ),

  large: (
    font-size: 36,
    line-height: 42
  ),
);

$font-default: $font-helvetica;
```

Then, with all that data stored we can finally use the mixins:

```scss
h1 {
  font-family: font-family($font-helvetica);
  @include font-scale(large);
}
```

The output will look like this in CSS:

```css
// CSS output

h1 {
  font-family: Open Sans, sans-serif;
  font-size: 36px;
  line-height: 42px;
}
```

## Acknowledgements

- [Setting typographic scale with Sass maps](http://erskinedesign.com/blog/setting-typographic-scale-with-sass-maps/)
