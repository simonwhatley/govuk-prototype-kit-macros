# Checkboxes

## Introduction

Use the checkbox component to allow users to select one or more options.

## Guidance

Find out when to use the checkboxes component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/checkboxes/#example-1).

#### Macro
```
{{ govukCheckboxes({
	"idPrefix": "nationality",
	"name": "nationality",
	"fieldset": {
		"legend": {
			"text": "What is your nationality?",
			"classes": "form-label-bold"
		}
	},
	"items": [
		{
			"value": "british",
			"text": "British"
		},
		{
			"value": "french",
			"text": "French"
		},
		{
			"value": "german",
			"text": "German"
		},
		{
			"value": "italian",
			"text": "Italian"
		},
		{
			"value": "spanish",
			"text": "Spanish"
		},
		{
			"value": "other",
			"text": "Citizen of another country"
		}
	]
}) }}
```
#### Markup
```
<div class="form-group">
	<fieldset>
		<legend class="form-label-bold">
			What is your nationality?
		</legend>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-1" name="nationality" value="british">
			<label for="checkboxes-example-1-1" class="form-label">
				British
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-2" name="nationality" value="french">
			<label for="checkboxes-example-1-2" class="form-label">
				French
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-3" name="nationality" value="german">
			<label for="checkboxes-example-1-3" class="form-label">
				German
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-4" name="nationality" value="italian">
			<label for="checkboxes-example-1-4" class="form-label">
				Italian
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-5" name="nationality" value="spanish">
			<label for="checkboxes-example-1-5" class="form-label">
				Spanish
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-1-6" name="nationality" value="other">
			<label for="checkboxes-example-1-6" class="form-label">
				Citizen of another country
			</label>
		</div>
	</fieldset>
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/checkboxes/#example-2).

#### Macro
```
{{ govukCheckboxes({
	"idPrefix": "nationality",
	"name": "nationality",
	"fieldset": {
		"legend": {
			"text": "What is your nationality?",
			"classes": "form-label-bold"
		}
	},
	"hint": {
		"text": "If you have dual nationality, select all options that are relevant to you."
	},
	"items": [
		{
			"value": "british",
			"text": "British"
		},
		{
			"value": "french",
			"text": "French"
		},
		{
			"value": "german",
			"text": "German"
		},
		{
			"value": "italian",
			"text": "Italian"
		},
		{
			"value": "spanish",
			"text": "Spanish"
		},
		{
			"value": "other",
			"text": "Citizen of another country"
		}
	]
}) }}
```
#### Markup
```
<div class="form-group">
	<fieldset>
		<legend class="form-label-bold">
			What is your nationality?
			<span class="form-hint">
				If you have dual nationality, select all options that are relevant to you.
			</span>
		</legend>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-1" name="nationality" value="british">
			<label for="checkboxes-example-2-1" class="form-label">
				British
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-2" name="nationality" value="french">
			<label for="checkboxes-example-2-2" class="form-label">
				French
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-3" name="nationality" value="german">
			<label for="checkboxes-example-2-3" class="form-label">
				German
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-4" name="nationality" value="italian">
			<label for="checkboxes-example-2-4" class="form-label">
				Italian
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-5" name="nationality" value="spanish">
			<label for="checkboxes-example-2-5" class="form-label">
				Spanish
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-2-6" name="nationality" value="other">
			<label for="checkboxes-example-2-6" class="form-label">
				Citizen of another country
			</label>
		</div>
	</fieldset>
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/checkboxes/#example-3).

