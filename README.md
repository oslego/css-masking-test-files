Test files for [CSS Masking](http://dev.w3.org/fxtf/css-masking-1) `clip-path` and `mask` support.

[support matrix](https://github.com/awgreenblatt/css-graphics)

# Notes
- Chrome and WebKit [bug with coordinate space](https://code.google.com/p/chromium/issues/detail?id=417370) when referencing SVG `<clipPath>`. (workaround: set `-webkit-transform: translate(0,0);` on HTML element).
- `mask` used to be a SVG-only CSS property. It is evolving to be a shorthand of `mask-image`, `mask-size`, `mask-mode`, etc for both SVG & HTML.
- Firefox supports referencing SVG `<mask>` elements for masking HTML, but not images.
- Change mask type (luminance or alpha) with CSS property `mask-source-type` (behind flag in Chrome, prefixed in WebKit), not `mask-mode`?? (`mask-type` is an attribute for the SVG `<mask>` element).

## Expected results

Fully compliant browsers for `clip-path` and `mask` must clip each box to a circle.
