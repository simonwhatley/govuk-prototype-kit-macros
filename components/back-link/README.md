# Back link

## Introduction

Use the back link component to help users go back to the previous page in a multi-page transaction.

## Guidance

Find out when to use the back link component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/back-link/#example-1).

#### Macro

```
{{ govukBackLink({
  "href": "#",
  "text": "Back to home"
}) }}
```

#### Markup

```
<a class="link-back" href="#">Back to home</a>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|href|string|Yes|The value of the link href attribute.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the back link component. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the back link component. If `html` is provided, the `text` argument will be ignored.|
|classes|string|No|Classes to add to the back link component.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the back link component.|


*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.