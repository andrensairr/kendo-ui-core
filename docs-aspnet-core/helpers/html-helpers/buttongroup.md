---
title: ButtonGroup
page_title: ButtonGroup | Telerik UI for ASP.NET Core HtmlHelpers
description: "Learn the basics when working with the ButtonGroup HtmlHelper for ASP.NET Core (MVC 6 or ASP.NET Core MVC)."
slug: htmlhelpers_buttongroup_aspnetcore
---

# ButtonGroup HtmlHelper Overview

The ButtonGroup HtmlHelper extension is a server-side wrapper for the [Kendo UI ButtonGroup](https://demos.telerik.com/kendo-ui/buttongroup/index) widget.

For more information on the HtmlHelper, refer to the article on the [ButtonGroup HtmlHelper for ASP.NET MVC](http://docs.telerik.com/aspnet-mvc/helpers/buttongroup/overview).

## Getting Started

### Initialization

The following example demonstrates how to initialize the ButtonGroup.

###### Example

```
        @(Html.Kendo().ButtonGroup()
            .Name("select-period")
            .Items(t =>
                {
                        t.Add().Text("Month");
                        t.Add().Text("Quarter");
                        t.Add().Text("Year");
                }))
```

## Icons

Kendo UI ButtonGroup provides a method for configuring icons - `.Icon()`.

###### Example

```
         @(Html.Kendo().ButtonGroup()
            .Name("player")
            .Items(t =>
            {
                    t.Add().Icon("play");
                    t.Add().Icon("pause");
                    t.Add().Icon("stop");
            }))
```

The above configuration is expected to produce the HTML output from the following example.

###### Example

        <div class="k-button-group k-widget" data-role="buttongroup" id="player" role="group" tabindex="0">
            <span data-icon="play" aria-pressed="false" role="button" class="k-button k-button-icon">
                <span class="k-icon k-i-play"></span>
            </span>
            <span data-icon="pause" aria-pressed="false" role="button" class="k-button k-button-icon">
                <span class="k-icon k-i-pause"></span>
            </span>
            <span data-icon="stop" aria-pressed="false" role="button" class="k-button k-button-icon">
                <span class="k-icon k-i-stop"></span>
            </span>
        </div>

## Features

### Enable and Disable ButtonGroup

Kendo UI ButtonGroup can be configured to be initially disabled via its `.Enable()` setting. The ButtonGroup can also be disabled or enabled at any time with JavaScript by using its `.Enable()` method with a Boolean argument.

The example below demonstrates how to enable and disable the ButtonGroup.

The following example demonstrates how to use `.Enable()`.

###### Example

```

        @(Html.Kendo().ButtonGroup()
            .Name("select-period")
            .Enable(false)
            .Items(t =>
                {
                        t.Add().Text("Month");
                        t.Add().Text("Quarter");
                        t.Add().Text("Year");
                }))
```

For more information on the [`enable` method of the ButtonGroup](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup#methods-enable), refer to the [API of the ButtonGroup control](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup).

### Index

Initially selected index of the Kendo UI ButtonGroup can be configured via its `index` property. An index could be selected via `select()` method with a Integer argument.

The example below demonstrates how to select a button by its index.

###### Example

```

        @(Html.Kendo().ButtonGroup()
            .Name("select-period")
            .Index(1)
            .Items(t =>
                {
                        t.Add().Text("Month");
                        t.Add().Text("Quarter");
                        t.Add().Text("Year");
                }))
```

For more information on the [`index` setting of the ButtonGroup](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup#configuration-index), refer to the [API of the ButtonGroup control](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup).


### Selection

Kendo UI ButtonGroup can restrict the numbers of Buttons that can be selected via its `.Selection()` property. It can be configured with `single` or `multiple` selection.

The following example demonstrates how to use `.Selection()`.

###### Example

```

        @(Html.Kendo().ButtonGroup()
            .Name("select-period")
            .Selection("multiple")
            .Items(t =>
                {
                        t.Add().Text("Month");
                        t.Add().Text("Quarter");
                        t.Add().Text("Year");
                }))
```

For more information on the [`selection` setting of the ButtonGroup](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup#configuration-selection), refer to the [API of the ButtonGroup control](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup).

## Reference

### Existing Instances

For more information on how to access an instance, refer to the [introductory article on the ButtonGroup](http://docs.telerik.com/kendo-ui/controls/navigation/buttongroup/overview).

## See Also

* [JavaScript API Reference of the ButtonGroup](http://docs.telerik.com/kendo-ui/api/javascript/ui/buttongroup)
* [ButtonGroup HtmlHelper for ASP.NET MVC](http://docs.telerik.com/aspnet-mvc/helpers/buttongroup/overview)
* [ButtonGroup Official Demos](http://demos.telerik.com/aspnet-core/buttongroup/index)
* [Overview of Telerik UI for ASP.NET Core]({% slug overview_aspnetmvc6_aspnetmvc %})
* [Get Started with Telerik UI for ASP.NET Core in ASP.NET Core Projects]({% slug gettingstarted_aspnetmvc6_aspnetmvc %})
* [Get Started with Telerik UI for ASP.NET Core in ASP.NET Core Projects on Linux]({% slug gettingstartedlinux_aspnetmvc6_aspnetmvc %})
* [Known Issues with Telerik UI for ASP.NET Core]({% slug knownissues_aspnetmvc6_aspnetmvc %})
