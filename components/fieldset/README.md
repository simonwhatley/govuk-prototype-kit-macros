# Fieldset

## Introduction

Use the fieldset component to group related form inputs.

## Guidance

Find out when to use the fieldset component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/fieldset/#example-1).

#### Macro
```
{% call govukFieldset({
  legend: {
    text: "What is your address?",
    classes: "heading-xlarge",
    isPageHeading: false
  }
}) %}

  {{ govukInput({
    id: "address-line-1",
    name: "address-line-1",
    label: {
      html: 'Building and street <span class="visually-hidden">line 1 of 2</span>',
      classes: "form-label-bold"
    },
    classes: "form-control-2-3"
  }) }}

  {{ govukInput({
    id: "address-line-2",
    name: "address-line-2",
    label: {
      html: '<span class="visually-hidden">Building and street line 2 of 2</span>',
      classes: "form-label-bold"
    },
    classes: "form-control-2-3"
  }) }}

  {{ govukInput({
    id: "address-town",
    name: "address-town",
    label: {
      text: "Town or city",
      classes: "form-label-bold"
    },
    classes: "form-control-1-2"
  }) }}

  {{ govukInput({
    id: "address-county",
    name: "address-county",
    label: {
      text: "County",
      classes: "form-label-bold"
    },
    classes: "form-control-1-2"
  }) }}

  {{ govukInput({
    id: "address-postcode",
    name: "address-postcode",
    label: {
      text: "Postcode",
      classes: "form-label-bold"
    },
    classes: "form-control-1-4"
  }) }}

{% endcall %}
```

#### Markup
```
<fieldset>
  <legend class="heading-xlarge">
    What is your address?
  </legend>
  <div class="form-group">
    <label for="address-line-1" class="form-label-bold">
      Building and street <span class="visually-hidden">line 1 of 2</span>
    </label>
    <input id="address-line-1" class="form-control form-control-2-3" name="address-line-1" type="text">
  </div>
  <div class="form-group">
    <label for="address-line-2" class="form-label-bold">
      <span class="visually-hidden">Building and street line 2 of 2</span>
    </label>
    <input id="address-line-2" class="form-control form-control-2-3" name="address-line-2" type="text">
  </div>
  <div class="form-group">
    <label for="address-town" class="form-label-bold">
      Town or city
    </label>
    <input id="address-town" class="form-control form-control-1-2" name="address-town" type="text">
  </div>
  <div class="form-group">
    <label for="address-county" class="form-label-bold">
      County
    </label>
    <input id="address-county" class="form-control form-control-1-2" name="address-county" type="text">
  </div>
  <div class="form-group">
    <label for="address-postcode" class="form-label-bold">
      Postcode
    </label>
    <input id="address-postcode" class="form-control form-control-1-4" name="address-postcode" type="text">
  </div>
</fieldset>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|isPageHeading|boolean|No|Whether the legend also acts as the heading for the page.|
|classes|string|No|Classes to add to the legend.|

### Legend

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|isPageHeading|boolean|No|Whether the legend also acts as the heading for the page.|
|classes|string|No|Classes to add to the legend.|

### Hint
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Optional `id` attribute to add to the hint span tag.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the hint. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the hint. If `html` is provided, the `text` argument will be ignored.|
|classes|string|No|Classes to add to the hint span tag.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the hint span tag.|

### errorMessage
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Optional `id` attribute to add to the error span tag.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the error. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the error. If `html` is provided, the `text` argument will be ignored.|
|classes|string|No|Classes to add to the error span tag.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the error span tag.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.