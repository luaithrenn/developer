---
title: Linking your Watson Assistant API key with your your IBMid
weight: 30
---

You can use your Watson Assistant API key or your IBMid to log in to the Watson Assistant console, An IBMid is a free, single ID and password that you can across the ibm.com domain, including IBM Cloud.

Before you can use your IBMid to log in, you must create an entry for your IBMid in the IBM Cloud Identity and Access Management (IAM) system.  When you receive your IAM ID, submit a request to the Watson Assistant support team to link your  your Watson Assistant API key with your IBMid.


Complete these steps:
1.  If you do not have an IBMid, create one. For instructions, see *Create a free account* on  [IBM Cloud](https://bluemix.net).
2.  Create a platform API key.  For instructions, see *Managing user API keys* in IBM Cloud Docs.
3.  Request an access token from the IAM system.  Using your platform API key, enter:<br>```curl -X POST "https://iam.bluemix.net/oidc/token" -H "Content-Type: application/x-www-form-urlencoded" -H "Accept: application/json" -d "grant_type=urn%3Aibm%3Aparams%3Aoauth%3Agrant-type%3Aapikey&apikey=your-platform-API-key"```<br>The IAM system returns a JSON blog that incudes *access_token*, *refresh_token*, *token_type*, *expires_in* and *expiration*.
**Important**: Copy only your access token from the JSON blob.
4. Request an IAM ID from the IAM system.  Using your access token, enter<br>```curl -X POST https://iam.bluemix.net/oidc/introspect -H 'content-type: application/x-www-form-urlencoded' -d token=your-IAM-access-token```<br>The IAM system returns your IAM ID.  Look for *"iam_id" "your_iam_id"* and copy your IAM ID.
5.  Send an email to the Watson Assistant support team to link your Watson Assistant API key with your IBMid.  Include the following information:<br>
  - IBMid
  - IAM ID (Starts with *IBMid-*)
  - Watson Assistant API key
6. Verify that you can log in to the Watson Assistant console using your IBMid.  <p>When you recieve an email from the Watson Assistant support team that confirms that your IBMid and your API key are now linked, log in to the console using your IBMid.  For log in instructions, see [Accessing the Watson Assistant Service]({{site.baseurl}}/get-started/get-api-key/).</p>
