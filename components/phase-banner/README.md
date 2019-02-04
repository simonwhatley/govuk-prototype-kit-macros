# Phase banner

## Introduction

Use the phase banner component to show users your service is still being worked on.

## Guidance

Find out when to use the phase banner component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/phase-banner/#example-1).

#### Macro
```
{{ govukPhaseBanner({
  "tag": {
    "text": "alpha"
  },
  "html": "This is a new service - your <a href="#">feedback</a> will help us to improve it."
}) }}
```

#### Markup
```
<div class="phase-banner">
  <p>
  <strong class="phase-tag">
  alpha
  </strong>
    <span>
      This is a new service - your <a href="#">feedback</a> will help us to improve it.
    </span>
  </p>
</div>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the phase banner. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the phase banner. If `html` is provided, the `text` argument will be ignored.|
|tag|object|No|Options for the tag component. See [tag](https://govuk-prototype-kit-macros.herokuapp.com/components/tag/).|
|classes|string|No|Classes to add to the phase banner container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the phase banner container.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.