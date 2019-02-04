# Date input

## Introduction

Use date input component to help users enter a dates, for example: Date of birth.

## Guidance

Find out when to use the date input component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/date-input/#example-1).

#### Macro
```
{{ govukDateInput({
	"id": "date-of-birth",
	"fieldset": {
		"legend": {
			"text": "What is your date of birth?"
		}
	},
	"hint": {
		"text": "For example, 31 3 1980"
	},
	"items": [
		{
			"id": "dob-day",
			"name": "dob-day",
			"formGroup": {
				"classes": "form-group-day"
			},
			"type": "number",
			"label": {
				"text": "Day"
			}
		},
		{
			"id": "dob-month",
			"name": "dob-month",
			"formGroup": {
				"classes": "form-group-month"
			},
			"type": "number",
			"label": {
				"text": "Month"
			}
		},
		{
			"id": "dob-year",
			"name": "dob-year",
			"formGroup": {
				"classes": "form-group-year"
			},
			"type": "number",
			"label": {
				"text": "Year"
			}
		}
	]
}) }}
```

#### Markup
```
<div class="form-group" role="group">
  <fieldset>
    <legend class="form-label-bold">
      What is your date of birth?
      <span for="date-of-birth-hint" class="form-hint">
        For example, 31 3 1980
      </span>
    </legend>
    <div class="form-date">
      <div class="form-group form-group-day">
        <label for="dob-day" class="form-label">
          Day
        </label>
        <input class="form-control" id="dob-day" name="dob-day" type="number">
      </div>
      <div class="form-group form-group-month">
        <label for="dob-month" class="form-label">
          Month
        </label>
        <input class="form-control" id="dob-month" name="dob-month" type="number">
      </div>
      <div class="form-group form-group-year">
        <label for="dob-year" class="form-label">
          Year
        </label>
        <input class="form-control" id="dob-year" name="dob-year" type="number">
      </div>
    </div>
  </fieldset>
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/date-input/#example-2).

#### Macro
```
{{ govukDateInput({
	"id": "date-of-birth",
	"fieldset": {
		"legend": {
			"text": "What is your date of birth?"
		}
	},
	"hint": {
		"text": "For example, 31 3 1980"
	},
	"errorMessage": {
		"text": "Error message goes here"
	},
	"items": [
		{
			"id": "dob-day",
			"name": "dob-day",
			"formGroup": {
				"classes": "form-group-day"
			},
			"type": "number",
			"label": {
				"text": "Day"
			}
		},
		{
			"id": "dob-month",
			"name": "dob-month",
			"formGroup": {
				"classes": "form-group-month"
			},
			"type": "number",
			"label": {
				"text": "Month"
			}
		},
		{
			"id": "dob-year",
			"name": "dob-year",
			"formGroup": {
				"classes": "form-group-year"
			},
			"type": "number",
			"label": {
				"text": "Year"
			}
		}
	]
}) }}
```

#### Markup
```
<div class="form-group form-group-error" role="group">
  <fieldset>
    <legend class="form-label-bold">
      What is your date of birth?
      <span for="date-of-birth-hint" class="form-hint">
        For example, 31 3 1980
      </span>
      <span id="date-of-birth-error" class="error-message">
        Error message goes here
      </span>
    </legend>
    <div class="form-date">
      <div class="form-group form-group-day">
        <label for="dob-day" class="form-label">
          Day
        </label>
        <input class="form-control form-control-error" id="dob-day" name="dob-day" type="number">
      </div>
      <div class="form-group form-group-month">
        <label for="dob-month" class="form-label">
          Month
        </label>
        <input class="form-control form-control-error" id="dob-month" name="dob-month" type="number">
      </div>
      <div class="form-group form-group-year">
        <label for="dob-year" class="form-label">
          Year
        </label>
        <input class="form-control form-control-error" id="dob-year" name="dob-year" type="number">
      </div>
    </div>
  </fieldset>
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/date-input/#example-3).

