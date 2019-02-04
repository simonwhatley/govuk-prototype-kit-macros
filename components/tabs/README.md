# Tabs

## Introduction

Use the tabs component to let users navigate between related sections of content, displaying one section at a time.

The tabs component requires the [tabs.js](#) and [tabs.scss](#).

## Guidance

Find out when to use the tabs component in your service in the [GOV.UK Elements documentation](http://govuk-elements.herokuapp.com/).

## Examples

### Example 1

Preview this example in the [prototype demo app](https://govuk-prototype-kit-macros.herokuapp.com/examples/tabs/#example-1).

#### Macro
```
{{ govukTabs({
  "items": [
    {
      "label": "Past day",
      "id": "past-day",
      "panel": {
        "html": "<h2 class="heading-large">Past day</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>3</td><td>0</td></tr><tr><td>Paul Farmer</td><td>1</td><td>0</td></tr><tr><td>Rita Patel</td><td>2</td><td>0</td></tr></tbody></table>"
      }
    },
    {
      "label": "Past week",
      "id": "past-week",
      "panel": {
        "html": "<h2 class="heading-large">Past week</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>24</td><td>18</td></tr><tr><td>Paul Farmer</td><td>16</td><td>20</td></tr><tr><td>Rita Patel</td><td>24</td><td>27</td></tr></tbody></table>"
      }
    },
    {
      "label": "Past month",
      "id": "past-month",
      "panel": {
        "html": "<h2 class="heading-large">Past month</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>98</td><td>95</td></tr><tr><td>Paul Farmer</td><td>122</td><td>131</td></tr><tr><td>Rita Patel</td><td>126</td><td>142</td></tr></tbody></table>"
      }
    },
    {
      "label": "Past year",
      "id": "past-year",
      "panel": {
        "html": "<h2 class="heading-large">Past year</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>1380</td><td>1472</td></tr><tr><td>Paul Farmer</td><td>1129</td><td>1083</td></tr><tr><td>Rita Patel</td><td>1539</td><td>1265</td></tr></tbody></table>"
      }
    }
  ]
}) }}
```

#### Markup
```
<div class="tabs" data-module="tabs">
  <h2 class="heading-medium">
    Contents
  </h2>
  <div class="tabs-nav">
    <ul class="tabs-list" role="tablist">
      <li role="presentation">
        <a href="#past-day" aria-selected="true" role="tab" tabindex="0" aria-controls="past-day">
          Past day
        </a>
      </li>
      <li role="presentation">
        <a href="#past-week" aria-selected="false" role="tab" tabindex="-1" aria-controls="past-week">
          Past week
        </a>
      </li>
      <li role="presentation">
        <a href="#past-month" aria-selected="false" role="tab" tabindex="-1" aria-controls="past-month">
          Past month
        </a>
      </li>
      <li role="presentation">
        <a href="#past-year" aria-selected="false" role="tab" tabindex="-1" aria-controls="past-year">
          Past year
        </a>
      </li>
    </ul>
  </div>
  <div class="tabs-content">
    <div class="tabs-panel" id="past-day" role="tabpanel">
      <div class="tabs-panel-inner" tabindex="0">
        <h2 class="heading-large">Past day</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>3</td><td>0</td></tr><tr><td>Paul Farmer</td><td>1</td><td>0</td></tr><tr><td>Rita Patel</td><td>2</td><td>0</td></tr></tbody></table>
      </div>
    </div>
    <div class="tabs-panel" id="past-week" role="tabpanel" aria-hidden="true">
      <div class="tabs-panel-inner" tabindex="0">
        <h2 class="heading-large">Past week</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>24</td><td>18</td></tr><tr><td>Paul Farmer</td><td>16</td><td>20</td></tr><tr><td>Rita Patel</td><td>24</td><td>27</td></tr></tbody></table>
      </div>
    </div>
    <div class="tabs-panel" id="past-month" role="tabpanel" aria-hidden="true">
      <div class="tabs-panel-inner" tabindex="0">
        <h2 class="heading-large">Past month</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>98</td><td>95</td></tr><tr><td>Paul Farmer</td><td>122</td><td>131</td></tr><tr><td>Rita Patel</td><td>126</td><td>142</td></tr></tbody></table>
      </div>
    </div>
    <div class="tabs-panel" id="past-year" role="tabpanel" aria-hidden="true">
      <div class="tabs-panel-inner" tabindex="0">
        <h2 class="heading-large">Past year</h2><table><thead><tr><th scope="col">Case manager</th><th scope="col">Cases opened</th><th scope="col">Cases closed</th></tr></thead><tbody><tr><td>David Francis</td><td>1380</td><td>1472</td></tr><tr><td>Paul Farmer</td><td>1129</td><td>1083</td></tr><tr><td>Rita Patel</td><td>1539</td><td>1265</td></tr></tbody></table>
      </div>
    </div>
  </div>
</div>
```

## Arguments

This component accepts the following arguments.

### Container

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|No|Specific id attribute for the component and to compose the id attribute for each tab.|
|idPrefix|string|No|String to prefix id for each tab item if no id is specified on each item.|
|items|array|Yes|Array of tab items objects. See [items](#items).|
|classes|string|No|Classes to add to the table head cell.|
|attributes|object|No|HTML attributes (for example data attributes) to add to the table head cell.|

### Items

|Name|Type|Required|Description|
|---|---|---|---|
|id|string|yes|The id attribute for the tab item. If omitted, then `idPrefix` string will be applied.|
|label|string|yes|The text label of the tab item.|
|panel|object|yes|The content for each tab item. See [panel](#panel).|

### Panel
|Name|Type|Required|Description|
|---|---|---|---|
|text|string|Yes|If `html` is set, this is not required. Text to use within the tab panel. If `html` is provided, the `text` argument will be ignored.|
|html|string|Yes|If `text` is set, this is not required. HTML to use within the tab panel. If `html` is provided, the `text` argument will be ignored.|

*Warning: If you’re using Nunjucks macros in production be aware that using HTML arguments, or ones ending with `.html` can be at risk from [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) attacks. More information about security vulnerabilities can be found in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).*

## Licence

Unless otherwise stated, this codebase is released under the [MIT License](https://github.com/whatterz/govuk-prototype-kit-macros/blob/master/LICENSE). This covers both the codebase and any sample code in the documentation.