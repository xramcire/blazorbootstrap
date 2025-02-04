﻿---
title: Blazor Badge Component
description: The Blazor Bootstrap Badge component shows the small count and labels.
image: https://i.imgur.com/ux0sTs9.png

sidebar_label: Badge
sidebar_position: 3
---

# Blazor Badge

The Blazor Bootstrap `Badge` component shows the small count and labels.

<img src="https://i.imgur.com/ux0sTs9.png" alt="Blazor Bootstrap: Badge Component" />

## Parameters

| Name | Type | Default | Required | Description | Added Version |
|:--|:--|:--|:--|:--|:--|
| ChildContent | RenderFragment | | | Specifies the content to be rendered inside the badge. | 1.7.0 |
| Color | `BadgeColor` | `BadgeColor.Secondary` | ✔️ | Gets or sets the badge color. | 1.7.0 |
| IndicatorType | `BadgeIndicatorType` | `BadgeIndicatorType.None` | | Gets or sets the badge indicator. | 1.7.0 |
| Placement | `BadgePlacement` | `BadgePlacement.None` | | Gets or sets the badge placement. | 1.7.0 |
| Position | `Position` | | | Gets or sets the badge position. | 1.7.0 |
| VisuallyHiddenText | string | | | Gets or sets the visually hidden text. | 1.7.0 |

## Examples

### Basic usage

Badges scale to match the size of the immediate parent element by using relative font sizing and em units. 
As of now, badges no longer have focus or hover styles for links.

<img src="https://i.imgur.com/6aAV5Nb.png" alt="Blazor Bootstrap: Badge Component - Basic usage" />

```cshtml {} showLineNumbers
<h1>Example heading <Badge>New</Badge></h1>
<h2>Example heading <Badge>New</Badge></h2>
<h3>Example heading <Badge>New</Badge></h3>
<h4>Example heading <Badge>New</Badge></h4>
<h5>Example heading <Badge>New</Badge></h5>
<h6>Example heading <Badge>New</Badge></h6>
```

[See demo here](https://demos.blazorbootstrap.com/badge#examples)

### Background colors

<img src="https://i.imgur.com/ux0sTs9.png" alt="Blazor Bootstrap: Badge Component - Background colors" />

```cshtml {} showLineNumbers
<Badge Color="BadgeColor.Primary" VisuallyHiddenText="Visually hidden text for Primary">Primary</Badge>
<Badge Color="BadgeColor.Secondary" VisuallyHiddenText="Visually hidden text for Secondary">Secondary</Badge>
<Badge Color="BadgeColor.Success" VisuallyHiddenText="Visually hidden text for Success">Success</Badge>
<Badge Color="BadgeColor.Danger" VisuallyHiddenText="Visually hidden text for Danger">Danger</Badge>
<Badge Color="BadgeColor.Warning" VisuallyHiddenText="Visually hidden text for Warning">Warning</Badge>
<Badge Color="BadgeColor.Info" VisuallyHiddenText="Visually hidden text for Info">Info</Badge>
<Badge Color="BadgeColor.Light" VisuallyHiddenText="Visually hidden text for Light">Light</Badge>
<Badge Color="BadgeColor.Dark" VisuallyHiddenText="Visually hidden text for Dark">Dark</Badge>
```

:::info Conveying meaning to assistive technologies
Using color to add meaning only provides a visual indication, which will not be conveyed to users of assistive technologies – such as screen readers. Ensure that information denoted by the color is either obvious from the content itself (e.g., the visible text) or is included through alternative means, such as additional text hidden with the `VisuallyHiddenText` parameter.
:::

[See demo here](https://demos.blazorbootstrap.com/badge#background-colors)

### Pill badges

Use the `IndicatorType` parameter to make badges more rounded with a larger `border-radius`.

<img src="https://i.imgur.com/sSuSSJX.png" alt="Blazor Bootstrap: Badge Component - Pill badges" />

```cshtml {} showLineNumbers
<Badge Color="BadgeColor.Primary" IndicatorType="BadgeIndicatorType.RoundedPill">Primary</Badge>
<Badge Color="BadgeColor.Secondary" IndicatorType="BadgeIndicatorType.RoundedPill">Secondary</Badge>
<Badge Color="BadgeColor.Success" IndicatorType="BadgeIndicatorType.RoundedPill">Success</Badge>
<Badge Color="BadgeColor.Danger" IndicatorType="BadgeIndicatorType.RoundedPill">Danger</Badge>
<Badge Color="BadgeColor.Warning" IndicatorType="BadgeIndicatorType.RoundedPill">Warning</Badge>
<Badge Color="BadgeColor.Info" IndicatorType="BadgeIndicatorType.RoundedPill">Info</Badge>
<Badge Color="BadgeColor.Light" IndicatorType="BadgeIndicatorType.RoundedPill">Light</Badge>
<Badge Color="BadgeColor.Dark" IndicatorType="BadgeIndicatorType.RoundedPill">Dark</Badge>
```

[See demo here](https://demos.blazorbootstrap.com/badge#pill-badges)

### Buttons

Badges can be used as part of links or buttons to provide a counter.

<img src="https://i.imgur.com/BO9dltp.png" alt="Blazor Bootstrap: Badge Component - Buttons" />

```cshtml {} showLineNumbers
<div class="mb-3">
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary">
        Announcement <Badge Color="BadgeColor.Danger">2</Badge>
    </Button>
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary">
        Notifications <Badge> 4</Badge>
    </Button>
</div>
<div class="mb-3">
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary">
        Announcement <Badge Color="BadgeColor.Danger"><Icon Name="IconName.MegaphoneFill" /> 2</Badge>
    </Button>
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary">
        Notifications <Badge><Icon Name="IconName.BellFill" /> 4</Badge>
    </Button>
</div>
```

[See demo here](https://demos.blazorbootstrap.com/badge#buttons)

### Positioned

Use `Position` and `Placement` parameters to position it in the corner of a link or button.

<img src="https://i.imgur.com/1e7xDAr.png" alt="Blazor Bootstrap: Badge Component - Positioned" />

```cshtml {} showLineNumbers
<div class="mb-3">
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.TopLeft"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.TopCenter"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.TopRight"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>
</div>
<div class="mb-3">
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.MiddleLeft"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.MiddleCenter"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.MiddleRight"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>
</div>
<div class="mb-3">
    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.BottomLeft"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.BottomCenter"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>

    <Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
        Inbox
        <Badge Color="BadgeColor.Danger"
               Position="Position.Absolute"
               Placement="BadgePlacement.BottomRight"
               IndicatorType="BadgeIndicatorType.RoundedPill"
               VisuallyHiddenText="unread messages">99+</Badge>
    </Button>
</div>
```

[See demo here](https://demos.blazorbootstrap.com/badge#positioned)

### Generic indicator

You can also replace the badge with a generic indicator without the count.

<img src="https://i.imgur.com/HVx7at0.png" alt="Blazor Bootstrap: Badge Component - Generic indicator" />

```cshtml {} showLineNumbers
<Button Type="ButtonType.Button" Color="ButtonColor.Primary" Position="Position.Relative">
    Inbox
    <Badge Color="BadgeColor.Danger"
           Position="Position.Absolute"
           Placement="BadgePlacement.TopRight"
           IndicatorType="BadgeIndicatorType.RoundedPill"
           VisuallyHiddenText="unread messages"></Badge>
</Button>
```

[See demo here](https://demos.blazorbootstrap.com/badge#generic-indicator)
