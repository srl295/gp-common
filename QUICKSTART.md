Quick Start Guide
=================

Below are some steps to help you quickly get started. For more detailed information about the service, please visit the official [Globalization Pipeline  documentation](https://console.ng.bluemix.net/docs/services/GlobalizationPipeline/index.html) page.

**Lets get started!**

### 1. Create a new Globalization Pipeline service instance
Head to the [Bluemix Catalog](https://new-console.ng.bluemix.net/catalog/) and look for the Globalization Pipeline service - it should be under the DevOps category.

![Bluemix Catalog](images/catalog.png "Globalization Pipeline")

Once you click the service icon, you should be taken to the Globalization Pipeline service page where you will find more information about the service.

On this page:

1. Provide a name for your service instance
2. Connect to an application (optional)
3. Select a plan
4. Click Create

![Bluemix Catalog Entry](images/catalog-entry.png "Globalization Pipeline catalog entry")

### 2. Globalization Pipeline Dashboard
Click on the new service instance to go to the Globalization Pipeline **Dashboard**.

![Globalization Pipeline Dashboard](images/dashboard-overview.png "Globalization Pipeline Dashboard")

1. The **Getting Started** tab provides some general information about the service and some useful links.
2. The **Bundles** tab allows you to view your bundles and create new bundles.
3. The **API Users** tab allows you to create new users with different levels of access to the service instance.
4. The **Machine Translation Configuration** tab can be used to configure additional Machine Translation engines from other providers, such as [Watson Language Translation](https://new-console.ng.bluemix.net/catalog/services/language-translation/).

### 3. New Bundle
Lets go ahead and create a new Bundle. Click the **New Bundle** button and then fill in the new Bundle's information:

![New Bundle](images/new-bundle.png "New Bundle")

1. Give the Bundle a unique name so it can be identified later
2. Provide the Resource file that contains your messages
3. Select the Target languages
4. Click Save

In the example above, `messages.json` contains:

```json
{
    "greet": "Hello there!",
    "weather": "It is snowing",
    "exit": "Goodbye"
}
```

Now that the new Bundle is created, select it from the Bundles list to view the Bundle details.

![Bundle Details](images/bundle-details.png "Bundle Details")

You can now click on one of the Target languages to view the  translated messages in that language. For example, Japanese:

![Translated Messages](images/translated-messages.png "Translated Messages")

You can now download the translated messages by clicking the **DOWNLOAD** button. Or you can access the translated messages directly in your app by using one of the SDKs or Plug-ins. To get started, head to the [SDKs and Plug-ins](#download) section.

### 4. Credentials
In order to access the service instance through the RESTful API, SDKs, or Plug-ins, you will need to provide the necessary credentials. To see the credentials, find the service instance in the Bluemix dashboard and click **View Credentials**:

![New Instance](images/new-instance.png "New Instance")

![Credentials](images/creds.png "Credentials")

**Note:** If the service instance is connected to an app on Bluemix, the credentials can be accessed from the app's environment variables - the SDKs automatically take care of this.

**Caution!** The default credentials shown above provide complete access to the service instance, including the ability to delete and modify bundles. When you are using the service in a production app, it is recommended that you create a new **Reader** account through the **API Users** tab. The Reader account can only read bundle data.