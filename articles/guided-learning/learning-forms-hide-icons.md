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
   featuredVideoId=
   courseDuration=/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="06/28/2017"
   ms.author="v-subohe

In the past few videos, we've learned about the basic fields in forms, how to add a cascading drop-down list, and how to manage default fields (edit form versus new form). The app we've created is working properly both in a web browser and on a mobile device.

## Show or hide icons at different times ##
Showing or hiding icons in an app is an optional step we may want to do. For example, the **Contact Type** field is set once the user selects one of the three methods for reporting the issue (by clicking or tapping either the **Phone**, **Mail**, or **People** icons). Normally, users don't go back and change it later, so we may want to hide the **Contact Type** field after we've seen it.

1. Click or tap each icon in the **Contact Type** field (press the **Ctrl** key to select all three at once).

2. Drag the icons to move them higher in the field. Since we're not using a flexible height gallery, even when we move the icons, the size of the field remains the same.

  **Note:** If a flexible height gallery is used, then the field resizes when the icons are hidden.

3. Go to **Visible** in the property list, and then in the formula bar, type **EditForm1.Mode=FormMode.New**.

The only time the icons are visible is if the form is new. If it's in edit mode, the icons are invisible.

To test the changes, preview the app. Click or tap the plus sign (+) and the icons display in the **Contact Type** field. Click or tap the pencil icon, and, because the form is now in edit mode, the icons are invisible.

After this series of videos on forms, we've learned that PowerApps can do many different things, such as adding cascading drop-down lists and hiding and showing items in a form, without actually writing any code. Next, we'll build an app from end-to-end, learn about error management, and learn how to manage an app.
