# Label

## Introduction

Use the label component to give the form field a visual label.

## Guidance

Find out when to use the label component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/label/#example-1).

#### Macro
```
{{ govukLabel({
  text: "National Insurance number"
}) }}
```

#### Markup
```
<label class="form-label">
  National Insurance number
</label>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/label/#example-2).

#### Macro
```
{{ govukLabel({
  text: "National Insurance number",
  classes: "form-label-bold"
}) }}
```

#### Markup
```
<label class="form-label-bold">
  National Insurance number
</label>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/label/#example-3).

#### Macro
```
{{ govukLabel({
  text: "What is your National Insurance number?",
  classes: "heading-xlarge",
  isPageHeading: true
}) }}
```

#### Markup
```
<h1>
<label class="heading-xlarge">
  What is your National Insurance number?
</label>
</h1>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|for|string|Yes|The value of the `for` attribute, the `id` of the `input` the label is associated with.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the label. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the label. If `html` is provided, the `text` argument will be ignored.|
|isPageHeading|boolean|No|Whether the label also acts as the heading for the page.|
|classes|string|No|Classes to add to the label tag.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the label tag.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.