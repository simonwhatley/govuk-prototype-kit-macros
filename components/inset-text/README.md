# Inset text

## Introduction

Use the inset text component to differentiate a block of text from the surrounding content.

## Guidance

Find out when to use the inset text component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/inset-text/#example-1).

#### Macro
```
{{ govukInsetText({
  "text": "It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application."
}) }}

```

#### Markup
```
<div class="panel panel-border-wide">
  It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.
</div>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Optional `id` attribute to add to the inset text container.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the inset text container. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the inset text container. If `html` is provided, the `text` argument will be ignored.|
|classes|string|No|Classes to add to the anchor tag.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the anchor tag.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.