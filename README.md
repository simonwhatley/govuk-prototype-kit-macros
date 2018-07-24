# About the GOV.UK prototype kit macros
This is a set of [Nunjucks](https://mozilla.github.io/nunjucks/) macros to help in the building UK Government digital service prototypes.

## About the GOV.UK Prototype Kit

The Prototype Kit provides a simple way to make interactive prototypes that look like pages on GOV.UK. These prototypes can be used to show ideas to people you work with, and to do user research.

Read the [project principles](https://govuk-prototype-kit.herokuapp.com/docs/principles).

## About Nunjucks

Nunjucks is a fully featured templating engine for JavaScript.

## Requirements
- [v6.3.0](https://github.com/alphagov/govuk-prototype-kit/tree/v6.3.0) of the prototype kit
- [Nunjucks](https://mozilla.github.io/nunjucks/)

## How to install these macros

Download this project and copy the `components` folder in the `views` folder in the prototype kit, for example:

```
- Prototype root folder
	- app
		- views
			- components
```

Reference the macros in the `layout.html` file, for example:

```
{% from "./components/back-link/macro.njk" import govukBackLink %}
{% from "./components/date-input/macro.njk" import govukDateInput %}
```

Reference the `layout.html` file in your view file, for example:

```
{% extends "./layout.html" %}
```

You're now free to use the macros, for example:

```
{{ govukDateInput({
	"id": "date-of-birth",
	"name": "date_of_birth",
	"fieldset": {
		"legend": {
			"text": "Date of birth"
		}
	},
	"hint": {
		"text": "For example, 31 3 1980"
	},
	"items": [
		{
			"name": "day"
		},
		{
			"name": "month"
		},
		{
			"name": "year"
		}
	]
}) }}
```

## How to use macros

`macro` allows you to define reusable chunks of content. It is similar to a function in a programming language. Here's an example:

```
{% macro field(name, value='', type='text') %}
<div class="field">
  <input type="{{ type }}" name="{{ name }}" value="{{ value | escape }}" />
</div>
{% endmacro %}
```

Now `field` is available to be called like a normal function:

```
{{ field('username') }}
{{ field('password', type='password') }}
```

Which results in the following HTML:

```
<div class="field">
  <input type="text" name="username" value="">
</div>
<div class="field">
  <input type="password" name="password" value="">
</div>
```

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.
