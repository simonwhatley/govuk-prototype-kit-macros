# Text input

## Introduction

Use the text input component to let users enter text that’s no longer than a single line, such as their name or phone number.

## Guidance

Find out when to use the text input component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/input/#example-1).

#### Macro
```
{{ govukInput({
	"id": "example-1",
	"name": "national-insurance-number",
	"label": {
		"text": "National Insurance number"
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="example-1" class="form-label">
		National Insurance number
	</label>
	<input id="example-1" class="form-control" name="national-insurance-number" type="text">
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/input/#example-2).

#### Macro
```
{{ govukInput({
	"id": "example-2",
	"name": "national-insurance-number",
	"label": {
		"text": "National Insurance number",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "It’s on your National Insurance card, benefit letter, payslip or P60\. For example, ‘QQ 12 34 56 C’."
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="example-2" class="form-label-bold">
		National Insurance number
		<span for="example-2-hint" class="form-hint">
			It’s on your National Insurance card, benefit letter, payslip or P60. For example, ‘QQ 12 34 56 C’.
		</span>
	</label>
	<input id="example-2" class="form-control" name="national-insurance-number" type="text">
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/input/#example-3).

#### Macro
```
{{ govukInput({
	"id": "example-3",
	"name": "national-insurance-number",
	"label": {
		"text": "National Insurance number",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "It’s on your National Insurance card, benefit letter, payslip or P60\. For example, ‘QQ 12 34 56 C’."
	},
	"errorMessage": {
		"text": "Error message goes here"
	}
}) }}
```

#### Markup
```
<div class="form-group form-group-error">
	<label for="example-3" class="form-label-bold">
		National Insurance number
		<span for="example-3-hint" class="form-hint">
			It’s on your National Insurance card, benefit letter, payslip or P60. For example, ‘QQ 12 34 56 C’.
		</span>
	</label>
	<span id="example-3-error" class="error-message">
	  You must provide a National Insurance number
	</span>
	<input id="example-3" class="form-control form-control-error" name="national-insurance-number" type="text">
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/input/#example-4).

#### Macro
```
{{ govukInput({
	"id": "example-4",
	"name": "national-insurance-number",
	"classes": "form-control-1-2",
	"label": {
		"text": "National Insurance number",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "It’s on your National Insurance card, benefit letter, payslip or P60\. For example, ‘QQ 12 34 56 C’."
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="example-4" class="form-label-bold">
		National Insurance number
		<span for="example-4-hint" class="form-hint">
			It’s on your National Insurance card, benefit letter, payslip or P60. For example, ‘QQ 12 34 56 C’.
		</span>
	</label>
	<input id="example-4" class="form-control form-control-1-2" name="national-insurance-number" type="text">
</div>
```

### Example 5

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/input/#example-5).

#### Macro
```
{{ govukInput({
	"id": "example-5",
	"name": "national-insurance-number",
	"label": {
		"text": "What is your National Insurance number?",
		"classes": "heading-xlarge",
		"isPageHeading": true
	},
	"hint": {
		"text": "It’s on your National Insurance card, benefit letter, payslip or P60\. For example, ‘QQ 12 34 56 C’."
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<h1>
		<label for="example-5" class="heading-xlarge">
			What is your National Insurance number?
			<span for="example-5-hint" class="form-hint">
				It’s on your National Insurance card, benefit letter, payslip or P60. For example, ‘QQ 12 34 56 C’.
			</span>
		</label>
	</h1>
	<input id="example-5" class="form-control" name="national-insurance-number" type="text">
</div>
```

## Arguments

This component accepts the following arguments.

### Container
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|Optional `id` attribute to add to the text input.|
|name|string|Yes|Name attribute for the text input.|
|value|string|No|Optional value of the text input.|
|type|string|No|Type of input control to render. Defaults to text.|
|formGroup|object|No|Options for the form-group wrapper. See [formGroup](#formgroup).|
|label|object|No|Options for the label component (e.g. text). See [label](#label).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|
|classes|string|No|Classes to add to the text input.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the text input.|

### formGroup
|Name|Type|Required|Description|
|---|---|---|---|
|classes|string|No|Classes to add to the form group wrapper.|

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