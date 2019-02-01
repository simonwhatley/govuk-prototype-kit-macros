# File upload

## Introduction

Use the file upload component to allow users to select and upload a file.

## Guidance

Find out when to use the file upload component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/file-upload/#example-1).

#### Macro
```
{{ govukFileUpload({
	"id": "file-upload",
	"name": "file-upload",
	"label": {
		"text": "Upload a file"
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="file-upload" class="form-label">
		Upload a file
	</label>
	<input id="file-upload" class="form-control" name="file-upload" type="file">
</div>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/file-upload/#example-2).

#### Macro
```
{{ govukFileUpload({
	"id": "file-upload",
	"name": "file-upload",
	"label": {
		"text": "Upload a file",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "Hint text goes here"
	}
}) }}
```

#### Markup
```
<div class="form-group">
	<label for="file-upload" class="form-label-bold">
		Upload a file
		<span for="file-upload-hint" class="form-hint">
			Hint text goes here
		</span>
	</label>
	<input id="file-upload" class="form-control" name="file-upload" type="file">
</div>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/file-upload/#example-3).

#### Macro
```
{{ govukFileUpload({
	"id": "file-upload",
	"name": "file-upload",
	"label": {
		"text": "Upload a file",
		"classes": "form-label-bold"
	},
	"hint": {
		"text": "Hint text goes here"
	},
	"errorMessage": {
		"text": "Error message goes here"
	}
}) }}
```

#### Markup
```
<div class="form-group form-group-error">
	<label for="file-upload" class="form-label-bold">
		Upload a file
		<span for="file-upload-hint" class="form-hint">
			Hint text goes here
		</span>
	</label>
	<span id="file-upload-error" class="error-message">
	  Error message goes here
	</span>
	<input id="file-upload" class="form-control form-control-error" name="file-upload" type="file">
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