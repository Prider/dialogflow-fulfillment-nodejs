# Dialogflow Fulfillment Library Alpha

| Alpha |
|-------|
| This is an Alpha release of Dialogflow's fulfillment library. This library might be changed in backward-incompatible ways and is not recommended for production use. It is not subject to any SLA or deprecation policy. |

The Dialogflow Fulfillment Library makes creating fulfillment for Dialogflow v1 and v2 agents for 8 chat and voice platforms on Node.js easy and simple. Cross-platform text, card, image, suggestion and custom payload responses are supported for Actions on Google, Facebook, Slack, Telegram, Kik, Skype, Line, Viber and Dialogflow's simulator.

Dialogflow fulfillment allows you to connect Dialogflow's natural language understanding and processing to your own systems, APIs and databases. Using fulfillment, you can surface commands and information from your services to your users through a natural conversational interface. More about Dialogflow fulfillment: https://dialogflow.com/docs/fulfillment

## Quick Start

1. [Sign up for or sign into Dialogflow](https://console.dialogflow.com/api-client/#/login)
1. Create a Dialogflow agent
1. [Enable the Cloud Function for Firebase inline editor](https://dialogflow.com/docs/fulfillment#cloud_functions_for_firebase)
1. Copy this code in `samples/quick-start/functions/index.js` the `index.js` file in the Dialogflow Cloud Function for Firebase inline editor.
1. Add `"dialogflow-fulfillment": "alpha"` to the `package.json` file's `dependencies` object in the Dialogflow Cloud Function for Firebase inline editor.
1. Click `Deploy`


## Setup Instructions

 1. Import the appropriate class:

```javascript
const WebhookClient = require('dialogflow-fulfillment');
```

 2. Create an instance:

```javascript
const agent = new WebhookClient({request: request, response: response});
```

## Reference
* Class Reference: [docs](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/tree/master/docs)
* Dialogflow documentation: [https://docs.dialogflow.com](https://docs.dialogflow.com).

## Issues and Questions
* If you find any issues, please open a bug on [GitHub](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/issues).
* Questions are answered on [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow).
* Known Issues/Limitations
    * No SSML support
    * No support for follow up events (follow up event docs: [v1](https://dialogflow.com/docs/fulfillment#requirements), [v2](https://dialogflow.com/docs/reference/api-v2/rest/v2beta1/WebhookResponse))
    * No checking for if a certain combination of response is incompatible with certain platforms (i.e. multiple cards are not support in a single Actions on Google Response)


## How to make contributions?
Please read and follow the steps in the CONTRIBUTING.md.

## License
See LICENSE.md.

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).
