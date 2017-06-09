<properties
   pageTitle="Create a gallery from the data in a collection | Microsoft PowerApps"
   description="Create a gallery from the data in a collection"
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

In this topic, we'll create a gallery using the data in a collection and then change some of the fields in the gallery template.

If you haven't saved the app created in the previous topic, save it now. In the left-hand pane, click or tap **Save As** (or press Ctrl-S). Make sure you save the app to the cloud, give it an appropriate name, and provide a description.

## Create a gallery from the data in a collection
Before creating a gallery, select a layout and theme for the app.

In the right-hand pane, click or tap a layout that you want to use.

![Add layout](./media/learning-create-gallery/add-layout.png)

On the **Home** tab, click or tap **Theme**. You should select the theme you want to use in your app before you start adding the controls. This is because once your select a theme, PowerApps will automatically color your controls to fit the theme.

**Note:** If you're running PowerApps from a web browser, you may not see the **Theme** icon.

The gallery you see doesn't currently have the right data. To display the data, click or tap the gallery. Notice that in the lower left-hand corner, you'll see the name of the gallery that you've selected.

In the formula bar, there's a long function that is already built for you. You'll need to do the following three tasks in the formula bar:
- Change the sample data source in the function to the data source you want to use (in the example, the data source is **CitySales**).
- Change the column name that you need to search by to the column name from your table.
- Change the column name you want to sort by to another column name from your data source.
<!--perhaps add a screenshot of the function -->
If you want, continue to add functionality to your data by changing the variables in the function.

## Change elements in the gallery template
To customize your gallery, change some of the elements or fields. For example, to change the title of the gallery, click or tap in the title area of the gallery to select it. Then, in the formula bar, type a new title (in the example, the title is changed to **Flooring Sales**).

You may want to hide the "add new" (+) button in the title area of the gallery because you probably won't be adding any new items. To do this, click or tap in the area around the (+) button to select it and then click or tap **Visible** in the property list. Then, in the formula bar, change the variable to **false** to hide the button.
<!--(Audrie shows a few other examples for customizing, mostly along the same lines as the previous 2 examples.) -->
