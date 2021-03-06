---
title: Window
page_title: Window | Telerik UI for ASP.NET Core Tag Helpers
description: "Learn the basics when working with the Window tag helper for ASP.NET Core (MVC 6 or ASP.NET Core MVC)."
previous_url: /aspnet-core/helpers/window
slug: taghelpers_window_aspnetcore
---

# Window Tag Helper Overview

The Window tag helper helps you configure the Kendo UI Window widget in ASP.NET Core applications.

## Basic Usage

The following example demonstrates how to define the Window by using the Window tag helper.

> **Important**
>
> A change in the Window's tag names has been introduced in R1 2018, in order to ensure tag naming consistency across the Telerik UI for ASP.NET Core suite. Previously it was possible to nest content directly within the `<kendo-window>` tag, since R1 2018 content must be nested within a `<content>` tag.

###### Example

        <kendo-window name="window1">
			<content>Window contents</content>
		</kendo-window>

## Configuration

The Window tag helper configuration options are passed as attributes of the tag. The Window contents is placed between the opening and closing tag.

###### Example

```tab-cshtml

        @(Html.Kendo().Window()
            .Name("window")
            .Title("About Alvar Aalto")
            .Content(@<text>
                <div class="armchair">
                    <img src="@Url.Content("~/shared/web/window/armchair-402.png")"
                            alt="Artek Alvar Aalto - Armchair 402" />
                    Artek Alvar Aalto - Armchair 402
                </div>

                <p>
                    Alvar Aalto is one of the greatest names in modern architecture and design.
                    Glassblowers at the iittala factory still meticulously handcraft the legendary
                    vases that are variations on one theme, fluid organic shapes that let the end user
                    ecide the use. Interpretations of the shape in new colors and materials add to the
                    growing Alvar Aalto Collection that remains true to his original design.
                </p>
            </text>)
            .Draggable()
            .Width(600)
            .Events(ev => ev.Close("onClose"))
        )
```
```tab-tagHelper

        <kendo-window name="window" title="About Alvar Aalto" draggable="true"
            width="400" on-close="onClose">
			<content>
				<div class="armchair">
					<img src="@Url.Content("~/shared/web/window/armchair-402.png")"
						alt="Artek Alvar Aalto - Armchair 402" />
					Artek Alvar Aalto - Armchair 402
				</div>

				<p>
					Alvar Aalto is one of the greatest names in modern architecture and design.
					Glassblowers at the iittala factory still meticulously handcraft the legendary
					vases that are variations on one theme, fluid organic shapes that let the end user
					ecide the use. Interpretations of the shape in new colors and materials add to the
					growing Alvar Aalto Collection that remains true to his original design.
				</p>
			</content>
        </kendo-window>
```

## See Also

* [Overview of Telerik UI for ASP.NET Core]({% slug overview_aspnetmvc6_aspnetmvc %})
* [Get Started with Telerik UI for ASP.NET Core in ASP.NET Core Projects]({% slug gettingstarted_aspnetmvc6_aspnetmvc %})
* [Get Started with Telerik UI for ASP.NET Core in ASP.NET Core Projects on Linux]({% slug gettingstartedlinux_aspnetmvc6_aspnetmvc %})
* [Known Issues with Telerik UI for ASP.NET Core]({% slug knownissues_aspnetmvc6_aspnetmvc %})
