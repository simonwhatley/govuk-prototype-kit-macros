# Warning text

## Introduction

Use the warning text component when you need to warn users about something important, such as legal consequences of an action, or lack of action, that they might take.

## Guidance

Find out when to use the warning text component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/warning-text/#example-1).

#### Macro
```
{{ govukWarningText({
  text: "You can be fined up to £5,000 if you don’t register."
}) }}
```

#### Markup
```
<div class="notice ">
  <i class="icon icon-important">
    <span class="visually-hidden">Warning</span>
  </i>
  <strong class="bold-small">
    You can be fined up to £5,000 if you don’t register.
  </strong>
</div>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the warning text component. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the warning text component. If `html` is provided, the `text` argument will be ignored.|
|iconFallbackText|string|No|The fallback text for the icon. Default: "Warning".|
|classes|string|No|Classes to add to the warning text component.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the warning text component.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.