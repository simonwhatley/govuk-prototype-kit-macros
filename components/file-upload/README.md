# File upload

## Introduction



## Guidance

Find out when to use the file upload component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app]().

#### Macro

#### Markup

## Arguments

This component accepts the following arguments.

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|Yes|This is used to compose the `id` attribute for each item.|
|name|string|Yes|This is used to compose the `name` attribute for each item.|

**Warning: If you’re using Nunjucks macros in production be aware that using <abbr title="HyperText Markup Language">HTML</abbr> arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).**

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.