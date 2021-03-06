---
title: Rating Menu
mainTitle: Components
layout: main.pug
category: Components
withHeadings: true
navWeight: 6
editable: true
githubSource: docs/src/components/RatingMenu.md
---

A rating menu is a numeric list of a rating. By default visualized with stars. Note that the attribute needs to have integers

<a class="btn btn-static-theme" href="stories/?selectedKind=ais-rating-menu">🕹 try out live</a>

## Usage

```html
<ais-rating-menu :attribute="value"></ais-rating-menu>
```

## Props

Name | Type | Default | Description | Required
---|---|---|---|---
attribute | string |  | The attribute to use for the rating | yes
max | number | `5` | maximum rating to show | no
class-names | Object | `{}` | Override class names | no

## Slots

Name | Scope | Description
---|---|---
default | `{ items: Array<Item>, refine: String => void, createURL: Item => String }` | Slot to override the DOM output
andUp | `{ }` | Slot to override the "& up" text after the star icons.

an `Item` has the following keys:

- `stars`: An array of booleans, e.g. `[true, true, true, false]` to show which stars should be colored
- `name`: string version of the "number of stars" to put
- `value`: string version of the "number of stars" to put
- `count`: number of hits with this refinement enabled
- `isRefined`: boolean which will be true if this Item is selected

## CSS classes

Here's a list of CSS classes exposed by this widget. To better understand the underlying
DOM structure, have a look at the generated DOM in your browser.

Note that you can pass the prop `class-names`, with an object of class names and their replacement to override this.

Class name | Description
---|---
`ais-RatingMenu` | Container class
`#ais-RatingMenu-starSymbol` | The svg symbol for a filled star
`#ais-RatingMenu-starEmptySymbol` | The svg symbol for an empty star
`ais-RatingMenu-list` | The list of ratings
`ais-RatingMenu-item` | each rating item
`ais-RatingMenu-link` | the link of each rating
`ais-RatingMenu-starIcon` | the star icon
`ais-RatingMenu-starIcon--full` | the star icon when it's filled
`ais-RatingMenu-starIcon--empty` | the star icon when it's not filled
`ais-RatingMenu-label` | the "and more" label
`ais-RatingMenu-count` | the number of results for this rating
