---
category: Components
type: Views
title: Tag
---

Tag for categorizing or markuping.

## When To Use

- It can be used to tag by dimension or property.

- categorizing

## API

| Property     | Description           | Type     | Default      |
|--------------|-----------------------|----------|--------------|
| bordered       | To set the style of Tag | boolean | true |
| checkable      | Make Tag behave like Checkbox | boolean    | false  |
| checked        | Specifies whether the tag is selected | boolean    | - |
| defaultChecked | Specifies the initial state: whether or not the tag is selected | boolean    | - |
| onChange       | The callback function that is triggered when the state changes | function(checked) | - |
| closable     | Tag can be closed.    | boolean  | false        |
| onClose      | Callback when tag was closed | function(event)| - |
| afterClose   | Callback when closed animation is complete | function(event)| - |
