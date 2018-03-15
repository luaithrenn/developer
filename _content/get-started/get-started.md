---
title: About the IBM Watson Assistant Solution
weight: 10
---
IBM Watson Assistant Solution is a framework for building personal assistants that automate tasks or answer questions in response to natural language input from a user.  Using the framework, you can build an assistant that has *multiple* skills.  A skill is a capability in a specific domain, for example, making restaurant reservations or answering general knowledge questions.

Skills are developed using natural language understanding (NLU) engines, such as the IBM Watson Conversation service on IBM Cloud.  You can choose from the pre-built skills that are provided with Watson Assistant out-of-the-box or you can develop your own custom skills from a boilerplate.

You can add intelligence to your skills to provide a customized experience for the your end user.  Contextual information is the type of information that changes frequently, such as location or the time of day. Making use of contextual information enables your assistant to:
- Respond in a personalized way.
- Use previous responses to enhance the conversation.
- Use contextual information across skills.

##How it works
When your assistant receives user input, the request is routed to all skills. Each skill determines how capabile it is of deliverying a resource.  The request is routed to the skill with the highest confidence scroe.

##Setup 

Configure skills & devices using APIs or via

Watson Assistant capabilities that are in beta mode are tagged with **[BETA]**.

* Firstly, [register]({{site.baseurl}}/get-started/get-api-key) for the Watson Assistant service.
* While you're waiting for your request to be approved, [understand]({{site.baseurl}}/understand-service/overview) the Watson Assistant service.
* When your request is approved, you will receive an API key to access your personal assistant.
* If you want to use Bluemix or Watson services to power your application, you must request access to those services separately.
* Using your API key, [create a simple skill]({{site.baseurl}}/skill/what-are-they) to learn how you go about giving your application intelligence.
* Lastly, [complete a _proactive_ tutorial]({{site.baseurl}}/knowledge/what-is-kr) to learn how to make your application proactive using the Knowledge and Rules service.
