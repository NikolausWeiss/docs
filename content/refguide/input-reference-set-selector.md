---
title: "Input Reference Set Selector"
parent: "input-widgets"
menu_order: 90
tags: ["studio pro"]
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details.
---

{{% alert type="warning" %}}The input reference set selector widget is not supported on native mobile pages.{{% /alert %}}

The input reference set selector is an [input widget](input-widgets) that can be used to display and edit [associations](associations) for which the multiplicity setting is configured to allow multiple parent objects to associate with multiple children. This type of association is also known as a reference set.

{{% alert type="info" %}}

![](attachments/16713883/16844008.jpg)
The multiplicity settings of an association can be found by double-clicking the association in the [domain model](domain-model).

{{% /alert %}}{{% alert type="info" %}}

![](attachments/pages/input-reference-set-selector.png)
This input reference set selector allows you to link an employee to organizations.

{{% /alert %}}

When clicked, the input reference set selector will open a select page containing a widget with all possible objects that can be used to fill the association.

## General Properties

### Select Page

The select page determines which page is displayed when the input reference selector is clicked. This page can be used to select associated objects from the list of all possible objects. This page should contain a data grid, template grid or list view connected to the same entity as the input reference set selector.

If an input reference set selector is not editable under any circumstances, no select page is required.

See [Opening Pages](opening-pages). Note that opening select pages in content is prohibited.

{{% alert type="info" %}}

You can generate a new page to show by right-clicking the widget and selecting 'Generate select page...'.

{{% /alert %}}

## Selectable Objects Properties

### XPath Constraint

With the XPath constraint you can add a manual constraint to limit the list of objects that can be selected.

{{% alert type="info" %}}

The XPath constraint `[InStock = true()]` on a reference selector for products will ensure that only products that are in stock are selectable.

{{% /alert %}}

### Constrained By

An input reference set selector can be constrained by one or more paths. This is typically used to make one reference selector dependent on another. For example, in page where you can edit a user, an organization selector can be constrained by a country selector. After selecting a country, the organization selector is constrained by this country and shows only organizations linked to that country.

{{% alert type="info" %}}

![](attachments/16713883/16844007.jpg)

In the domain model the user has a reference association to country and a reference set association to organization. The third association, from country to organization, describes the relation between those two entities. Such a 'triangle' shaped part of the domain model is what makes constraining possible.

![](attachments/16713883/16844006.jpg)

The page has displays a reference selector for the reference to country and an input reference set selector for the reference set to organization. The latter is constrained by the path through the domain model that forms the triangle.

![](attachments/16713883/16844005.jpg)

{{% /alert %}}

## Data Source Properties

{{% snippet file="refguide/attribute-path-property.md" %}}

{{% snippet file="refguide/label-property.md" %}}

## Editability Properties

{{% snippet file="refguide/editable-property.md" %}}

{{% snippet file="refguide/read-only-style.md" %}}

{{% snippet file="refguide/condition-property.md" %}}

## Visibility Properties

{{% snippet file="refguide/visibility-property.md" %}}

{{% snippet file="refguide/visibility-property-with-module-roles-simple.md" %}}

## Events Properties

{{% snippet file="refguide/on-change-event.md" %}}

## Common Properties

{{% snippet file="refguide/name-property.md" %}}

{{% snippet file="refguide/class-property.md" %}}

{{% snippet file="refguide/style-property.md" %}}

{{% snippet file="refguide/tab-index-property.md" %}}

## Read More

*   [Data view](data-view)
