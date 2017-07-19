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

# Create a data source using a formula
In this section, you'll create a data source by using a formula, and eventually, you'll use the data source  to build galleries. The steps in this section are intended for PowerApps Desktop. When using PowerApps in a web browser, the steps may vary slightly.

## Create a data source
<!--Add a link to the resources text file here with the link on the word 'resources' in 1st sentence -->
In resources, you'll find a text file named *CollectionDataFormula.txt*. This file contains a large formula that you'll use to create a collection, or table, that lists the sales figures for different cities. The formula uses the **ClearCollect** function, which clears, or deletes, all the records from a collection and then adds a different set of records to the same collection. If the collection doesn't exist, it will create the collection. In this example, you'll create a collection named **CitySales**.

**Note:** The data in the text file is formatted for the **ClearCollect** function as follows:
  - The data between each set of curly braces "**{ }**" is a single record, or row. 
  - Column names are immediately followed by a colon (**:**), for example "**City:**".
  - The value for each column in a record comes after the colon (**:**) and ends with a comma (**,**). Numerical values are written without quotes, but text values must be in quotes, for example, **City:"Seattle",** and **Sales:1657500**. 

To create a collection to use in the galleries, first select all of the data in the text file.

1. Use NotePad to open *CollectionDataFormula.txt*, select all of the text in the file (for example, press Ctrl+A), and copy it (Ctrl+C).

   **Note:** It's recommended to use a text editor such as NotePad to open and copy the data. Using a word processor, such as Word, can introduce unintended formatting into the text which PowerApps won't recognize, for example, curly quotes.
   

2. Open PowerApps, click or tap **New** on the **File** menu (near the left-hand edge).

3. On the **Blank app** tile, click or tap **Phone layout**.

   ![Insert drop-down](./media/learning-create-data-source/blank-app.png)

   A new app with a blank screen will open in the PowerApps workspace.

4. Select **OnVisible** in the **Property** list drop-down.

   ![Set OnVisible property](./media/learning-create-data-source/onvisible.png)

5. In the formula bar next to **OnVisible**, paste the data that you copied from *CollectionDataFormula.txt*. (The data contains the  **ClearCollect** function with a list of sales figures from several countries and cities). To see the entire formula, expand the formula bar by dragging down the bottom edge. Notice that the information displays in different colors - column names in black, text values in red, and so on - to make it easier to see the information.

   ![Copy data](./media/learning-create-data-source/copy-data.png)

6. On the **Insert** tab, click or tap **New Screen**, and select **Blank** to create a new screen. In the left-hand pane, select **Screen1**. Going back to **Screen1** this way triggers the **OnVisible** property of the screen so that the collection is built.

   ![New screen](./media/learning-create-data-source/new-screen.png)

7. On the **View** tab, click or tap **Collections** and make sure the table was created. You won't see all of the data in the table, only the first five rows. Review the table to make sure all of the data is there.

   ![View collection](./media/learning-create-data-source/view-collection.png)

8. In the left-hand pane, click or tap **Save As** (or press Ctrl-Shift-S) to save the app. Make sure to save the app to the cloud, give it an appropriate name, and provide a description. A helpful tip when saving an app is to change the icon. This makes the app stand out in the list and people can easily find it.

   ![Save as](./media/learning-create-data-source/save-as.png)

<!--Audrie ends the video by not saving the app, and she starts the next video by having you save the app created in the first video. I thought it would be best to include a step here on saving your app -->
