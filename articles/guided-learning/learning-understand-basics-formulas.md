<properties
   pageTitle="Understand the basics of formulas | Microsoft PowerApps"
   description="Formulas are the key to making PowerApps work"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-subohe"
   manager="anneta"
   editor=""
   tags=""
   featuredVideoId=
   courseDuration=/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="06/28/2017"
   ms.author="v-subohe"/>

This section provides a close up look at the formula bar and how to use it.

At the top of PowerApps, the formula bar is similar to what you'd see in Excel. Formulas in PowerApps are also based on the formulas in Excel.

![Formula bar](./media/learning-understand-basics-formulas/formula-bar1.png)

## Find available functions on the formula bar
On the formula bar, click or tap the **Fx** button to browse available functions. For example, under the **Text** property, the options listed below it are typically used with text, such as **Concatenate**.

![Fx button on the formula bar](./media/learning-understand-basics-formulas/formula-fx-button.png)

On the **Insert** tab, click or tap **Label**. When it appears in the form, move the text box to a location where it doesn't cover any other fields.

Click or tap the **Fx** button, and in the list of options under **Text**, click or tap **Left**. The **Left** function appears in the formula bar and will extract the left portion of some text. In the formula bar, type:

**Left(txtDepartment.Text,3)**

This function takes the name of another field called **Marketing**, and then extracts only the initial three characters: **Mar**.

Click or tap the **Fx** button, and in the list of options under **Text**, click or tap **Concatenate**. In the formula bar, type:

**Concatenate(txtDepartment.Text, "Book")**

This function takes the name of the field called **Marketing** and concatenates (or adds) the word "Book": **MarketingBook**.

To see another example using the **Text** property, type the following in the formula bar:

**"Department: " & txtDepartment.Text**

This function adds the word **Department** to help the user identify the value, such as **Department: Marketing**.

**Note:** The formula bar uses color coding to help identify the values. For example, click or tap **txtDepartment** in the formula bar. It appears in the color red to help verify the correct control is selected. If a red dot appears in the formula bar, that means a closing parentheses is needed.

## Use formulas for SharePoint lists
Open a gallery that we used for a SharePoint list. We're going to add two fields to the gallery that are for two complex fields in SharePoint. Notice that in the right-hand pane, the drop-down lists we created earlier are not listed. For example, the drop-down list called **Follow** is not listed.

To work around this issue, go to **Text** in the property list, and in the formula bar, it currently displays **ThisItem.Comments**. Delete the word **Comments**.

Click or tap the dot to view all of the fields on SharePoint.

Click or tap to select **Follow** from the list. Notice that it's still red. This is because the formula needs an additional step. In the formula bar, type:

**ThisItem.Follow.Value**

**Value** is needed for complex lists, especially lists that require users to select an item, such as a drop-down list.

**Note:** When a red line or squiggly red line appears in the formula, it means something's missing. Click or tap the dot to find other properties that are available to use.
