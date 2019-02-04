# Radios

## Introduction

Use the radios component when users can only select one option from a list.

## Guidance

Find out when to use the radios component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-1).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-1",
  "name": "example-1",
  "fieldset": {
    "legend": {
      "text": "To what extent do you agree?",
      "classes": "form-label-bold"
    }
  },
  "items": [
    {
      "value": "1",
      "text": "Strongly disagree"
    },
    {
      "value": "2",
      "text": "Disagree"
    },
    {
      "value": "3",
      "text": "Neither agree nor disagree"
    },
    {
      "value": "4",
      "text": "Agree"
    },
    {
      "value": "5",
      "text": "Strongly agree"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <fieldset>
    <legend class="form-label-bold">
      To what extent do you agree?
    </legend>
    <div class="multiple-choice">
      <input type="radio" id="example-1-1" name="example-1" value="1">
      <label for="example-1-1" class="form-label">
        Strongly disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-1-2" name="example-1" value="2">
      <label for="example-1-2" class="form-label">
        Disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-1-3" name="example-1" value="3">
      <label for="example-1-3" class="form-label">
        Neither agree nor disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-1-4" name="example-1" value="4">
      <label for="example-1-4" class="form-label">
        Agree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-1-5" name="example-1" value="5">
      <label for="example-1-5" class="form-label">
        Strongly agree
      </label>
    </div>
  </fieldset>
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-2).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-2",
  "name": "example-2",
  "fieldset": {
    "legend": {
      "text": "To what extent do you agree?",
      "classes": "form-label-bold"
    }
  },
  "hint": {
    "text": "Select the option that is most relevant to you."
  },
  "items": [
    {
      "value": "1",
      "text": "Strongly disagree"
    },
    {
      "value": "2",
      "text": "Disagree"
    },
    {
      "value": "3",
      "text": "Neither agree nor disagree"
    },
    {
      "value": "4",
      "text": "Agree"
    },
    {
      "value": "5",
      "text": "Strongly agree"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <fieldset>
    <legend class="form-label-bold">
      To what extent do you agree?
      <span for="example-2-hint" class="form-hint">
        Select the option that is most relevant to you.
      </span>
    </legend>
    <div class="multiple-choice">
      <input type="radio" id="example-2-1" name="example-2" value="1">
      <label for="example-2-1" class="form-label">
        Strongly disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-2-2" name="example-2" value="2">
      <label for="example-2-2" class="form-label">
        Disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-2-3" name="example-2" value="3">
      <label for="example-2-3" class="form-label">
        Neither agree nor disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-2-4" name="example-2" value="4">
      <label for="example-2-4" class="form-label">
        Agree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-2-5" name="example-2" value="5">
      <label for="example-2-5" class="form-label">
        Strongly agree
      </label>
    </div>
  </fieldset>
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-3).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-3",
  "name": "example-3",
  "fieldset": {
    "legend": {
      "text": "To what extent do you agree?",
      "classes": "form-label-bold"
    }
  },
  "hint": {
    "text": "Select the option that is most relevant to you"
  },
  "errorMessage": {
    "text": "Choose an answer"
  },
  "items": [
    {
      "value": "1",
      "text": "Strongly disagree"
    },
    {
      "value": "2",
      "text": "Disagree"
    },
    {
      "value": "3",
      "text": "Neither agree nor disagree"
    },
    {
      "value": "4",
      "text": "Agree"
    },
    {
      "value": "5",
      "text": "Strongly agree"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group form-group-error">
  <fieldset>
    <legend class="form-label-bold">
      To what extent do you agree?
      <span for="example-3-hint" class="form-hint">
        Select the option that is most relevant to you
      </span>
      <span id="example-3-error" class="error-message">
        Choose an answer
      </span>
    </legend>
    <div class="multiple-choice">
      <input type="radio" id="example-3-1" name="example-3" value="1">
      <label for="example-3-1" class="form-label">
        Strongly disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-3-2" name="example-3" value="2">
      <label for="example-3-2" class="form-label">
        Disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-3-3" name="example-3" value="3">
      <label for="example-3-3" class="form-label">
        Neither agree nor disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-3-4" name="example-3" value="4">
      <label for="example-3-4" class="form-label">
        Agree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-3-5" name="example-3" value="5">
      <label for="example-3-5" class="form-label">
        Strongly agree
      </label>
    </div>
  </fieldset>
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-4).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-4",
  "name": "example-4",
  "fieldset": {
    "legend": {
      "text": "To what extent do you agree?",
      "classes": "form-label-bold"
    }
  },
  "hint": {
    "text": "Select the option that is most relevant to you."
  },
  "items": [
    {
      "value": "1",
      "text": "Strongly disagree",
      "disabled": true
    },
    {
      "value": "2",
      "text": "Disagree",
      "disabled": true
    },
    {
      "value": "3",
      "text": "Neither agree nor disagree",
      "disabled": true
    },
    {
      "value": "4",
      "text": "Agree",
      "disabled": true
    },
    {
      "value": "5",
      "text": "Strongly agree",
      "disabled": true
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <fieldset>
    <legend class="form-label-bold">
      To what extent do you agree?
      <span for="example-4-hint" class="form-hint">
        Select the option that is most relevant to you.
      </span>
    </legend>
    <div class="multiple-choice">
      <input type="radio" id="example-4-1" name="example-4" value="1" disabled>
      <label for="example-4-1" class="form-label">
        Strongly disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-4-2" name="example-4" value="2" disabled>
      <label for="example-4-2" class="form-label">
        Disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-4-3" name="example-4" value="3" disabled>
      <label for="example-4-3" class="form-label">
        Neither agree nor disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-4-4" name="example-4" value="4" disabled>
      <label for="example-4-4" class="form-label">
        Agree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-4-5" name="example-4" value="5" disabled>
      <label for="example-4-5" class="form-label">
        Strongly agree
      </label>
    </div>
  </fieldset>
</div>
```

### Example 5

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-5).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-5",
  "name": "example-5",
  "fieldset": {
    "legend": {
      "text": "To what extent do you agree?",
      "classes": "form-label-bold"
    }
  },
  "hint": {
    "text": "Select the option that is most relevant to you."
  },
  "errorMessage": {
    "text": "Choose an answer."
  },
  "items": [
    {
      "value": "1",
      "text": "Strongly disagree"
    },
    {
      "value": "2",
      "text": "Disagree"
    },
    {
      "value": "3",
      "text": "Neither agree nor disagree",
      "checked": true
    },
    {
      "value": "4",
      "text": "Agree",
    },
    {
      "value": "5",
      "text": "Strongly agree"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <fieldset>
    <legend class="form-label-bold">
      To what extent do you agree?
      <span for="example-5-hint" class="form-hint">
        Select the option that is most relevant to you.
      </span>
    </legend>
    <div class="multiple-choice">
      <input type="radio" id="example-5-1" name="example-5" value="1">
      <label for="example-5-1" class="form-label">
        Strongly disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-5-2" name="example-5" value="2">
      <label for="example-5-2" class="form-label">
        Disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-5-3" name="example-5" value="3" checked>
      <label for="example-5-3" class="form-label">
        Neither agree nor disagree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-5-4" name="example-5" value="4">
      <label for="example-5-4" class="form-label">
        Agree
      </label>
    </div>
    <div class="multiple-choice">
      <input type="radio" id="example-5-5" name="example-5" value="5">
      <label for="example-5-5" class="form-label">
        Strongly agree
      </label>
    </div>
  </fieldset>
</div>
```

### Example 6

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/radios/#example-6).

#### Macro
```
{{ govukRadios({
  "idPrefix": "example-6",
  "name": "example-6",
  "fieldset": {
    "legend": {
      "text": "How do you want to be contacted?",
      "classes": "form-label-bold"
    }
  },
  "hint": {
    "text": "Select the option most relevant to you."
  },
  "items": [
    {
      "value": "email",
      "text": "Email",
      "conditional": {
        "html": email_panel_html
      }
    },
    {
      "value": "phone",
      "text": "Phone",
      "conditional": {
        "html": phone_panel_html
      }
    },
    {
      "value": "text",
      "text": "Text message",
      "conditional": {
        "html": message_panel_html
      }
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <fieldset>
    <legend class="form-label-bold">
      How do you want to be contacted?
      <span for="example-6-hint" class="form-hint">
        Select the option most relevant to you.
      </span>
    </legend>
    <div class="multiple-choice" data-target="example-6-1-panel">
      <input type="radio" id="example-6-1" name="example-6" value="email" aria-controls="example-6-1-panel" aria-expanded="false">
      <label for="example-6-1" class="form-label">
        Email
      </label>
    </div>
    <div class="panel panel-border-narrow js-hidden" id="example-6-1-panel" aria-hidden="true">
      <label class="form-label" for="contact-email">Email address</label>
      <input class="form-control" name="contact-email" type="text" id="contact-email">
    </div>
    <div class="multiple-choice" data-target="example-6-2-panel">
      <input type="radio" id="example-6-2" name="example-6" value="phone" aria-controls="example-6-2-panel" aria-expanded="false">
      <label for="example-6-2" class="form-label">
        Phone
      </label>
    </div>
    <div class="panel panel-border-narrow js-hidden" id="example-6-2-panel" aria-hidden="true">
      <label class="form-label" for="contact-phone">Phone number</label>
      <input class="form-control" name="contact-phone" type="text" id="contact-phone">
    </div>
    <div class="multiple-choice" data-target="example-6-3-panel">
      <input type="radio" id="example-6-3" name="example-6" value="text" aria-controls="example-6-3-panel" aria-expanded="false">
      <label for="example-6-3" class="form-label">
        Text message
      </label>
    </div>
    <div class="panel panel-border-narrow js-hidden" id="example-6-3-panel" aria-hidden="true">
      <label class="form-label" for="contact-mobile">Mobile phone number</label>
      <input class="form-control" name="contact-mobile" type="text" id="contact-mobile">
    </div>
  </fieldset>
</div>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|idPrefix|string|No|String to prefix id for each radio item if no id is specified on each item. If not passed, fall back to using the name option instead.|
|name|string|Yes|Name attribute for all radio items.|
|fieldset|object|No|Options for the fieldset component (e.g. legend). See [fieldset](#fieldset).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|
|items|array|Yes|Array of radio items objects. See [items](#items).|
|classes|string|No|Classes to add to the radioes container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the radio's container.|

### Items
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Specific id attribute for the radio item. If omitted, then `idPrefix` option will be applied.|
|name|string|Yes|Specific name for the radio item. If omitted, then component global `name` string will be applied.|
|value|string|Yes|Value for the radio input.|
|label|object|No|Provide attributes and classes to each radio item label. See [label](#label).|
|hint|object|No|Provide hint to each radio item. See [hint](#hint).|
|checked|boolean|No|If true, radio will be checked.|
|disabled|boolean|No|If true, radio will be disabled.|
|conditional|object|No|Provide content for the conditional reveal. See [conditional](#conditional).|
|attributes|object|No|HTML attributes (for example data attributes) to add to the radio input tag.|

#### Conditional
|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the conditional block. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the conditional block. If `html` is provided, the `text` argument will be ignored.|

### Fieldset
|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the legend. If `html` is provided, the `text` argument will be ignored.|
|isPageHeading|boolean|No|Whether the legend also acts as the heading for the page.|
|classes|string|No|Classes to add to the legend.|

### Label
|Name|Type|Required|Description|
|---|---|---|---|
|for|string|Yes|The value of the `for` attribute, the `id` of the `input` the label is associated with.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the label. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the label. If `html` is provided, the `text` argument will be ignored.|
|isPageHeading|boolean|No|Whether the label also acts as the heading for the page.|
|classes|string|No|Classes to add to the label tag.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the label tag.|

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