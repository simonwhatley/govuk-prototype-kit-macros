# Error summary

## Introduction

Use the error summary component at the top of a page to summarise any errors a user has made.

When a user makes an error, you must show both an error summary and an [error message](https://govuk-prototype-kit-macros.herokuapp.com/examples/error-message/) next to each answer that contains an error.

## Guidance

Find out when to use the error summary component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/error-summary/#example-1).

#### Macro
```
{{ govukErrorSummary({
	"titleText": "Message to alert the user to a problem goes here",
	"descriptionText": "Optional description of the errors and how to correct them",
	"errorList": [
		{
			"text": "Descriptive link to the question with an error",
			"href": "#question-1"
		},
		{
			"text": "Descriptive link to the question with an error",
			"href": "#question-2"
		}
	]
}) }}
```

#### Markup
```
<div class="error-summary" aria-labelledby="error-summary-title" role="alert" tabindex="-1" data-module="error-summary">
	<h2 class="heading-medium error-summary-heading" id="error-summary-title">
		Message to alert the user to a problem goes here
	</h2>
	<p>
		Optional description of the errors and how to correct them
	</p>
	<ul class="error-summary-list">
		<li>
			<a href="#question-1">Descriptive link to the question with an error</a>
		</li>
		<li>
			<a href="#question-2">Descriptive link to the question with an error</a>
		</li>
	</ul>
</div>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|titleText|string|Yes|If `titleHtml` is set, this is not required. Text to use for the heading of the error summary block. If `titleHtml` is provided, `titleText` will be ignored.|
|titleHtml|string|Yes|If `titleText` is set, this is not required. HTML to use for the heading of the error summary block. If `titleHtml` is provided, `titleText` will be ignored.|
|descriptionText|string|Yes|If `descriptionHtml` is set, this is not required. Text to use for the description of the errors. If `descriptionHtml` is provided, `descriptionText` will be ignored.|
|descriptionHtml|string|Yes|If `descriptionText` is set, this is not required. HTML to use for the description of the errors. If `descriptionHtml` is provided, `descriptionText` will be ignored.|
|errorList|array|Yes|Contains an array of error link items and all their available arguments. See [items](#items).|
|classes|string|No|Classes to add to the error summary container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the error summary container.|

### Items

|Name|Type|Required|Description|
|---|---|---|---|
|href|string|No|Optional `href` attribute for the error link item. If provided the item will be an anchor.|
|text|string|Yes|If `html` is set, this is not required. Text to use within the error link item. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the error link item. If `html` is provided, the `text` argument will be ignored.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the error link anchor.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.