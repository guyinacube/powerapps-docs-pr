<properties
   pageTitle="Customize a gallery template | Microsoft PowerApps"
   description="Format fields, align multiple fields, and change colors to customize a gallery template"
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
   ms.date="05/15/2017"
   ms.author="v-subohe"/>

# Customize a gallery template
Customize the gallery template by formatting fields, aligning multiple fields, or changing a background color.

## Format fields
1. In the **Flooring Sales** example we've been discussing, the sales figure as it's currently formatted may be difficult to recognize as currency. To reformat the sales figure to make it clearer, highlight the field that shows the sales figure in the gallery. In the formula bar, click or tap directly in front of **ThisItem** and enter this **Text** function around **ThisItem.Sales**:

  **Text(ThisItem.Sales,"$#,#00")**

  **ThisItem.Sales** represents the value that exists for each sales item.

  **Note:** If you're familiar with Microsoft Excel, the custom number formats in PowerApps are similar.

2. To make the sales figure appear more clearly as currency, directly in front of **Text**, enter the following in the formula bar:

  **"Total Sales: " & Text(ThisItem.Sales,"$#,#00")**

  Adding the **Total Sales** label will help users view the sales figures as currency.

3. To view the gallery with these changes, open Preview mode by pressing F5 (or by clicking or tapping the play button near the upper-right corner).

## Reduce the size of fields in a template
Change the width (or length) of any field in the gallery template to reduce the amount of space some fields occupy on the screen (such as the **City** and **City code** fields in this example).

**Note:** In PowerApps, use one control as a reference to set the property of another control.

1. In the left-hand pane, go to **Width** in the property list. In the formula bar, notice that **Parent.TemplateWidth** is set to minus 45, which is the default value. One of the ways to change the width is by dividing it by 2 to use only half of the width of the template or by 4 to use only a quarter of the width of the template. For example, select the **City** field and enter **Parent.TemplateWidth/2** in the formula bar, and the field occupies only half of the template width.

2. After reducing the size of the **City** and **City code** fields, move the fields to other parts of the template to make more space for other fields. As fields are moved around on the screen, PowerApps automatically helps to center it.

## Align multiple fields in a template
1. Use the Ctrl key to select multiple fields to align. On the **Home** tab, click or tap **Align** (on the far right-hand side) and then click or tap **Align Top** to ensure both fields are equally aligned at the top.

  **Warning:** Fields may overlap, so be careful to make sure this doesn't occur. For example, if the **City** field is moved next to the **Sales figure** field, and the **Sales figure** field contains a very large number, it may hide the city name. To reduce the size of the field that's overlapping another field, using a corner of a field, drag it to make it smaller; or, to move a field, grab the edge and move it. As the field is moved, PowerApps automatically aligns it.

2. Since we've resized and moved around fields, the template now has too much blank space. Use the edges of the template to reduce the overall size.

## Change the background color and padding of a template
1. To change the background color of the template, in the left-hand pane, go to **TemplateFill** in the property list. In the formula bar, delete the current color and change it to a different color, such as **LightGray**. The background changes to light gray.

2. The padding is the space around the edge of the template. To add a padding to a template, go to **TemplatePadding** in the property list and set the padding size in the formula bar, such as **10** or **20** points.

3. Another way to use **TemplateFill** is to use a different color for a selected item. To highlight the selected item with a different color, type the following in the formula bar:

  **If(ThisITem.IsSelected,LightBlue)**

  When the item is selected, the background color changes to light blue.

4. To add an **Or** statement, type the following in the formula bar:
**If(ThisITem.IsSelected,LightBlue.White)**
When the item is selected, the background color changes to light blue, otherwise, it remains white.
