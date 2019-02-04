# Button

## Introduction

Use the button component to help users carry out an action on a GOV.UK page like starting an application or saving their information.

## Guidance

Find out when to use the button component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/button/#example-1).

#### Macro

```
{{ govukButton({
	"text": "Save and continue",
	"classes": "button button-primary"
}) }}
```

#### Markup

```
<button type="submit" class="button button-primary">
  Save and continue
</button>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/button/#example-2).

#### Macro

```
{{ govukButton({
	"element": "input",
	"type": "submit",
	"text": "Save and continue",
	"classes": "button button-primary"
}) }}
```

#### Markup

```
<input value="Save and continue" type="submit" class="button button-primary">
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/button/#example-3).

#### Macro

```
{{ govukButton({
	"element": "a",
	"text": "Start now",
	"classes": "button button-start",
	"href": "/"
}) }}
```

#### Markup

```
<a href="/" role="button" class="button button-start">
  Start now
</a>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|element|string|Yes|Whether to use an `input`, `button` or `a` element to create the button.|
|name|string|Yes|Name for the `input` or `button`. This has no effect on `a` elements.|
|type|string|Yes|Type of `input` or `button` – `button`, `submit` or `reset`. Defaults to `submit`. This has no effect on `a` elements.|
|value|string|Yes|Value for the `button` tag. This has no effect on `a` or `input` elements.|
|text|string|No|If `html` is set, this is not required. Text to use within the button component. If `html` is provided, the `text` argument will be ignored. This argument has no effect if element is set to `input`.|
|html|string|No|If `text` is set, this is not required. HTML to use within the button component. If `html` is provided, the `text` argument will be ignored. This argument has no effect if element is set to `input`.|
|href|string|No|The URL that the button should link to.|
|disabled|boolean|No|Whether the button should be disabled. For button and input elements, `disabled` and `aria-disabled` attributes will be set automatically.|
|classes|string|No|Classes to add to the button component.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the button component.|


*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.