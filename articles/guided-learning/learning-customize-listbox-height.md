<properties
   pageTitle="Customize the height of list boxes in a gallery | Microsoft PowerApps"
   description="Make the height of list boxes in a gallery variable using a function"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-subohe"
   manager="anneta"
   editor=""
   tags=""/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="06/05/2017"
   ms.author="v-subohe"/>

In the previous section, we created a flexible height gallery and used the **GroupBy** function to group the data by countries. Then, we added a list box to the gallery and displayed the cities for each country. Because we created a flexible height gallery, the list boxes are set to a predefined height. Some of the list boxes are too large for the data that's shown in them. In this section, we're going make the height settings for the list boxes variable.

## Make the height of list boxes variable
Click or tap inside one of the list boxes to select it, and then click or tap **Height** in the property list. In the formula bar, you'll see that the **Height** property has a locked value of **225**. To make the height variable, count the rows and then multiply the number by some value that will represent the row height. In the formula bar, type **CountRows(Cities) * 55**.

The function counts the rows of cities and then sets a row height of 55.

When you run the app, you'll see that the height is variable and adjusts depending on the number of cities listed with the country in each row.

## Customize a list box using other settings
Other ways to customize a list box to make it adjust to the data within it include reducing the size of the text, removing the border, and dragging and moving list boxes. <!-- I'm not sure if it should be 'fields' or another term here. Ditto for all the references to 'field' in this section.-->

### Reduce text size
On the **Home** tab, click or tap the arrow next to the **Size** icon and then click or tap a smaller value, such as **18**. Alternatively, click or tap **Size** in the property list, and then type a smaller size in the formula bar.

### Remove borders
Remove the border around the list box. On the **Home** tab, click or tap **Border** and then click or tap **Border Style** and select **None**.

### Move a list box to accommodate more fields
Move the city list box by dragging it closer to the *country* field (which is the **United States** in the example). You can do this because the *country* field is shown across one line in the gallery.

Adjust the width of fields to make room for another field. With the *country* field selected in the gallery, click or tap **Width** in the property list, and then type **Gallery2.TemplateWidth/2** in the formula bar.
<!-- add a screenshot of the formula here? -->

**Gallery2** is the name of the gallery you have open, and when you type **TemplateWidth/2**, you are dividing the template width in half. The *country* field is reduced by half.

Copy the *country* field (Ctrl+C) and move the copy to the other side of the gallery template on the same line. The copy of this field will be *sales*. <!-- note that the item selected in the property list automatically changes to Text when the copy is moved)--> Then, create a math function that aggregates the total sales for all four cities in the country that's selected.
With **Text** selected in the property list, type the following in the formula bar:

**Text(Sum(Filter(CitySales,Country=ThisItem.Country),Sales, "$#,###")**

The formula is wrapped in a **Text** function so the sales figure displays as currency with a dollar sign. Three things were accomplished by this formula: the data is filtered, the sales are aggregated, and then the sales are formatted as currency.
<!-- add a screenshot showing the final result here -->
