<properties
   pageTitle="The Common Data Service: Advance Apps | Microsoft PowerApps"
   description="Building Advanced Applications with the Common Data Service"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-brbene"
   manager="anneta"
   editor=""
   tags=""
   featuredVideoId="os33pHQ9jSU"
   courseDuration="7m"/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="6/20/2017"
   ms.author="v-brbene"/>

# Building advanced applications with the Common Data Service

In this video, we’re going to talk about the different ways that you can build your apps with the Common Data Service. One of the great things about the Common Data Service is that we have application creation experiences for different skill levels. We’ll look at some of these experiences in this session. 

Let’s take a quick tour of some of these options.

- First, you can build your apps with PowerApps. Most of the steps in this process are automated. To create your application, you select the desired layout, choose the Common Data Service data source, find the entity you want to use, and then let PowerApps automatically build your app.
- Next, you can build what we call a **powered-up** PowerApp. In this case, you can hook an Azure function into your app via custom APIs. The Azure function can have custom logic and complex queries that use the Common Data Service C# SDK.  To use this method, first register the app with Azure AD, and then build your Azure function. 
- A third way is to use the Common Data Service C# SDK in a middle tier, deploy that middle-tier, and then build a Rich Client Application on top of that. 
- And finally, you can use the Common Data Service C# SDK directly in your web apps or SaaS applications. 

Let’s look at two of these options, starting with the PowerApps experience. 

## Create an app with PowerApps

On the **PowerApps page**, click **New app**.

![Create a new app](./media/learning-common-data-service-advanced-apps/powerapps-new-app.png)

In the **Blank app** template, click **Tablet layout**. 

![Tablet layout](./media/learning-common-data-service-advanced-apps/tablet-layout.png)

In the left navigation bar, click or tap an icon in the upper-right corner to switch to the thumbnail view. 

![Toggle the views](./media/learning-common-data-service-advanced-apps/toggle-view.png)


Click **Add Data Source**, click **Common Data Services**, select **Flooring Estimates**, and click **Connect**.

![Connect to CDS](./media/learning-common-data-service-advanced-apps/add-data-source.png)

Click **Insert**, click **Forms**, and then select **Entity form**.

![Add entity form](./media/learning-common-data-service-advanced-apps/insert-entity-form.png)

Expand the data source list and select the Common Data Service that you connected to above. 

![Select data source](./media/learning-common-data-service-advanced-apps/select-data-source.png)

Next, we’ll create a second screen to view the details of each item. 

Click **New screen**, and click **Blank**. Add an entity form to this new screen and bind it to the Common Data Service using the same steps as above. 

![Add new screen](./media/learning-common-data-service-advanced-apps/new-blank-screen.png)

Click **Advanced**, and search for **pattern**. In the **Pattern** field, enter **FormPattern.Details** as the value. 

![Configure pattern value](./media/learning-common-data-service-advanced-apps/pattern-value.png)

Click on the first screen, click on the entity form, and then click **Options**. Under **PrimaryID**, select **Screen2** as the value for **Navigate**. This will set the **PrimaryID** column as a clickable link that will take you to the second screen. 

![Configure navigation](./media/learning-common-data-service-advanced-apps/options-screen.png)


Click on the second screen, click the entity form, and select **Advanced**. Search for **item**, and in the **Item** field, add **NavigationContext** as the value.  This tells the form to load the data from the item that was previously clicked on the first screen. 

![Load form](./media/learning-common-data-service-advanced-apps/navigation-setting.png)

Remaining on the second screen, click **Insert**, and then click **Button**. Drag the button to an empty space on the screen, and in the button's **OnSelect** field, enter **Navigate(Screen1, ScreenTransition.Fade)**. 

![Navigation button](./media/learning-common-data-service-advanced-apps/navigation-button.png)

Click the play button and test the app. Although this is a simple app, it shows how quickly you can create a tablet view that shows all the information inside of the Flooring Estimates entity, provide a deeper look into the details, and navigate back and forth. 

## Create an app with the Common Data Service C# SDK

Pro developers can use the Common Data Service C# SDK to either increase the complexity of logic that is used in a PowerApp, or for building Rich Clients or SaaS and web applications. 

Apps that are using the SDK need to be registered with Azure AD, so they can make requests and use the Common Data Service. We won’t build an entire SDK-based app in this session, but we will look at a few of the patterns you can support with the SDK, including rich queries. The SDK is built on a link-based syntax, and supports actions such as create, delete, insert, and update.  

![Visual Studio example](./media/learning-common-data-service-advanced-apps/vs-sdk-example.png)
 
1. This is an example of how you can query the Common Data Service. In this case, the query looks for two product categories – **Surfaces** or **Phones**. In general, you’ll create a query builder, provide the **where** clauses, (in this case where the name of the product category is either **Surface** or **Phone**), and get back the category ID and name for the product category.

2. This is a Delete action to clean up any existing cateogories.

3. In this procedure, you have an insert operation to insert new entries into the **Product Category** entity. Two categories are created and inserted - one for the **Surface**, and one for the **Phone**.  

The SDK works on batches - this is how PowerApps can optimize moving large amounts of data back and forth. Simply create the insert request for Surface, and the insert request for Phone, and then execute those requests. This is just the beginning of what you can do with the Common Data Service C# SDK, and in the coming months you’ll continue to see more and more features using the SDK from the PowerApps team.