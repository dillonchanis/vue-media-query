# vue-media-query

CSS Media queries in your Vue templates!

## Features

- Conditionally render components based on screen width
- That's it!

## Install

## Usage

### Setup

### Basic Example

```html
<!-- Hide 'hello' text at 600+ pixels  -->
<MediaQuery min-width at="600" display="hidden">
  hello
</MediaQuery>
```

## API

### Props

| Name | Required | Type | Default | Description |
| ---  | ---      | ---  | ---     | ---         |
| at   | true     | String, Number | N/A | Width at which you want the breakpoint to be set. |
| display | true  | String | `'visible'` | Takes two possible values: `'visible'` or `'hidden'`. Tells the component whether to show or hide contents at specified breakpoint. |
| maxWidth | [true] | Boolean | `false` | Render based on `display` prop at or below the `at` prop. Note either `maxWidth` or `minWidth` must be set. |
| minWidth | [true] | Boolean | `false` | Render based on `display` prop at or above the `at` prop. Note either `maxWidth` or `minWidth` must be set. |
| unit | false | String | `'px'` | Unit to measure `at` prop with. Accepts `'px'` or '`em`'. |