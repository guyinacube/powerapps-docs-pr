<properties
   pageTitle="Filter a gallery using a drop-down control | Microsoft PowerApps"
   description="Quickly search for data in a gallery using a filter drop down control"
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
   ms.date="05/30/2017"
   ms.author="v-subohe"/>

Another way to search for data in a gallery is to use a filter drop down control. If you're using a drop down filter in a phone application, however, drop down controls are not always the best choice since they require precision. For phone applications, it's better to use a radio button or a control that's larger.

On the **Insert** tab, click or tap **Controls**, and then click or tap **Drop down**. When the drop down control appears in the gallery, resize or move the drop down control to where you want it.
<!-- add screen shot here -->

Under **Dropdown** in the upper left-hand pane, type a name for the drop down control so you can easily find it. For this example, the drop down control is named **ddCountry**.
<!-- add screen shot here -->

Determine the data you want to filter on (for example, filter by country). In the formula bar next to the **Items** property, change the value to **CitySales**, which is the data in the collection. It's a best practice to add the **Distinct** function to the **Items** property to make sure the data that's retrieved is filtered on specific items. To filter the **CitySales** data by the column **Country**, type the following in the formula bar:
**Distinct(CitySales,Country)**

Connect the drop down control to the gallery by changing the value in the **Items** property for the gallery. Click or tap the gallery and make sure that **BrowseGallery1** is selected in the right-hand pane. In the left-hand pane, click or tap the **Items** property and then, in the formula bar, delete all of the text next for the **Items** property and type the following:
**Filter(CitySales,ddCountry.Selected.Value in Country)**

The drop down control is set to automatically filter the **CitySales** data by country.
