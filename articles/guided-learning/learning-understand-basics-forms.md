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
In previous video, we discussed how to prepare our data in SharePoint and created two lists: **IssuesLog** to store data the app is collecting, and **Zones** to store data on zones. The **Zones** list will be used to create a cascading drop-down control. In this section, we'll discuss the basics of creating forms.

## Create a new app in SharePoint

1. Open **IssuesLog**, and at the top, click or tap **PowerApps** and then click or tap **Create an app**.

2. In **Create an app**, under **Name**, type a name for the app. In the example, the name is **Installation issues**.

3. Click or tap **Create**.

  **Note:** Because we've already created the fields **DivisionCodes** and **Zones** that collect data, we can connect Power BI to the list and get specific information, such as how often installation issues occur and which zones the issues occur in.

4. After the app is created, add at least one item to the list before adding all the data because it'll make it easier to customize the gallery later.

  **Note:** PowerApps automatically determines which fields should go in the gallery when the app is created. In the example, the fields added include: division code, the title of the issue, comments, and how the issue was taken, such as by person or through email.

5. To expand the space for the **Comments** field, change the property to **AutoHeight** in the property list and then type **True** in the formula bar.

6. To edit the fields after the app is created, click or tap the pencil icon in the upper right-hand corner of the gallery.

  ![Pencil icon](./media/learning-understand-basics-forms/edit-template.png)

## Create a form ##
Create a form to add a cascading drop-down control. Eventually, we want to have a cascading drop-down control so that when a zone is selected, the correct division codes for that zone appear in the list.

1. In **IssuesLog**, click or tap the plus sign (+) in the upper right-hand corner to create a new item. A new blank form appears.

  **Note:** When working with forms, you're working with independent sections of the form called data cards. When you select the form, you'll see at the lower left-hand corner a file called **EditForm1** that has several different data cards in it. Each data card is independent and can have its own unique formatting. This is different from a gallery where if you make a change to one section, it affects the entire gallery.

2. Select the title of a data card in the form and then drag the data card to a different location in the form. In the example, the **Title** data card is moved to the top of the form. You can also move data cards by using options in the right-hand pane.

3. Click or tap **Comments** to select that data card and, in the right-hand pane, click or tap **Edit Multiline Text**. The size of the **Comments** data card automatically expands.

4. Make additional changes to the form, such as changing a title. Click or tap a title of a data card you want to change, and then in the right-hand pane, click or tap **Advanced**.

5. Click or tap **Unlock** to change properties. By default, PowerApps locks the ability to change properties to help minimize accidental mistakes.

6. In the form, edit the title.

7. To make the gallery larger, drag the lower edge of the gallery down since, by default, it's not a flexible height gallery.
