# Select

## Introduction

Use the select component to allow users to choose an option from a long list.

## Guidance

Find out when to use the select component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

The select component should only be used as a last resort in public-facing services because research shows that some users find selects very difficult to use.

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-1).

#### Macro
```
{{ govukSelect({
  id: "example-1",
  name: "example-1",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-1" class="form-label-bold">
    Label text goes here
  </label>
  <select id="example-1" class="form-control" name="example-1">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-2).

#### Macro
```
{{ govukSelect({
  id: "example-2",
  name: "example-2",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-2" class="form-label-bold">
    Label text goes here
    <span for="example-2-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <select id="example-2" class="form-control" name="example-2">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-3).

#### Macro
```
{{ govukSelect({
  id: "example-3",
  name: "example-3",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  errorMessage: {
    text: "Error message goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}

```

#### Markup
```
<div class="form-group form-group-error">
  <label for="example-3" class="form-label-bold">
    Label text goes here
    <span for="example-3-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <span id="example-3-error" class="error-message">
    Error message goes here
  </span>
  <select id="example-3" class="form-control form-control-error" name="example-3">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-4).

#### Macro
```
{{ govukSelect({
  id: "example-4",
  name: "example-4",
  classes: "form-control-3-4",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-4" class="form-label-bold">
    Label text goes here
    <span for="example-4-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <select id="example-4" class="form-control form-control-3-4" name="example-4">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 5

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-5).

#### Macro
```
{{ govukSelect({
  id: "example-5",
  name: "example-5",
  label: {
    text: "Label text goes here",
    classes: "heading-xlarge",
    isPageHeading: true
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <h1>
    <label for="example-5" class="heading-xlarge">
      Label text goes here
      <span for="example-5-hint" class="form-hint">
        Hint text goes here
      </span>
    </label>
  </h1>
  <select id="example-5" class="form-control" name="example-5">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 6

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-6).

#### Macro
```
{{ govukSelect({
  id: "example-6",
  name: "example-6",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1",
      selected: true
    },
    {
      value: 2,
      text: "Option 2"
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-6" class="form-label-bold">
    Label text goes here
    <span for="example-6-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <select id="example-6" class="form-control" name="example-6">
    <option value="">Select an option</option>
    <option value="1" selected>Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 7

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-7).

#### Macro
```
{{ govukSelect({
  id: "example-7",
  name: "example-7",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1"
    },
    {
      value: 2,
      text: "Option 2",
      disabled: true
    },
    {
      value: 3,
      text: "Option 3"
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-7" class="form-label-bold">
    Label text goes here
    <span for="example-7-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <select id="example-7" class="form-control" name="example-7">
    <option value="">Select an option</option>
    <option value="1">Option 1</option>
    <option value="2" disabled>Option 2</option>
    <option value="3">Option 3</option>
  </select>
</div>
```

### Example 8

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/select/#example-8).

#### Macro
```
{{ govukSelect({
  id: "example-8",
  name: "example-8",
  label: {
    text: "Label text goes here",
    classes: "form-label-bold"
  },
  hint: {
    text: "Hint text goes here"
  },
  items: [
    {
      value: "",
      text: "Select an option"
    },
    {
      value: 1,
      text: "Option 1",
      attributes: {
        data-destination: true,
        data-cost: true
      }
    },
    {
      value: 2,
      text: "Option 2",
      attributes: {
        data-destination: false,
        data-cost: false
      }
    },
    {
      value: 3,
      text: "Option 3",
      attributes: {
        data-destination: true,
        data-cost: true
      }
    }
  ]
}) }}
```

#### Markup
```
<div class="form-group">
  <label for="example-8" class="form-label-bold">
    Label text goes here
    <span for="example-8-hint" class="form-hint">
      Hint text goes here
    </span>
  </label>
  <select id="example-8" class="form-control" name="example-8">
    <option value="">Select an option</option>
    <option value="1" data-destination="true" data-cost="true">Option 1</option>
    <option value="2" data-destination="false" data-cost="false">Option 2</option>
    <option value="3" data-destination="true" data-cost="true">Option 3</option>
  </select>
</div>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|Optional `id` attribute to add to the `select`.|
|name|string|Yes|Name attribute for the `select`.|
|label|object|No|Options for the label component (e.g. text). See [label](#label).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|
|items|array|Yes|Array of option items objects. See [items](#items).|
|classes|string|No|Classes to add to the `select`.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the `select`.|

### Items
|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|Text for the option item.|
|value|string|No|Value for the option item.|
|selected|boolean|No|If true, option item will be selected.|
|disabled|boolean|No|If true, option item will be disabled.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the option item.|

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