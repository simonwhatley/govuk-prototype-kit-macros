# Details

## Introduction

Use the details component to make a page easier to scan by letting users reveal more detailed information only if they need it.

## Guidance

Find out when to use the details component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/details/#example-1).

#### Macro
```
{{ govukDetails({
  summaryText: "Help with nationality",
  text: "We need to know your nationality so we can work out which elections you’re entitled to vote in. If you can’t provide your nationality, you’ll have to send copies of identity documents through the post."
}) }}
```

#### Markup
```
<details role="group">
  <summary role="button" aria-controls="details-content-0" aria-expanded="false">
    <span class="summary">
      Help with nationality
    </span>
  </summary>
  <div class="panel panel-border-narrow" id="details-content-0" aria-hidden="true">
    We need to know your nationality so we can work out which elections you’re entitled to vote in. If you can’t provide your nationality, you’ll have to send copies of identity documents through the post.
  </div>
</details>
```

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Optional `id` attribute to add to the `details` element.|
|summaryText|string|Yes|If `summmaryHtml` is set, this is not required. Text to use within the `summary` element (the visible part of the details element). If `summmaryHtml` is provided, the `summaryText` argument will be ignored.|
|summaryHtml|string|Yes|If `summaryText` is set, this is not required. HTML to use within the `summary` element (the visible part of the details element). If `summmaryHtml` is provided, the `summaryText` argument will be ignored.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the disclosed part of the `details` element. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the disclosed part of the `details` element. If `html` is provided, the `text` argument will be ignored.|
|open|boolean|No|If true, `details` element will be expanded.|
|classes|string|No|Classes to add to the `details` element.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the `details` element.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.