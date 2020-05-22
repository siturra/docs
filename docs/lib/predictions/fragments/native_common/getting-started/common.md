The Predictions category for enables you to integrate machine learning in your application without any prior machine learning experience.  We support a number of use cases which include, but not limited to: translating text from one language to another, converting text to speech, text recognition from an image, entities recognition, labeling real world objects, interpretation of text, uploading images for automatic training, and (currently, iOS only) transcribing text.  These use cases are powered by Amazon services including: [Amazon Translate](https://docs.aws.amazon.com/translate/latest/dg/what-is.html), [Amazon Polly](https://docs.aws.amazon.com/polly/latest/dg/what-is.html), [Amazon Transcribe](https://docs.aws.amazon.com/transcribe/latest/dg/what-is-transcribe.html), [Amazon Rekognition](https://docs.aws.amazon.com/rekognition/latest/dg/what-is.html), [Amazon Textract](https://docs.aws.amazon.com/textract/latest/dg/what-is.html), and [Amazon Comprehend](https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html).

<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/10_coreml.md"></inline-fragment>

## Goal
To setup and configure your application with Amplify Predictions and go through a simple example of translating text.

## Prerequisites
<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/20_preReq.md"></inline-fragment>
<inline-fragment platform="android" src="~/lib/predictions/fragments/android/getting-started/20_preReq.md"></inline-fragment>

## Provision Backend Services
To use the predictions category we will need to setup the auth backend resources.  To provision auth resources in the backend, go to your project directory and **execute the command**:
```bash
amplify add auth
```

Enter the following when prompted:
```console
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Email`
? Do you want to configure advanced settings?
    `No, I am done.`
```

Now, to provision predictions resources, go to your project directory and **execute the command**
```bash
amplify add predictions
```

Enter the following when prompted:
```console
? Please select from one of the categories below
    `Convert`
? What would you like to convert?
    `Translate text into a different language`
? Provide a friendly name for your resource
    `transTextSample`
? What is the source language?
    `English`
? What is the target language?
    `Italian`
? Who should have access?
    ` Auth and Guest users`
```
Note that the languages selected during this stage will be the default language your app will translate to/from.  These source and target languages can be overridden when we write the code in our application.

To push your change to the cloud, `execute the command:`
```bash
amplify push
```

Upon completion, `awsconfiguration.json` and `amplifyconfiguration.json` should be updated to reference provisioned backend storage resources.  Note that these files should already be a part of your project if you followed the [Project setup walkthrough](~/lib/project-setup/create-application.md).

## Install Amplify Libraries
<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/30_installLib.md"></inline-fragment>
<inline-fragment platform="android" src="~/lib/predictions/fragments/android/getting-started/30_installLib.md"></inline-fragment>

## Initialize Amplify Predictions
<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/40_init.md"></inline-fragment>
<inline-fragment platform="android" src="~/lib/predictions/fragments/android/getting-started/40_init.md"></inline-fragment>

## Translating Text
To translate text from one language to another, specify the text you want translated, a source language, and a target langauge.  The source and target language parameters will override any choice you made while adding this resource using the Amplify CLI.

<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/50_translate.md"></inline-fragment>
<inline-fragment platform="android" src="~/lib/predictions/fragments/android/getting-started/50_translate.md"></inline-fragment>

As a result of executing this code, you should see the following printed to your console:

```console
Me gusta comer espaguetis
```

## Next Steps
Congratulations! You've translated text from one language to another.  Check out the following links to explore other Amplify Predictions use cases:

<inline-fragment platform="ios" src="~/lib/predictions/fragments/ios/getting-started/60_nextSteps.md"></inline-fragment>
<inline-fragment platform="android" src="~/lib/predictions/fragments/android/getting-started/60_nextSteps.md"></inline-fragment>
