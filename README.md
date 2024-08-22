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

Use the provided `configure` mixin to define your dropdown defaults.

```scss
@include simple-dropdown.configure(...);
```

<details>
<summary>List of available configure options</summary>

| Option         | Type            | Default  | Description                                                               |
|----------------|-----------------|----------|---------------------------------------------------------------------------|
| icon           | Map             |          | Configure which icons from your icon font should be used                  |
| icon.indicator | String (Quoted) | `null`   | The UTF-8 character of the icon to help understand the button label       |
| icon.closed    | String (Quoted) | `null`   | The UTF-8 character of the icon to use when the dropdown panel is hidden  |
| icon.opened    | String (Quoted) | `null`   | The UTF-8 character of the icon to use when the dropdown panel is visible |
| icon.spacing   | Number          | `null`   | The gap between icons and button label                                    |
| direction      | String (Quoted) | `"down"` | Should the panel drop `"up"` or `"down"`                                  |

Check out [the actual configure mixin](src/styles/_config.scss) for better understanding.
</details>

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