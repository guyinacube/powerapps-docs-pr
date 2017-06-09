<properties
   pageTitle="Create a data source by using a formula | Microsoft PowerApps"
   description="Build a data source using only a formula and, later, use the data source to build galleries."
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

In this section, you'll add a data source by using a formula, and eventually, you'll use the data source you created to build galleries. The steps in this section are intended for PowerApps Desktop. If you're using PowerApps in a web browser, the steps will vary slightly.

## Create a data source
<!--I should add a link to the resources text file here with the link on the word 'resources' in 1st sentence -->
In your resources, there's a text file called *CollectionDataFormula.txt*. This file contains a large formula that you'll use to create a table of data that lists the sales figures for each city. The formula uses the function **ClearCollect** to delete all records from a collection and then add a different set of records to the same collection. In this example, **CitySales** will be the name of the collection you create.

**Note:** In the text file, some words, such as **City**, are followed by a colon(:). These words represent column headers in a table. The words that follow the column headers are in quotes and represent the value for that column header.

To create a collection that you'll use in the galleries, first select all of the data in the text file.

1. With *CollectionDataFormula.txt* open, select all of the text in the file (for example, press Ctrl+A), copy it (Ctrl+C), and then paste (Ctrl+V) the text into NotePad.

  **Note:** It's recommended that you use NotePad when copying and pasting the data because if you use another application, some of the text that you copy could be altered and won't work in PowerApps (for example, curly quotes).

2. Open PowerApps, and in the left-hand pane, click or tap **New**, and then click or tap **Phone Layout**. After you do this, a new screen in PowerApps appears.
<!-- add screenshot here? -->

3. Click or tap **OnVisible** in the **Property** list in the left-hand pane.

4. In the formula bar, <!--verify what this UI area should be called. Should it be formula bar or formula text area? --> paste the data you copied from *CollectionDataFormula.txt* (the data contains the function **ClearCollect** with a list of sales figures from several countries and cities). To see the entire formula, scroll to the right and make the formula bar larger. The information you pasted appears in different colors to help you make sure that the information was correctly copied over. <!-- add screenshot with the formula text here? The formula text is really long though -->

5. On the **Insert** tab, click or tap **New Screen** near the top of the PowerApps window to create a new screen. This creates a trigger for the **OnVisible** property so that the collection is built.

6. On the **Content** tab, look in **Collection** and you'll see the table you created. You won't see all of the data, but you'll see the first five rows. Review the table to make sure that you have all the data you need.

<!--Audrie ends the video by not saving the app, and she starts the next video by having you save the app created in the first video. I thought it would be best to include a step here on saving your app -->

7. After making sure all of your data is in the app, in the left-hand pane, click or tap **Save As** (or press Ctrl-S) to save the app you created. Make sure you save the app to the cloud, give it an appropriate name, and provide a description. A helpful tip when saving your app is to change the icon. This makes your app stand out in the list and people can easily find it.
