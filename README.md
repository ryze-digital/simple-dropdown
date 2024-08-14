# RYZE Digital Simple Dropdown

## Install

```sh
npm i @ryze-digital/simple-dropdown
```

## Usage

### Scss

```scss
@use "@ryze-digital/simple-dropdown";
```

Use the provided `configure` mixin to define your dropdown defaults. A complete list of possible configurations can be
found in [/src/styles/_config.scss](src/styles/_config.scss).

```scss
@include simple-dropdown.configure(...);
```

There is a separate mixin for each element in the accordion so styles can be applied to any markup.

```scss
.simple-dropdown {
    @include simple-dropdown.container();
    .panel {
        @include simple-dropdown.panel();
    }
    button {
        @include simple-dropdown.button();
    }
}
```

## Demos

Checkout this repository and use the [/demos](/demos) folder as document root to see a running demo in the browser.

- [Basic use case](/demos/basic.html)