#### Macro
```
{{ govukCheckboxes({
	"idPrefix": "nationality",
	"name": "nationality",
	"fieldset": {
		"legend": {
			"text": "What is your nationality?",
			"classes": "form-label-bold"
		}
	},
	"hint": {
		"text": "If you have dual nationality, select all options that are relevant to you."
	},
	"errorMessage": {
		"text": "Choose at least one nationality."
	},
	"items": [
		{
			"value": "british",
			"text": "British"
		},
		{
			"value": "french",
			"text": "French"
		},
		{
			"value": "german",
			"text": "German"
		},
		{
			"value": "italian",
			"text": "Italian"
		},
		{
			"value": "spanish",
			"text": "Spanish"
		},
		{
			"value": "other",
			"text": "Citizen of another country"
		}
	]
}) }}
```
#### Markup
```
<div class="form-group form-group-error">
	<fieldset>
		<legend class="form-label-bold">
			What is your nationality?
			<span class="form-hint">
				If you have dual nationality, select all options that are relevant to you.
			</span>
			<span id="checkboxes-example-3-error" class="error-message">
			  Choose at least one nationality.
			</span>
		</legend>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-1" name="nationality" value="british">
			<label for="checkboxes-example-3-1" class="form-label">
				British
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-2" name="nationality" value="french">
			<label for="checkboxes-example-3-2" class="form-label">
				French
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-3" name="nationality" value="german">
			<label for="checkboxes-example-3-3" class="form-label">
				German
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-4" name="nationality" value="italian">
			<label for="checkboxes-example-3-4" class="form-label">
				Italian
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-5" name="nationality" value="spanish">
			<label for="checkboxes-example-3-5" class="form-label">
				Spanish
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-3-6" name="nationality" value="other">
			<label for="checkboxes-example-3-6" class="form-label">
				Citizen of another country
			</label>
		</div>
	</fieldset>
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/checkboxes/#example-4).

#### Macro
```
{{ govukCheckboxes({
	"idPrefix": "nationality",
	"name": "nationality",
	"fieldset": {
		"legend": {
			"text": "What is your nationality?",
			"classes": "form-label-bold"
		}
	},
	"hint": {
		"text": "If you have dual nationality, select all options that are relevant to you."
	},
	"items": [
		{
			"value": "british",
			"text": "British"
		},
		{
			"value": "french",
			"text": "French"
		},
		{
			"value": "german",
			"text": "German"
		},
		{
			"value": "italian",
			"text": "Italian"
		},
		{
			"value": "spanish",
			"text": "Spanish"
		},
		{
			"value": "other",
			"text": "Citizen of another country",
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
			What is your nationality?
			<span class="form-hint">
				If you have dual nationality, select all options that are relevant to you.
			</span>
		</legend>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-1" name="nationality" value="british">
			<label for="checkboxes-example-4-1" class="form-label">
				British
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-2" name="nationality" value="french">
			<label for="checkboxes-example-4-2" class="form-label">
				French
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-3" name="nationality" value="german">
			<label for="checkboxes-example-4-3" class="form-label">
				German
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-4" name="nationality" value="italian">
			<label for="checkboxes-example-4-4" class="form-label">
				Italian
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-5" name="nationality" value="spanish">
			<label for="checkboxes-example-4-5" class="form-label">
				Spanish
			</label>
		</div>
		<div class="multiple-choice">
			<input type="checkbox" id="checkboxes-example-4-6" name="nationality" value="other" disabled>
			<label for="checkboxes-example-4-6" class="form-label">
				Citizen of another country
			</label>
		</div>
	</fieldset>
</div>
```

### Example 5

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/checkboxes/#example-5).

#### Macro
```
{{ govukCheckboxes({
	"idPrefix": "checkboxes-example-5",
	"name": "contact",
	"fieldset": {
		"legend": {
			"text": "How do you want to be contacted?",
			"classes": "form-label-bold"
		}
	},
	"hint": {
		"text": "Select all options that are relevant to you."
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
			<span class="form-hint">
				Select all options that are relevant to you.
			</span>
		</legend>
		<div class="multiple-choice" data-target="checkboxes-example-5-1-panel">
			<input type="checkbox" id="checkboxes-example-5-1" name="contact" value="email" aria-controls="checkboxes-example-5-1-panel" aria-expanded="false">
			<label for="checkboxes-example-5-1" class="form-label">
				Email
			</label>
		</div>
		<div class="panel panel-border-narrow js-hidden" id="checkboxes-example-5-1-panel" aria-hidden="true">
			<label class="form-label" for="contact-email">Email address</label>
			<input class="form-control" name="contact-email" type="text" id="contact-email">
		</div>
		<div class="multiple-choice" data-target="checkboxes-example-5-2-panel">
			<input type="checkbox" id="checkboxes-example-5-2" name="contact" value="phone" aria-controls="checkboxes-example-5-2-panel" aria-expanded="false">
			<label for="checkboxes-example-5-2" class="form-label">
				Phone
			</label>
		</div>
		<div class="panel panel-border-narrow js-hidden" id="checkboxes-example-5-2-panel" aria-hidden="true">
			<label class="form-label" for="contact-phone">Phone number</label>
			<input class="form-control" name="contact-phone" type="text" id="contact-phone">
		</div>
		<div class="multiple-choice" data-target="checkboxes-example-5-3-panel">
			<input type="checkbox" id="checkboxes-example-5-3" name="contact" value="text" aria-controls="checkboxes-example-5-3-panel" aria-expanded="false">
			<label for="checkboxes-example-5-3" class="form-label">
				Text message
			</label>
		</div>
		<div class="panel panel-border-narrow js-hidden" id="checkboxes-example-5-3-panel" aria-hidden="true">
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
|idPrefix|string|No|String to prefix id for each checkbox item if no id is specified on each item. If not passed, fall back to using the name option instead.|
|name|string|Yes|Name attribute for all checkbox items.|
|fieldset|object|No|Options for the fieldset component (e.g. legend). See [fieldset](#fieldset).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|
|items|array|Yes|Array of checkbox items objects. See [items](#items).|
|classes|string|No|Classes to add to the checkboxes container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the checkboxes container.|

### Items
|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Specific id attribute for the checkbox item. If omitted, then `idPrefix` option will be applied.|
|name|string|Yes|Specific name for the checkbox item. If omitted, then component global `name` string will be applied.|
|value|string|Yes|Value for the checkbox input.|
|label|object|No|Provide attributes and classes to each checkbox item label. See [label](#label).|
|hint|object|No|Provide hint to each checkbox item. See [hint](#hint).|
|checked|boolean|No|If true, checkbox will be checked.|
|disabled|boolean|No|If true, checkbox will be disabled.|
|conditional|object|No|Provide content for the conditional reveal. See [conditional](#conditional).|
|attributes|object|No|HTML attributes (for example data attributes) to add to the checkbox input tag.|

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