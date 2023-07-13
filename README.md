### Alexa Youtube Music Skill

Alexa does not provide native integration to neither youtube nor youtube music. This skill helps to play music from
youtube music on your amazon echo device

NOTE: The skill will not be published for public use as it can incur charges due to AWS Lambda usage.  Users who
are looking to install this skill on their echo device should have AWS developer account and then use the skill

Anyone is free to publish the skill in their AWS account so that non-tech savvy users can also make use of it. If there
is some skill that is available please raise a PR so that, the link to the skill can be added here

#### Setting up the skill
1. You need to have last version of NodeJS and ```npm``` installed from [https://nodejs.org/en/download/](https://nodejs.org/en/download/)

2. You need an [AWS account](https://aws.amazon.com) and an [Amazon developer account](https://developer.amazon.com) to create an Alexa Skill.

3. You need to install and configure the [AWS CLI]([https://aws.amazon.com/cli/](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

4. You need to install and to initialize [ASK CLI](https://developer.amazon.com/docs/smapi/quick-start-alexa-skills-kit-command-line-interface.html) with

5. Generate a [Google Cloud API](https://console.cloud.google.com/apis/credentials) with `YouTube Data API v3` restriction, and add a it to the lambda function as an environment variable with the name `YOUTUBE_API_KEY`

### Deployment

ASK will create the skill and the lambda function for you.

Lambda function will be created in ```eu-west-1```.

You deploy the skill and the lambda function in one step :

```bash
$ ask deploy
```

## Cleanup

If you were deploying this skill just for learning purposes or for testing, do not forget to clean your AWS account to avoid recurring charges for your DynamoDB table.

- delete the lambda function (ask-custom-Multi_Stream_Audio_Player-default)
- delete the IAM execution role (ask-lambda-Multi-Stream-Audio-Player)
- delete the DynamoDB table (LongFormAudioSample)
