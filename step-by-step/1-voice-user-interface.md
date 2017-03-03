# Build An Alexa Quiz Game Skill
<a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/1-voice-user-interface.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/1-on._TTH_.png" /></a><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/spacer._TTH_.png" /><a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/2-lambda-function.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/2-off._TTH_.png" /></a><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/spacer._TTH_.png" /><a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/3-connect-vui-to-code.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/3-off._TTH_.png" /></a><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/spacer._TTH_.png" /><a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/4-testing.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/4-off._TTH_.png" /></a><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/spacer._TTH_.png" /><a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/5-customization.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/5-off._TTH_.png" /></a><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/spacer._TTH_.png" /><a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/6-publication.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/navigation/6-off._TTH_.png" /></a>

## Setting up Your Alexa Skill in the Developer Portal

<!--<a href="https://www.youtube.com/watch?v=cpXn8AM1JO8" target="_new"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/youtube._TTH_.png" style="align:right;" /></a>-->

There are two parts to an Alexa skill.  The first part is the [Voice User Interface (VUI)](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/defining-the-voice-interface).  This is where we define how we will handle a user's voice input, and which code should be executed when specific commands are uttered.  The second part is the actual code logic for our skill, and we will handle that on [page #2](https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/2-lambda-function.md) of this step-by-step guide.

