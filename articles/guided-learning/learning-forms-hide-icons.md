<properties
   pageTitle="Hide icons in a form | Microsoft PowerApps"
   description="Hide icons in a form"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-subohe"
   manager="anneta"
   editor=""
   tags=""
   featuredVideoId=123
   courseDuration=/>

   <tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="08/04/2017"
   ms.author="v-subohe"/>

# Hiding icons in a form
In the past few topics, you've learned about the basic fields in forms, how to add a cascading drop-down list, and how to manage default fields (in edit form mode versus new form mode). The app you've created is working properly both in a web browser and on a mobile device.

## Show or hide icons at different times ##
Showing or hiding icons in an app is an optional step you can take. For example, the **Contact Type** field is set when the user selects one of the three methods for reporting an issue (by selecting either the **Phone**, **Mail**, or **People** icon). Normally, users don't go back and change their contact method, so you may want to hide the **Contact Type** icons once the item has been created. In other words, you want the field to be visible in the **new form mode**, and hidden in the **edit form mode**.

1. Press the **Ctrl** key and tap all three icons to multi-select them.

1. Select **Visible** in the property list, and in the formula bar, type **EditForm1.Mode=FormMode.New**.

    The formula is evaluated whenever the edit form is opened. If it's **true**, and the user is in **new form mode**, then the icons are visible. If it's **false**, and they are in **edit form mode**, then the icons are hidden.

1. To test the changes, preview the app. Create a new item, and the icons will display under the **Contact Type** field. Open an existing item, and click or tap the pencil icon to edit it. Because the form is now in **edit form mode**, the icons are hidden.
