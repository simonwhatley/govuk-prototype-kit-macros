# Breadcrumbs

## Introduction

Use the breadcrumbs component to help users to understand where they are within a website’s structure and move between levels.

## Guidance

Find out when to use the breadcrumbs component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/breadcrumbs/#example-1).

#### Macro

```
{{ govukBreadcrumbs({
  "items": [
    {
      text: "Section",
      href: "/section"
    },
    {
      text: "Sub-section",
      href: "/section/sub-section"
    },
    {
      text: "Sub-sub-section"
    }
  ]
}) }}
```

#### Markup

```
<div class="breadcrumbs">
  <ol>
    <li>
      <a href="/section">Section</a>
    </li>
    <li>
      <a href="/section/sub-section">Sub-section</a>
    </li>
    <li aria-current="page">Sub-sub-section</li>
  </ol>
</div>
```

## Arguments

This component accepts the following arguments.

### Container
|Name|Type|Required|Description|
|---|---|---|---|
|items|array|Yes|Array of breadcrumbs item objects. See [items](#items)|
|classes|string|No|Classes to add to the breadcrumbs container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the breadcrumbs container.|

### Items
|Name|Type|Required|Description|
|---|---|---|---|
|href|string|No|Link for the breadcrumbs item. If not specified, the breadcrumbs item is a normal list item.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the breadcrumbs item. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the breadcrumbs item. If `html` is provided, the `text` argument will be ignored.|


*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.