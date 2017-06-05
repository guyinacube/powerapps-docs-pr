<properties
   pageTitle="Customize a gallery template | Microsoft PowerApps"
   description="Customize a gallery template"
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

Customize your gallery template by formatting fields, aligning multiple fields, or changing a background color.

In the **Flooring Sales** example we've been discussing, the sales figure as it's currently formatted may be difficult to recognize as currency. To reformat the sales figure to make it clearer, highlight the field that shows the sales figure in the gallery. In the formula bar, click or tap directly in front of **ThisItem** and enter this **Text** function around **ThisItem.Sales**:
**Text(ThisItem.Sales,"$#,#00")**
**ThisItem.Sales** represents the value that exists for each sales item.

**Note:** If you're familiar with Microsoft Excel, the custom number formats in PowerApps are similar.

To make the sales figure appear more clearly as currency, directly in front of **Text**, enter the following:
**"Total Sales: " & Text(ThisItem.Sales,"$#,#00")**
Adding the **Total Sales** label will help users view the sales figures as currency.

To view the gallery with these changes, open Preview mode by pressing F5 (or by clicking or tapping the play button near the upper-right corner).

**Reduce the size of fields in a template**
You can change the width (or length) of any field in the gallery template. To reduce the amount of space some fields occupy on the screen (such as the **City** and **City code** fields in this example), change the width.

**Note:** In PowerApps, you can use one control as a reference to set the property of another control.

In the left-hand pane, change the property to **Width**. In the formula bar, notice that **Parent.TemplateWidth** is set to minus 45, which is the default value. One of the ways you can change the width by dividing it by 2 to use only half of the width of the template or by 4 to use only a quarter of the width of the template. For example, when you highlight the **City** field and enter **Parent.TemplateWidth/2** in the formula bar, the field occupies only half of the template width.

After reducing the size of the **City** and **City code** fields, you can then move the fields around to other parts of the template to make more room for other fields. As you drag fields around on the screen, PowerApps automatically helps you center it.

**Align multiple fields in a template**
Use the Ctrl key to select multiple fields to align. On the **Home** tab, click or tap **Align** (on the far right-hand side), and then click or tap **Align Top** to ensure both fields are equally aligned at the top.

**Warning:** Fields may overlap, so be careful to make sure this doesn't occur. For example, if you moved the **City** field next to the **Sales figure** field, and the **Sales figure** field contains a very large number, it may hide the city name. To reduce the size of the field that is overlapping another field, use drag and drop from a corner of a field; or, to move a field, grab the edge and move it. As you move a field, PowerApps aligns it for you.

Since you've resized and moved around fields, the template now has too much blank space. Use the edges of the template to reduce the overall size.

**Change the background color and padding of a template**
To change the background color of your template, in the left-hand pane, change the property to **TemplateFill**. In the formula bar, delete the current color and change it to a different color, such as **LightGray**. The background changes to light gray.

The padding is the space around the edge of the template. To add a padding to a template, in the left-hand pane, change the property to **TemplatePadding**. In the formula bar, set the padding size, such as to 10 or 20 points.

Another way to use **TemplateFill** is when you want to use a different color for a selected item. To highlight the selected item with a different color, type the following in the formula bar:
**If(ThisITem.IsSelected,LightBlue)**
When the item is selected, the background color changes to light blue.

If you want to add an **Or** statement, type the following:
**If(ThisITem.IsSelected,LightBlue.White)**
When the item is selected, the background color changes to light blue, otherwise, it remains white.