#### Macro
```
{{ govukDateInput({
	"id": "date-of-birth",
	"fieldset": {
		"legend": {
			"text": "What is your date of birth?"
		}
	},
	"hint": {
		"text": "For example, 31 3 1980"
	},
	"items": [
		{
			"id": "dob-day",
			"name": "dob-day",
			"formGroup": {
				"classes": "form-group-day"
			},
			"type": "number",
			"label": {
				"text": "Day"
			},
			"attributes": {
				"pattern": "[0-9]*",
				"max": "31",
				"min": "1"
			}
		},
		{
			"id": "dob-month",
			"name": "dob-month",
			"formGroup": {
				"classes": "form-group-month"
			},
			"type": "number",
			"label": {
				"text": "Month"
			},
			"attributes": {
				"pattern": "[0-9]*",
				"max": "31",
				"min": "1"
			}
		},
		{
			"id": "dob-year",
			"name": "dob-year",
			"formGroup": {
				"classes": "form-group-year"
		},
			"type": "number",
			"label": {
				"text": "Year"
			},
			"attributes": {
				"pattern": "[0-9]*",
				"max": "2019",
				"min": "1900"
			}
		}
	]
}) }}
```

#### Markup
```
<div class="form-group" role="group">
  <fieldset>
    <legend class="form-label-bold">
      What is your date of birth?
      <span for="date-of-birth-hint" class="form-hint">
        For example, 31 3 1980
      </span>
    </legend>
    <div class="form-date">
      <div class="form-group form-group-day">
        <label for="dob-day" class="form-label">
          Day
        </label>
        <input class="form-control" id="dob-day" name="dob-day" type="number" pattern="[0-9]*" max="31" min="1">
      </div>
      <div class="form-group form-group-month">
        <label for="dob-month" class="form-label">
          Month
        </label>
        <input class="form-control" id="dob-month" name="dob-month" type="number" pattern="[0-9]*" max="31" min="1">
      </div>
      <div class="form-group form-group-year">
        <label for="dob-year" class="form-label">
          Year
        </label>
        <input class="form-control" id="dob-year" name="dob-year" type="number" pattern="[0-9]*" max="2019" min="1900">
      </div>
    </div>
  </fieldset>
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/date-input/#example-4).

#### Macro
```
{{ govukDateInput({
	"id": "date-of-birth",
	"fieldset": {
		"legend": {
			"text": "What is your date of birth?"
		}
	},
	"hint": {
		"text": "For example, 31 3 1980"
	},
	"items": [
		{
			"id": "dob-day",
			"name": "dob-day",
			"formGroup": {
				"classes": "form-group-day"
			},
			"type": "number",
			"label": {
				"text": "Day"
			},
			"value": 1
		},
		{
			"id": "dob-month",
			"name": "dob-month",
			"formGroup": {
				"classes": "form-group-month"
			},
			"type": "number",
			"label": {
				"text": "Month"
			},
			"value": 1
		},
		{
			"id": "dob-year",
			"name": "dob-year",
			"formGroup": {
				"classes": "form-group-year"
			},
			"type": "number",
			"label": {
				"text": "Year"
			},
			"value": 1970
		}
	]
}) }}
```

#### Markup
```
<div class="form-group" role="group">
  <fieldset>
    <legend class="form-label-bold">
      What is your date of birth?
      <span for="date-of-birth-hint" class="form-hint">
        For example, 31 3 1980
      </span>
    </legend>
    <div class="form-date">
      <div class="form-group form-group-day">
        <label for="dob-day" class="form-label">
          Day
        </label>
        <input class="form-control" id="dob-day" name="dob-day" type="number" value="1">
      </div>
      <div class="form-group form-group-month">
        <label for="dob-month" class="form-label">
          Month
        </label>
        <input class="form-control" id="dob-month" name="dob-month" type="number" value="1">
      </div>
      <div class="form-group form-group-year">
        <label for="dob-year" class="form-label">
          Year
        </label>
        <input class="form-control" id="dob-year" name="dob-year" type="number" value="1970">
      </div>
    </div>
  </fieldset>
</div>
```

## Arguments

This component accepts the following arguments.

### Container
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|Optional `id` attribute to add to the main component and compose the `id` attribute for each item.|
|items|array|Yes|Array of input objects. See [items](#items).|
|formGroup|object|No|Options for the form-group wrapper. Defaults to `form-group`. See [formGroup](#formgroup).|
|fieldset|object|No|Options for the fieldset component (e.g. legend). See [fieldset](#fieldset).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|

### Items
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|Optional `id` attribute to add to the text input.|
|name|string|Yes|Name attribute for the text input.|
|value|string|No|Optional value of the text input.|
|label|object|No|Options for the label component (e.g. text). See [label](#label).|
|formGroup|object|No|Options for the form-group wrapper. Defaults to `form-group`. See [formGroup](#formgroup).|
|classes|string|No|Classes to add to the text input. Defaults to `form-control`.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the text input.|

### formGroup
|Name|Type|Required|Description|
|---|---|---|---|
|classes|string|No|Classes to add to the form group wrapper.|

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