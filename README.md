# Skype Calling Bot Sample

A sample bot showing how to use the Skype Bot Plaform for Calling API for receiving and handling Skype voice calls.

The bot shall handle the call, record it and send it for analysis to the BING API.
Then it recieves the text and sends it to LUIS for text analysis. 
    
### Code Highlights

Skype Bot Platform for Calling API provides a mechanism for receiving and handling Skype voice calls by bots.

### Prerequisites

The minimum prerequisites to run this sample are:
* The latest update of Visual Studio 2015. You can download the community version [here](http://www.visualstudio.com) for free.
* Skype Preview. To install the Skype Preview, get the app from [here](https://www.microsoft.com/en-us/store/p/skype-preview/9wzdncrfj364).
*  To fully test this sample you must:
   *  [Publish your bot, for example to Azure](https://docs.microsoft.com/en-us/bot-framework/publish-bot-overview) or use [Ngrok to interact with your local bot in the cloud](https://blogs.msdn.microsoft.com/jamiedalton/2016/07/29/ms-bot-framework-ngrok/).
   *  Register you bot in [Microsoft Bot Framework Portal](https://dev.botframework.com/bots). Please refer to [this](https://docs.microsoft.com/en-us/bot-framework/portal-register-bot) for the instructions. Once you complete the registration, update the [Bot's Web.config](Web.config#L10-L12) file with the registered config values (Bot Id, MicrosoftAppId and MicrosoftAppPassword). 
   *  Enable the Skype Channel and update the settings by enabling 1:1 audio cals and updating the Calling Webhook to be `https:://{your domain}/api/calling/call`. Refer to [this](https://docs.microsoft.com/en-us/bot-framework/portal-configure-channels) for more information on how to configure channels. 
   * Update the `Microsoft.Bot.Builder.Calling.CallbackUrl` setting of the [Bot's Web.config](Web.config#L15) file with the callback route `https://{yourdomain}/api/calling/callback`. 
   * Subscribe to the Microsoft Cognitive Services Bing Speech API [here](https://www.microsoft.com/cognitive-services/en-us/subscriptions) to get a key to use the API. Update the `MicrosoftSpeechApiKey` setting of the [Bot's Web.config](Web.config#L18) with the obtained key.
   * Change the Uri to the endpoint URL in GetEntityFromLUIS function to the URI obtained from the LUIS API.
