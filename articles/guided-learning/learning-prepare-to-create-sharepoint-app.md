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

## Add a new SharePoint app ##
1. In the SharePoint site, click or tap the **Setting** icon in the upper right-hand corner of the web browser, and then click or tap **Add an app**.

2. In the list of template apps that are displayed, select **Custom List**. If you don't see the **Custom List** template, search for it in the **Search** box.

3. In **Add Custom List**, type **IssuesLog** as the name for the app, and then click or tap **Create** to create the log where the data will be stored.

  When you create a new app in SharePoint using the Custom List template, it shows up in a list under **Contents**. In the list, find **IssuesLog** and open the file.

  When the file opens, it displays a list <!-- actually, it looks like a table, but Audrie is using the word 'list' here --> with a **Title** column and a plus sign **(+)** column.

## Add columns to the list ##
In **IssuesLog**, create six new columns to add more data to the list.
<!-- It would be helpful to have access to the SharePoint site Audrie's using, which is https://microsoft.sharepoint.com/teams/PlanningTeamSite/Lists/IssuesLog. This will help me take screenshots related to these steps. -->
1. To add a new single line column, click or tap **(+)** and then click or tap **Single line of text**. In **New text column**, type **ContactType** for the name, and then click or tap **Create**. The new column provides data on how the contact was made for the issue, such as by a phone call, in person, or through an email.

2. To add a column named **AssignedTo**, click or tap **(+)** and then click or tap **Person**. In **New person column**, type **AssignedTo** for the name, and then click or tap **Create**. This column allows you to assign different issues to different people.

3. To add a column named **Vendor**, click or tap **(+)** and then click or tap **More...** to add a choice list.

  In **Name and Type**, under the **Column name**, type **Vendor**.

  Under **Type of information listed in the column**, click or tap **Choice (menu to choose from)**.

  In **Additional column settings**, in the box under **Type each choice on a separate line**, type the following:
  **Vendor Name 1**
  **Vendor Name 2**
  **Vendor Name 3**

  In **Default value**, type **Vendor Name 1** for the default because it's the name that will be used the most. Click or tap **OK** to see how the columns look.

4. To add a column with a division code, click or tap **(+)** and then click or tap **Single line of text**. In **New text column**, type **DivisionCode** for the name, and then click or tap **Create**.

5. To add a column named **Resolved**, click or tap **(+)** and then click or tap **Yes/No**. In **New text column**, type **Resolved** for the name, and then click or tap **Create**.

6. To add a column for comments, click or tap **(+)** and then click or tap **Multiple lines of text**. In **New multiline text column**, type **Comments for the name**, and then click or tap **Create**.

7. Before starting to work on the app, add one line of data to assess the layout of the fields. Click or tap **New** in the upper left-hand corner, and in **New Item**, add some data in each field in the list. Click or tap **Save** to save the item.

## Add a cascading drop-down list for the DivisionCode field ##
There are three division zones and each zone has different codes. We want to be able to pick a zone and then show only the codes for that zone using a cascading drop-down list. To do this, you need to add a new SharePoint app.

1. In the SharePoint site, click or tap the **Setting** icon in the upper right-hand corner of the web browser, and then click or tap **Add an app**.

2. In the list of template apps that are displayed, select **Custom List**. If you don't see the **Custom List** template, search for it in the **Search** box.

3. In **Add Custom List**, type **Zones** as the name for the app, and then click or tap **Create**.

4. With the new app **Zones** open, create a single line column. Click or tap **(+)** and then click or tap **Single line of text**. In **New text column**, type **SubCodes** for the name, and then click or tap **Create**.

5. Click or tap **Quick edit** in the upper left-hand side to add the zones. In the table that appears, under the **Title** column, type each zone, and, under the **SubCode** column, type each subcode. In the example, the initial two zones have three subcodes, and the third zone has two. Use this list as a basis for the cascading drop-down list.

6. Click or tap **Site Contents** in the left-hand pane, and then open **IssuesLog**.

In the next video, we'll discuss how to build the app.
