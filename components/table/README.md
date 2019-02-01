# Tables

## Introduction

Use the table component to make it easier for users to scan and compare information.

## Guidance

Find out when to use the table component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/table/#example-1).

#### Macro
```
{{ govukTable({
	"rows": [
		[
			{
				"text": "January"
			},
			{
				"text": "£85",
				"format": "numeric"
			},
			{
				"text": "£95",
				"format": "numeric"
			}
		],
		[
			{
				"text": "February"
			},
			{
				"text": "£75",
				"format": "numeric"
			},
			{
				"text": "£55",
				"format": "numeric"
			}
			],
			[
			{
				"text": "March"
			},
			{
				"text": "£165",
				"format": "numeric"
			},
			{
				"text": "£125",
				"format": "numeric"
			}
		]
	]
}) }}
```

#### Markup
```
<table>
	<tbody>
		<tr>
			<td>January</td>
			<td class="numeric">£85</td>
			<td class="numeric">£95</td>
		</tr>
		<tr>
			<td>February</td>
			<td class="numeric">£75</td>
			<td class="numeric">£55</td>
		</tr>
		<tr>
			<td>March</td>
			<td class="numeric">£165</td>
			<td class="numeric">£125</td>
		</tr>
	</tbody>
</table>
```

### Example 2

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/table/#example-2).

#### Macro
```
{{ govukTable({
	"head": [
		{
			"text": "Month you apply"
		},
		{
			"text": "Rate for bicycles",
			"format": "numeric"
		},
		{
			"text": "Rate for vehicles",
			"format": "numeric"
		}
	],
	"rows": [
		[
			{
				"text": "January"
			},
			{
				"text": "£85",
				"format": "numeric"
			},
			{
				"text": "£95",
				"format": "numeric"
			}
		],
		[
			{
				"text": "February"
			},
			{
				"text": "£75",
				"format": "numeric"
			},
			{
				"text": "£55",
				"format": "numeric"
			}
			],
			[
			{
				"text": "March"
			},
			{
				"text": "£165",
				"format": "numeric"
			},
			{
				"text": "£125",
				"format": "numeric"
			}
		]
	]
}) }}
```

#### Markup
```
<table>
	<thead>
		<tr>
			<th scope="col">Month you apply</th>
			<th class="numeric" scope="col">Rate for bicycles</th>
			<th class="numeric" scope="col">Rate for vehicles</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>January</td>
			<td class="numeric">£85</td>
			<td class="numeric">£95</td>
		</tr>
		<tr>
			<td>February</td>
			<td class="numeric">£75</td>
			<td class="numeric">£55</td>
		</tr>
		<tr>
			<td>March</td>
			<td class="numeric">£165</td>
			<td class="numeric">£125</td>
		</tr>
	</tbody>
</table>
```

### Example 3

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/table/#example-3).

#### Macro
```
{{ govukTable({
	"caption": "Caption 1: Months and rates",
	"captionClasses": "heading-large",
	"firstCellIsHeader": true,
	"head": [
		{
			"text": "Month you apply"
		},
		{
			"text": "Rate for bicycles",
			"format": "numeric"
		},
		{
			"text": "Rate for vehicles",
			"format": "numeric"
		}
	],
	"rows": [
		[
			{
				"text": "January"
			},
			{
				"text": "£85",
				"format": "numeric"
			},
			{
				"text": "£95",
				"format": "numeric"
			}
		],
		[
			{
				"text": "February"
			},
			{
				"text": "£75",
				"format": "numeric"
			},
			{
				"text": "£55",
				"format": "numeric"
			}
			],
			[
			{
				"text": "March"
			},
			{
				"text": "£165",
				"format": "numeric"
			},
			{
				"text": "£125",
				"format": "numeric"
			}
		]
	]
}) }}
```

#### Markup
```
<table>
	<caption class="heading-large">Caption 1: Months and rates</caption>
	<thead>
		<tr>
			<th scope="col">Month you apply</th>
			<th class="numeric" scope="col">Rate for bicycles</th>
			<th class="numeric" scope="col">Rate for vehicles</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th scope="row">January</th>
			<td class="numeric">£85</td>
			<td class="numeric">£95</td>
		</tr>
		<tr>
			<th scope="row">February</th>
			<td class="numeric">£75</td>
			<td class="numeric">£55</td>
		</tr>
		<tr>
			<th scope="row">March</th>
			<td class="numeric">£165</td>
			<td class="numeric">£125</td>
		</tr>
	</tbody>
</table>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|head|array|No|Array of table head cells. See [head](#head).|
|rows|array|Yes|Array of table rows and cells. See [rows](#rows).|
|caption|string|No|Caption text.|
|captionClasses|string|No|Classes for caption text. Classes should correspond to the available typography heading classes: `heading-xlarge`, `heading-large`, `heading-medium` and `heading-small`.|
|firstCellIsHeader|boolean|No|If set to true, the first cell in table row will be a `th` instead of a `td`.|
|classes|string|No|Classes to add to the table container.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the table container.|

### Head

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the table head cell. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the table head cell. If `html` is provided, the `text` argument will be ignored.|
|format|string|No|The format of a cell. The only supported option is `numeric`.|
|colspan|integer|No|The number of columns a cell extends.|
|rowspan|integer|No|The number of rows a cell extends.|
|classes|string|No|Classes to add to the table head cell.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the table head cell.|

### Rows

|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the table cell. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the table cell. If `html` is provided, the `text` argument will be ignored.|
|format|string|No|The format of a cell. The only supported option is `numeric`.|
|colspan|integer|No|The number of columns a cell extends.|
|rowspan|integer|No|The number of rows a cell extends.|
|classes|string|No|Classes to add to the table cell.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the table cell.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.