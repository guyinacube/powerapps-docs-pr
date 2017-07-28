<properties
   pageTitle="Understand the basics of creating forms | Microsoft PowerApps"
   description="Understand the basics of creating forms including expanding fields in a form and unlocking property settings to customize a form"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-subohe"
   manager="anneta"
   editor=""
   tags=""
   featuredVideoId="Y057qUJ2NNk"
   courseDuration="11m"/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="06/15/2017"
   ms.author="v-subohe"/>

# Creating forms in an app
In the previous session, you prepared data in SharePoint and created two lists: **IssuesLog** to store the data the app is collecting, and **Zones** to store the data on division zones and subcodes. The **Zones** list will be used to create a cascading drop-down control. This section discusses the basics of creating forms.

## Create a new PowerApp from SharePoint

1. Open the **IssuesLog** list, and at the top, click or tap **PowerApps**, and then click or tap **Create an app**.

    ![Create PowerApp](./media/learning-understand-basics-forms/create-powerapp.png)

2. Type a name for the app, for example **Installation issues**, and click **Create**.

After the app builds and opens in PowerApps Studio for Web, you can adjust the fields in the template gallery to match the view that you want. For example:

   ![Format gallery template](./media/learning-understand-basics-forms/format-gallery-template.png)

Without doing anything else, your app is now fully functional. Test the app by running it in preview mode and opening an item for editing. Make a change to one of the fields, submit the form, and verify that the change you made now appears in the SharePoint list item. 


## Add a cascading drop-down control

In left-hand navigation tree, under **EditScreen1**, select **EditForm1**. This is the form that the user will fill out when they create a new item.

![EditForm1 tree view](./media/learning-understand-basics-forms/editform-tree.png)

When working with forms, you're working with independent sections of the form called **data cards**. In left-hand navigation tree, under **EditForm1**, you can see all the data cards (and other controls) that make up the form. Each data card is independent and can have its own unique formatting. This is different from a gallery where if you make a change to the template, it affects the entire gallery.

Data cards can be arranged on the form by dragging the handle in the upper left of the data card, or by dragging the fields in the right-hand pane. They can also be resized or have their properties customized like any other control. 

![Move data cards](./media/learning-understand-basics-forms/move-data-card.png)

Modify the data cards as follows:

- Select the **ID** data card and set the **Visible** property to **false**.
- Move the **AssignedTo** field so it's above the **ContactType** field. 
- Edit the titles for **AssignedTo**, **ContactType**, and **DivisionCode** to add a space between the words. 
- Select **Comments**, and in the right-hand pane, select **Data**. Scroll down to the **Comments** field, select the **abc** drop-down, and select **Edit multi-line text**. This expands the text box to display the multi-line comment. 

Your form should look similar to this now:

![Final form edit](./media/learning-understand-basics-forms/edited-form.png)

Some data cards may be locked by default to prevent accidental changes. To unlock a data card, select the data card, select **Advanced** in the right-hand pane, and click **Unlock to change properties**.

