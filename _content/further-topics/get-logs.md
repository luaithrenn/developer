---
title: Accessing your Watson Assistant logs
weight: 40
---
### About this task#
The Watson Assistant service uses [IBM Cloud Logging](https://logging.ng.bluemix.net/app/) to log conversation data.   To learn about IBM Cloud Logging, see the [IBM Cloud Logging documentation](https://console.bluemix.net/docs/services/CloudLogAnalysis/index.html#getting-started-with-cla).

Before you can access your logs, you must send your IBM Cloud tenant ID to the Watson Assistant support team.  When logging is provisioned for you, you can access your logs files from the Watson Assistant console or directly from IBM Cloud.  <br>You can view and analyze log data in Kibana, an open source analytics and visualation tool. To learn more about Kibana, see the [Kibana 5.1 Getting Started documentation](https://www.elastic.co/guide/en/kibana/5.1/getting-started.html).

### Before you begin#
1. If you do not have an IBMid, create one. For instructions, see *Create a free account* on  [IBM Cloud](https://bluemix.net).
2. Log in to US South region of IBM Cloud. Create an org and a space for your applications or services in this region.
3. Install the [IBM Cloud cli tool](https://console.bluemix.net/docs/cli/index.html#cli).

### Procedure#
Complete these steps:

2. Install the IBM Cloud Log Analysis cli plugin.  Enter:<br>```bx plugin install logging-cli -r Bluemix```<br>
3. Log in to US South region of IBM Cloud.  Enter:<br>`bx login -a https://api.ng.bluemix.net  --sso`<br>and follow the onscreen prompts.
4. Set the target org and space of your applicaiton and services. Enter:<br>```bx target -o paste-your-org-name-here -s paste-your-space-name-here```<br>
5. Find the tenant ID of your org and space.  Enter:<br>```bx cf space paste-your-space-name-here --guid```<br>
6. Copy your tenant ID.  Your ID is similar to *a02ad488f-a456-423c-3drsg348hcv8*.
7. Send an email to the Watson Assistant support team to associate your tenant ID with your Watson Assistant instance.  Include the following information:<br>
  - Tenant ID
  - Watson Assistant API key.<br>
The Watson Assistant support team sends you an email confirming that logging is set up for your tenant ID.
8. Verify that you can access your Watson Assistant logs from the Watson Assistant console.  Log in to the console and click **Coversation logs**.  Alternatively, open the log files from [IBM Cloud Logging](https://logging.ng.bluemix.net/app/).
9. To see logs that are associated with the Watson Assistant only, enter the search string `type:watsonassistant`.
