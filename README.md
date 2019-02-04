# About the GOV.UK prototype kit macros
This is a set of [Nunjucks](https://mozilla.github.io/nunjucks/) macros to help in the building UK Government digital service prototypes.

## About the GOV.UK Prototype Kit

The Prototype Kit provides a simple way to make interactive prototypes that look like pages on GOV.UK. These prototypes can be used to show ideas to people you work with, and to do user research.

Read the [project principles](https://govuk-prototype-kit.herokuapp.com/docs/principles).

## About Nunjucks and macros

Nunjucks is a fully featured templating engine for JavaScript.

The `macro` feature allows you to define reusable chunks of content. It is similar to a function in a programming language. Here's an example:

Define the macro:

```
{% macro input(params) %}
<input type="{{ params.type | default('text') }}" name="{{ params.name }}" value="{{ params.value | escape }}">
{% endmacro %}
```

Now `input` is available to be called like a normal function:

```
{{ input(type: 'text', name: 'username') }}
```

Which results in the following HTML:

```
<input type="text" name="username" value="">
```

## Requirements
- [v6.3.0](https://github.com/alphagov/govuk-prototype-kit/tree/v6.3.0) of the prototype kit
- [Nunjucks](https://mozilla.github.io/nunjucks/)

## How to install these macros

### Installing the macros

Download this project and copy the `components` folder in the `views` folder in the prototype kit, for example:

```
- Prototype root folder
  - app
    - assets
    - models
    - views
      - components
      - includes
      - index.html
      - layout.html
    - config.js
    - filters.js
    - routes.js
```

Reference the macros in the `layout.html` file, just below the `{% extends "govuk_template.html" %}` block. For example:

```
{% from "./components/back-link/macro.njk" import govukBackLink %}
{% from "./components/breadcrumbs/macro.njk" import govukBreadcrumbs %}
{% from "./components/button/macro.njk" import govukButton %}
{% from "./components/checkboxes/macro.njk" import govukCheckboxes %}
{% from "./components/date-input/macro.njk" import govukDateInput %}
{% from "./components/details/macro.njk" import govukDetails %}
{% from "./components/error-message/macro.njk" import govukErrorMessage %}
{% from "./components/error-summary/macro.njk" import govukErrorSummary %}
{% from "./components/fieldset/macro.njk" import govukFieldset %}
{% from "./components/file-upload/macro.njk" import govukFileUpload %}
{% from "./components/footer/macro.njk" import govukFooter %}
{% from "./components/header/macro.njk" import govukHeader %}
{% from "./components/hint/macro.njk" import govukHint %}
{% from "./components/input/macro.njk" import govukInput %}
{% from "./components/inset-text/macro.njk" import govukInsetText %}
{% from "./components/label/macro.njk" import govukLabel %}
{% from "./components/panel/macro.njk" import govukPanel %}
{% from "./components/phase-banner/macro.njk" import govukPhaseBanner %}
{% from "./components/radios/macro.njk" import govukRadios %}
{% from "./components/select/macro.njk" import govukSelect %}
{% from "./components/skip-link/macro.njk" import govukSkipLink %}
{% from "./components/table/macro.njk" import govukTable %}
{% from "./components/tabs/macro.njk" import govukTabs %}
{% from "./components/tag/macro.njk" import govukTag %}
{% from "./components/textarea/macro.njk" import govukTextarea %}
{% from "./components/warning-text/macro.njk" import govukWarningText %}
```

Reference the `layout.html` file in your view file, for example:

```
{% extends "./layout.html" %}
```

### Installing the associated JavaScript and CSS assets

Merge the `assets` folder in the `assets` folder in the prototype kit, for example:

```
- Prototype root folder
  - app
    - assets
      - images
      - javascripts
      - sass
    - models
    - views
    - config.js
    - filters.js
    - routes.js
```

Reference the JavaScript files in the `includes/scripts.html` file in the prototype, for example:

```
<script src="/public/javascripts/components/tabs.js"></script>
```

Reference the `SASS` in the `application.scss`, for example:

```
@import 'components/tabs';
```

## How to use these macros

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

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.
