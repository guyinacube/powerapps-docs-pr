<properties
   pageTitle="Sort data in a gallery using the GroupBy function | Microsoft PowerApps"
   description="Group together specific data in a gallery based on certain values"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="skjerland"
   manager="anneta"
   editor=""
   tags=""/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="10/10/2017"
   ms.author="sharik"/>

# Sorting data in a gallery using the GroupBy function
When working with galleries, you'll often find that you have a large amount of data that you need to group together based on certain values. Using our **CitySales** example, let's group the sales data by country using the  **GroupBy** function, so that each country is displayed in a single item with all of the data for that country displayed next to it.

## Create a gallery with flexible height
On the **Insert** tab, click or tap **New screen**, and then select **Blank screen** to create a new screen. On the **Insert** tab, click or tap **Gallery**, select **Blank flexible height**, and then expand the gallery to the bottom of the screen. This gives you room to add items to the gallery.

   ![Insert flexible height gallery](./media/learning-display-records-groupby/gallery-flex-height.png)

To connect the gallery to the **CitySales** collection, in the property list, select **Items**, and then in the formula bar, replace **CustomGallerySample** with **CitySales**.

In the upper left-hand corner of the gallery, click or tap the pencil icon to select the gallery template. Go back to the **Insert** tab, click or tap **Label**, and then in the formula bar, replace the default value with **ThisItem.Country**.

## Group specific data together in the gallery

Note that the country for each item is displayed in the gallery, and because there are multiple cities for each country, each country is displayed multiple times.

To group all of the items for a country together, select the gallery (not the gallery template), and replace **CitySales** in the **Items** property with the  **GroupBy** function, as shown in the formula bar below. This formula also creates a group named **Cities** that holds the rest of the data for each country group.

![Country groups](./media/learning-display-records-groupby/groupedby.png)

Next, select the template, and on the **Insert** tab, click or tap **Controls**, and then click or tap **List box**. Resize or move the list box control so that it fits in the template next to the **Country** field.

![Format list box](./media/learning-display-records-groupby/format-list-box.png)

To display the data in the list box, set the **Items** property of the list box control to **Cities**. When you preview the app, the gallery displays each country as a separate item with the associated cities grouped next to it.

![Insert list box](./media/learning-display-records-groupby/final-display.png)

You may have noticed that the list boxes are set to a predefined height, and some of them are larger than they need to be for the data they contain. In the next topic, you'll learn how to customize list boxes by making the height setting variable.
