<properties
   pageTitle="Prepare Excel data to use in an app | Microsoft PowerApps"
   description="Use data in an Excel spreadsheet as a data source for an app"
   services=""
   suite="powerapps"
   documentationCenter="na"
   authors="v-subohe"
   manager="anneta"
   editor=""
   tags=""
   featuredVideoId=""
   courseDuration=""/>

<tags
   ms.service="powerapps"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="na"
   ms.date="08/07/2017"
   ms.author="v-subohe"/>

# Preparing Excel data to use in an app
In this topic, we'll discuss how PowerApps expedites building apps. In the next topic, we'll create an app for the sales associates of Contoso Flooring company to use on their mobile devices. The app will be used to show the customers how the installation process works. Before we create the app, we need to create a data source.

## Create a data source
Use a data source that let's you set up tabular data. In the example, we'll use Excel as a data source.

When using an Excel spreadsheet as a data source with PowerApps, the data range must be formatted as a table. Having the data range formatted as a table tells PowerApps exactly what range of data to use. Since Excel normally has hundreds of columns and rows, the data can be anywhere. By defining a data range, we're telling PowerApps that this is the data we'd like to use for our app. To format data as a table:

1. Open your Excel worksheet and select the data range, including the column header. 

1. On the **Home** tab in Excel, click or tap **Format as Table** and select a style.

1. On the **Formulas** tab in Excel, click or tap **Name Manager**. In **Name Manager**, the default name for the range is **Table**. Click or tap **Edit** and rename the data range to **Videos**.

1. Save the Excel file. The data source is ready to use when we build our app.
