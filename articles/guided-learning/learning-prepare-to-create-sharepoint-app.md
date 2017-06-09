<properties
   pageTitle="Add data to SharePoint to prepare to create an app | Microsoft PowerApps"
   description="Build additional data into SharePoint to prepare for creating an app"
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
   ms.date="06/07/2017"
   ms.author="v-subohe"/>

We've already created two apps for Contoso hardwood flooring. The first app we created was to estimate the cost of the flooring for the size of the room, and we created the second app to display the sales figures for the cities and countries. Next, we're going to create an app for people who are out installing the flooring. When they're installing flooring, issues can occur, so this app let's them log the problems they encounter. The new app will store the data on SharePoint, and people can continue to add issues to the SharePoint list using the app.

## Add a new SharePoint app
In the SharePoint site, click or tap the **Setting** icon in the upper right-hand corner of the web browser, and then click or tap **Add an app**.

In the list of template apps that are displayed, select **Custom List**. If you don't see the **Custom List** template, search for it in the **Search** box.

In **Add Custom List**, type **IssuesLog** as the name for the app, and then click or tap **Create** to create the log where the data will be stored.

When you create a new app in SharePoint using the Custom List template, it shows up in a list under **Contents**. In the list, find **IssuesLog** and open the file.

When the file opens, it displays a list <!-- actually, it looks like a table, but Audrie is using the word 'list' here --> with a **Title** column and a plus sign **(+)** column.

## Add columns to the list
Add five new columns to the list to add more data to the list.
<!-- It would be helpful to have access to the SharePoint site Audrie's using, which is https://microsoft.sharepoint.com/teams/PlanningTeamSite/Lists/IssuesLog. This will help me take screenshots that pertain to these steps. -->
To add a new single line column, click or tap **(+)** and then click or tap **Single line of text**. In **New text column**, type **ContactType** for the name, and then click or tap **Create**. The new column provides data on how the contact was made for the issue, such as by a phone call, in person, or through an email.

<!-- work on the organization here since we're adding a total of 5 new columns and the steps are very similar, perhaps  -->
For the next column, click or tap **(+)** and then click or tap **Person**. In **New person column**, type **AssignedTo** for the name, and then click or tap **Create**. This column allows you to assign different issues to different people.

Add a vendor column. Click or tap **(+)** and then click or tap **More...** to add a choice list. In **Name and Type**, under the **Column name**, type **Vendor**. Under **Type of information listed in the column**, click or tap **Choice (menu to choose from)**. In **Additional column settings**, in the box under **Type each choice on a separate line**, type the following:
**Vendor Name 1**
**Vendor Name 2**
**Vendor Name 3**

In **Default value**, type **Vendor Name 1** for the default because it's the name that will be used the most. Click or tap **OK** to see how the columns look.

Add a new column with a division code. Click or tap **(+)** and then click or tap **Single line of text**. In **New text column**, type **DivisionCode** for the name, and then click or tap **Create**.

Add a new column for resolved. Click or tap **(+)** and then click or tap **Yes/No**. In **New text column**, type **Resolved** for the name, and then click or tap **Create**.

Add a new column for comments. Click or tap **(+)** and then click or tap **Multiple lines of text**. In **New multiline text column**, type **Comments for the name**, and then click or tap **Create**.

Now we have all of the columns we need.
<!-- screenshot of the list needs to go here-->

Before starting to work on the app, add one line of data to assess how the fields are placed when we start customizing the app.
<!-- left off here, finish editing topic on Monday-->

Click or tap **New** in the upper left-hand corner, and in **New Item**, add this information to each field:
Title: Missing Corner Tiles
ContactType: In Person
AssignedTo: Audrie Gordon
Vendor: Vendor Name 1
DivisionCode: 101
Comments: Installation box was missing 2 tiles, please arrange for replacement.
Click **Save** to save the item.

## Add a cascading drop down for the DivisionCode field
There are 3 division zones, and each zone has different codes. We want to be able to pick the zone and show only the codes for that zone. To do this, you need toa add a new SharePoint app. In the SharePoint site, click or tap the Setting icon in the upper right-hand corner of the web browser, and then click or tap Add an app.
In the list of template apps that are displayed, select Custom List.
In the Adding Custom List box, name the app Zones. Click or tap Create.
For this app, we only need one more column. Create a new Single line of text column and call it SubCodes.
Click or tap Quick edit in the upper left-hand corner to add the zones. The first 2 zones have 3 subcodes, and the third zone has 2.
<<need a screenshot here to show the zones that are added>>

Click or tap Site Contents in the left-hand pane, and then open IssuesLog.

The next video will talk about how to build the app.
