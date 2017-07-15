<properties
   pageTitle="Determine whether a form is in edit mode | Microsoft PowerApps"
   description="Differences between an edit form and a new form"
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
   ms.date="06/23/2017"
   ms.author="v-subohe"/>


# Understand the difference between an edit form and a new form
In the previous video, we discussed how to create cascading drop-down lists. In this section, we'll discuss some differences between an edit form and a new form and why it's important for the cascading drop-down lists.

## Edit forms and a new forms 
When you add an edit form, you're basically adding two forms at the same time because an edit form can convert to a new form when it needs to. With an existing item in a SharePoint list, if you click or tap the pencil icon, the item is in edit form. It's the same exact form but in a mode called edit. When you click the plus sign (+) in an item, you create a new form. In edit form, you want the SharePoint list to look at the data that's currently set. Be careful when you make changes to the default values as you need to be aware of what mode the form is in.

## Determine whether a form is in edit mode
In the previous video, we made the **Division Code** field invisible. To see hidden fields in a form, press and hold the **Alt** key, which shows all fields whether they're hidden or not. Then, click or tap the **Division Code** field to select it.

Go to **Visible** in the property list, and in the formula bar, type **True** to make the field visible again.

For the **Division Code** field, the value for the **Default** property is set to **ddSubCodes.Selected.Value**. As a best practice, when we're in edit mode, make sure the division code is always retrieved from the SharePoint list. To make sure this happens, we need to add an **If** statement to the **Default** property. In the formula bar, type:
**If(EditForm1.Mode=FormMode.Edit,Parent.Default,ddSubCodes.Selected.Value)**

This is important because the data for the **Zones** drop-down list doesn't exist in the SharePoint list that we're pulling data from. To get the default value for **Zones**, we need to look up the zone for the division code if it's in edit form.
For the **Default** property of the **Zones** drop-down list, type the following in the formula bar:
**If(EditForm1.Mode=FormMode.Edit,LookUp(Zones,ThisItem.DivisionCode in SubCode,Title))**

This formula checks to see if the form is in edit mode and, if it is, then it looks up the values.

The data in the **SubCodes** drop-down list is pulled from the SharePoint list. For this drop-down list, go to **Default** in the property list, and in the formula bar, type:
**If(EditForm1.Mode=FormMode.Edit,ThisItem.DivisionCode)**

This formula says if the form is in edit form, then the default value should come from the SharePoint list.

The key point in this video is to help you understand if a form's in edit mode, then it needs to go look up the source for the field in SharePoint. However, if it's a new form, then we want to ignore those default values and just use the actual raw data.

Add a new item to **IssesLog** to test your changes and then review it in edit mode.
