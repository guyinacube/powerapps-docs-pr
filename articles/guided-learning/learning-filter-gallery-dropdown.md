<properties
   pageTitle="Filter a gallery using a drop-down control | Microsoft PowerApps"
   description="Quickly filter data in a gallery using a drop down control"
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
   ms.date="08/05/2017"
   ms.author="v-subohe"/>

# Using a drop-down control to filter data in a gallery
When you generate an app from a data source, the gallery that is created includes a search box. Another way to search for data in a gallery is to filter the results using a drop-down control. We'll look at filtering in this topic.

**Note:** If you're creating an app for mobile devices, drop-down controls are not always the best choice because they require precision. For mobile devices, consider using radio buttons or a larger control.

## Create a drop down control
1. On the **Insert** tab, click or tap **Controls** and then click or tap **Drop down**. When the drop-down control appears in the gallery, drag and resize it so it fits below the title bar and above the gallery template.

    ![Insert drop-down control](./media/learning-filter-gallery-dropdown/insert-control-dropdown.png)

1. In the left-hand pane, search for **Dropdown1**, click or tap the **...** menu, select **Rename**, and type a name for the drop-down control so that it's easy to find later. For this example, the drop-down control is named **ddCountry**, because you'll filter on the **Country** field. 

    ![Rename drop-down control](./media/learning-filter-gallery-dropdown/rename-control.png)

## Select data to filter
1. Select **Items** in the property list for the drop-down control, and, in the formula bar, change the value to **CitySales**. If you click the drop-down arrow, you'll see that only the **City** values are listed. Because a column wasn't specified in **Items**, PowerApps returned the first column by default. 

1. Change the formula to **CitySales.Country**, and now the drop-down displays all the **Country** values. However, notice that there are duplicates, because there are several cities that have the same country. You can remove the duplicates by using the **Distinct** function:

    **Distinct(CitySales, Country)**

    If the **Distinct** function detects multiple instances of a value, it will only display one of them. 

    ![Distinct function](./media/learning-filter-gallery-dropdown/distinct.png)

## Select data to display in the gallery

To connect the drop-down control to the gallery, configure the **Items** property for the gallery to use the **Filter** function instead of the **SortByColumn** function. 

Click or tap the gallery to select it, and then select **Items** in the property list. In the formula bar, delete all of the existing text and type the following:

**Filter(CitySales,ddCountry.Selected.Value in Country)**

The gallery is now set to filter the **CitySales** data by the country that is selected in the drop-down.

![Distinct function](./media/learning-filter-gallery-dropdown/filtered-gallery.png)