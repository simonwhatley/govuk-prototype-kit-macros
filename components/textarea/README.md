# Text area

## Introduction

Use the textarea component when you need to let users enter an amount of text that’s longer than a single line.

## Guidance

Find out when to use the textarea component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/textarea/#example-1).

#### Macro
```
{{ govukTextarea({
	"id": "additional-information",
	"name": "additional-information",
	"label": {
		"text": "Please provide more information",
		"classes": "form-label-bold"
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="additional-information-1" class="form-label-bold">
		Please provide more information
	</label>
	<textarea id="additional-information-1" class="form-control" name="additional-information-1" rows="5"></textarea>
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/textarea/#example-2).

#### Macro
```
{{ govukTextarea({
	"id": "additional-information",
	"name": "additional-information",
	"label": {
		"text": "Please provide more information",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "Don't include personal or financial information, for example your National Insurance number or credit card details."
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="additional-information-2" class="form-label-bold">
		Please provide more information
		<span for="additional-information-2-hint" class="form-hint">
			Don't include personal or financial information, for example your National Insurance number or credit card details.
		</span>
	</label>
	<textarea id="additional-information-2" class="form-control" name="additional-information-2" rows="5"></textarea>
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/textarea/#example-3).

#### Macro
```
{{ govukTextarea({
	"id": "additional-information",
	"name": "additional-information",
	"label": {
		"text": "Please provide more information",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "Don't include personal or financial information, for example your National Insurance number or credit card details."
	},
	"errorMessage": {
		"text": "Error message goes here"
	}
}) }}
```

#### Markup
```
<div class="form-group form-group-error">
	<label for="additional-information-3" class="form-label-bold">
		Please provide more information
		<span for="additional-information-3-hint" class="form-hint">
			Don't include personal or financial information, for example your National Insurance number or credit card details.
		</span>
	</label>
	<span id="additional-information-3-error" class="error-message">
	  Error message goes here
	</span>
	<textarea id="additional-information-3" class="form-control form-control-error" name="additional-information-3" rows="5"></textarea>
</div>
```

### Example 4

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/textarea/#example-4).

#### Macro
```
{{ govukTextarea({
	"id": "additional-information-1",
	"name": "additional-information-1",
	"label": {
		"text": "Please provide more information",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "Don't include personal or financial information, for example your National Insurance number or credit card details."
	},
	"value": "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur a amet iste repellat. Labore explicabo assumenda, architecto non expedita sit, fuga nulla suscipit. Tenetur neque dicta, ea ad aliquam eligendi?"
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="additional-information-4" class="form-label-bold">
		Please provide more information
		<span for="additional-information-4-hint" class="form-hint">
			Don't include personal or financial information, for example your National Insurance number or credit card details.
		</span>
	</label>
	<textarea id="additional-information-4" class="form-control" name="additional-information-4" rows="5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur a amet iste repellat. Labore explicabo assumenda, architecto non expedita sit, fuga nulla suscipit. Tenetur neque dicta, ea ad aliquam eligendi?</textarea>
</div>
```

### Example 5

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/textarea/#example-5).

#### Macro
```
{{ govukTextarea({
	"id": "additional-information",
	"name": "additional-information",
	"label": {
		"text": "Please provide more information",
		"classes": "heading-xlarge",
		"isPageHeading": true
	},
	"hint": {
		"text": "Don't include personal or financial information, for example your National Insurance number or credit card details."
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<h1>
		<label for="additional-information-5" class="heading-xlarge">
			Please provide more information
			<span for="additional-information-5-hint" class="form-hint">
				Don't include personal or financial information, for example your National Insurance number or credit card details.
			</span>
		</label>
	</h1>
	<textarea id="additional-information-5" class="form-control" name="additional-information-5" rows="5"></textarea>
</div>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|Optional `id` attribute to add to the textarea.|
|name|string|Yes|Name attribute for the textarea.|
|rows|integer|No|Optional number of textarea rows. Default is 5 rows.|
|value|string|No|Optional value of the textarea.|
|label|object|No|Options for the label component (e.g. text). See [label](#label).|
|hint|object|No|Options for the hint component (e.g. text). See [hint](#hint).|
|errorMessage|object|No|Options for the errorMessage component (e.g. text). See [errorMessage](#errormessage).|
|classes|string|No|Classes to add to the textarea.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the textarea.|

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