1.  **Go to the [Amazon Developer Portal](http://developer.amazon.com).  In the top-right corner of the screen, click the "Sign In" button.** </br>(If you don't already have an account, you will be able to create a new one for free.)

    <a href="http://developer.amazon.com" target="_new"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-1-developer-portal._TTH_.png" /></a>

2.  **Once you have signed in, click the Alexa button at the top of the screen.**

    <a href="https://developer.amazon.com/edw/home.html#/" target="_new"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-2-alexa-button._TTH_.png" /></a>

3.  **On the Alexa page, choose the "Get Started" button for the Alexa Skills Kit.**

    <a href="https://developer.amazon.com/edw/home.html#/skills/list" target="_new"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-3-alexa-skills-kit._TTH_.png" /></a>

4.  **Select "Add A New Skill."** This will get you to the first page of your new Alexa skill.

    <a href="https://developer.amazon.com/edw/home.html#/skill/create/" target="_new"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-4-add-a-new-skill._TTH_.png" /></a>

5.  **Fill out the Skill Information screen.**  Make sure to review the tips we provide below the screenshot.

    <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-5-skill-information._TTH_.png" />
    
    ### Skill Information Tips
    1.  **Skill Type** For this skill, we are creating a skill using the Custom Interaction Model.  This is the default choice.

    2.  **Language** Choose the first language you want to support.  You can add additional languages in the future, but we need to start with one.  (This guide is using U.S. English to start.)

    3.  **Name** This is the name that will be shown in the Alexa Skills Store, and the name your users will refer to.

    4.  **Invocation Name** This is the name that your users will need to say to start your skill.  We have provided some common issues developers encounter in the list below, but you should also review the entire [Invocation Name Requirements](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/choosing-the-invocation-name-for-an-alexa-skill).

        | Invocation Name Requirements | Examples of incorrect invocation names |
        | ---------------------------- | -------------------------------------- |
        | The skill invocation name must not infringe upon the intellectual property rights of an entity or person. | korean air; septa check |
        | Invocation names should be more than one word (unless it is a brand or intellectual property), and must not be a name or place | horoscope; trivia; guide; new york |
        | Two word invocation names are not allowed when one of the words is a definite article, indefinite article, or a preposition | any poet; the bookie; the fool |
        | The invocation name must not contain any of the Alexa skill launch phrases and connecting words.  Launch phrase examples include "launch," "ask," "tell," "load," and "begin."  Connecting word examples include "to," "from," "by," "if," "and," "whether." | trivia game for star wars; better with bacon |
        | The invocation name must not contain the wake words "Alexa," "Amazon," "Echo," or the words "skill" or "app." | hackster initial skill; word skills |
        | The invocation name must be written in each language you choose to support.  For example, the German version of your skill must have an invocation name written in German, while the English (US) version must have an invocation name written in English. | kitchen stories (German skill) |
    
    5.  **Audio Player** For this Quiz Game skill, we won't be using any audio files, so you can select No for this option.  If you would like to learn more about adding audio to your skills, please check out our [Audio Player Guide](https://github.com/alexa/skill-sample-nodejs-audio-player).

6.  **Click the Next button to move to the Interaction Model.**

    <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-6-next-button._TTH_.png" />

7.  **Fill out the Interaction Model screen.**  Below the screenshot, we have provided links to the content you need to include in each box.

    <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-7-interaction-model._TTH_.png" />

    ### Interaction Model Tips
    1.  **Intent Schema** An intent schema defines the actions that we want our users to be able to take.  We will dive into modifying this schema later in this guide, so for now, just copy and paste this code into the Intent Schema box. ([Read more about Defining the Voice Interface](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/defining-the-voice-interface))

        ```JAVASCRIPT
        {"intents": [
            {"intent": "AnswerIntent", "slots":[{"name": "StateName", "type": "AMAZON.US_STATE"},
                                        {"name": "Capitol", "type": "AMAZON.US_CITY"}, 
                                        {"name": "StatehoodYear", "type": "AMAZON.FOUR_DIGIT_NUMBER"},
                                        {"name": "Abbreviation", "type": "US_STATE_ABBR"},
                                        {"name": "StatehoodOrder", "type": "AMAZON.NUMBER"}]},
            {"intent": "QuizIntent"},
            {"intent": "AMAZON.StopIntent"},
            {"intent": "AMAZON.CancelIntent"},
            {"intent": "AMAZON.StartOverIntent"},
            {"intent": "AMAZON.HelpIntent"}
            ]
        }
        ```
        ([get this code on GitHub](https://github.com/alexa/tutorial-quiz-game/blob/master/speechAssets/intentSchema.json))

        You should notice that there is an AnswerIntent, and it has five slots defined: StateName, Capitol, StatehoodYear, Abbreviation, and StatehoodOrder.  Thanks to many of the [Built-In Slots](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/built-in-intent-ref/slot-type-reference#list-types) that Amazon provides us, we can easily set the "type" of four of our slots to those built-in values with AMAZON.US_STATE, AMAZON.US_CITY, AMAZON.FOUR_DIGIT_NUMBER, and AMAZON.NUMBER.  For the last value, we need to define a custom slot type.

    2.  **Custom Slot Types** Custom slots are sets of training data for Alexa to give her an idea of the types of data you are expecting to receive from your users.  It is important to note that the values in a custom slot *do not* function like a drop-down list on a website.  If your custom slot contains a list of colors in the rainbow, and your user responds with a color that isn't in your list, you will still receive "sky blue" as an answer, and you need to be prepared for those situations.

        For this guide, you will need to create one custom slot type: [US_STATE_ABBR](https://github.com/alexa/tutorial-quiz-game/blob/master/speechAssets/US_STATE_ABBR_slotvalues.txt).  To create a custom slot type, click the "Add Slot Type" button.

        <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-7-2-add-slot-type._TTH_.png" />

        You will see two boxes: **Enter Type** and **Enter Values**.

        <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-7-2-adding-slot-type._TTH_.png" />

        To create your custom slot, follow these steps:

        1.  Use the exact same name for **Enter Type** that is listed in the intent schema: US_STATE_ABBR.

        2.  Copy the state abbreviations below to the **Enter Values** box.

            ```
            AK
            AL
            AZ
            AR
            CA
            CO
            CT
            DE
            FL
            GA
            HI
            ID
            IL
            IN
            IA
            KS
            KY
            LA
            ME
            MD
            MA
            MI
            MN
            MS
            MO
            MT
            NE
            NV
            NH
            NJ
            NM
            NY
            NC
            ND
            OH
            OK
            OR
            PA
            RI
            SC
            SD
            TN
            TX
            UT
            VT
            VA
            WA
            WV
            WI
            WY
            ```
            ([get this on GitHub](https://github.com/alexa/tutorial-quiz-game/blob/master/speechAssets/US_STATE_ABBR_slotvalues.txt))

        3.  Click the **Save** button when you are done with your new custom slot value.

            <img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/1-7-3-save-button._TTH_.png" /> 

    3.  **Sample Utterances** Sample utterances are a guide for Alexa to figure out how to map what a user says to your Intents that we defined earlier.  For now, you just need to copy these sample utterances into the Sample Utterances box in your browser.

        ```javascript
        AnswerIntent {StateName}
        AnswerIntent {Capitol}
        AnswerIntent {StatehoodYear}
        AnswerIntent {StatehoodOrder}
        AnswerIntent {Abbreviation}

        QuizIntent start a quiz
        QuizIntent and start a quiz
        QuizIntent and quiz me
        ```
        ([get this on GitHub](https://github.com/alexa/tutorial-quiz-game/blob/master/speechAssets/intentSchema.json))

        Once you have added these sample utterances to your skill, you can click the "Save" button to verify that your interaction model is built properly without any errors.

8.  If your interaction model builds successfully, you can click next to move on to Configuration.  In our next step of this guide, we will be creating our Lambda function, but keep this browser tab open, because we will be returning here in [Step #3: Connect VUI to Code](https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/3-connect-vui-to-code.md).

    If you get an error from your interaction model, check through this list:

    *  **Is your custom slot named "US_STATE_ABBR?"**
    *  **Did you copy & paste the provided code into the appropriate boxes?**
    *  **Did you accidentally add any characters to the Interaction Model or Sample Utterances?**

<br/><br/>
<a href="https://github.com/alexa/skill-sample-nodejs-quiz-game/blob/master/step-by-step/2-lambda-function.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/buttons/button_next_lambda_function._TTH_.png" /></a>