<properties
   pageTitle="Add a cascading drop-down list | Microsoft PowerApps"
   description="Add a data source and then add some cascading drop-down lists"
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
   ms.date="06/20/2017"
   ms.author="v-subohe"/>

#Cascading drop-down lists
In the last video, we learned some basic information about forms and how forms combine with columns in our SharePoint lists. We also learned about locking and unlocking property settings in order to customize forms.

In this section, we'll add a cascading drop-down control because, when a zone is selected, we want the correct division codes <!--subcodes?--> for that zone to appear in the drop-down list. The subcode that's selected needs to be automatically added to the list under the **DivisionCode** column. To do this, we'll need to connect to the data source that has the data needed for the cascading drop-down lists.

**Note:** There's already a data source connection to **IssuesLog** when the app was created.

## Add a data source to use for the cascading drop-down list ##

1. In the right-hand pane, click or tap **Add data source**. In the list of connections, click or tap the connection you want to use.

  **Note:** If you don't see the connection you want to use, click or tap **New connection**.

2. Under **Connect to a SharePoint site**, copy and paste the URL for the SharePoint site (in the example, it's https://microsoft.sharepoint.com/teams/PlanningTeamSite), and then click or tap **Go**.

  PowerApps searches for all of the lists that are available on the SharePoint site. In the list, find **Zones** and select it. Then, click or tap **Connect**. In the right-hand pane, notice that there are now two data sources in the list.

  **Note:** With PowerApps, you can add many types of connections. For example, you can add a connection to Dynamics 365 and include account data from Dynamics 365 at the same time you're submitting data to a SharePoint list. You can also add connections to third-party applications.

## Add cascading drop-down lists ##
Now that you've added the **Zones** connection, add the cascading drop-down lists to the form.

1. At the bottom of the form, click or tap **Add a custom card** to add a custom card to the form.

2. On the **Insert** tab, click or tap **Controls** and then click or tap **Drop down**.

  ![Insert drop-down](./media/learning-add-data-dropdown/insert-control-dropdown.png)

  We'll add two drop-down lists, one for the top-level **Zones**, and the second for **Subcodes**.

  When creating the second drop-down list, copy the first one and move it down. Name the first drop-down list **ddZones** and the second one **ddSubCodes**.

3. Click or tap the first drop-down list, **ddZones**, and go to **Items** in the property list. In the formula bar next to **Items**, type **Distinct(Zones,Title)**.
The **Distinct** property is needed because the title **Zones** is repeated in the form.

4. Click or tap the second drop-down list, **ddSubCodes**, and go to **Items** in the property list. In the formula bar next to **Items**, type the following:
  **Filter(Zones,Title=ddZones.Selected.Value).SubCode**

  This function retrieves the data in **Zones** where the **Title** field is equal to **ddZones** and returns the subcode.

5. Run the app to see if the cascading drop-downs work correctly.

## Connect the cascading drop-down lists to the SharePoint list ##
Connect both of the cascading drop-down lists to the **Division Code** column in the SharePoint list.

1. In the form, move the card you created for the drop-down lists to the space above the **Division Code** field.

2. Click or tap the **Divison Code** field and go to **Default** in the property list. In the formula bar next to **Default**, type **ddSubCodes.Selected.Value**.

  The function changes the default setting in the **Division Code** field so that it automatically displays whatever is selected in the **ddSubCodes** drop-down list.

3. (Optional) Since the **Division Code** field is no longer needed, you can hide it. Go to **Visible** in the property list, and in the formula bar, type **False**.
