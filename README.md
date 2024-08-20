# RYZE Digital Simple Dropdown

![Run linter(s) workflow status](https://github.com/ryze-digital/simple-dropdown/actions/workflows/run-lint.yml/badge.svg)

## Install

```sh
npm i @ryze-digital/simple-dropdown
```

## Usage

### HTML

You can change the HTML to your needs if necessary, as long as you include the mixins (see Scss) correctly.

```html
<div class="simple-dropdown" tabindex="0">
    <button type="button">
        <span>Your button label</span>
    </button>
    <div class="panel">
        Your dropdown content
    </div>
</div>
```

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