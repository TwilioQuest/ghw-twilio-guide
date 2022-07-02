# Getting started with Twilio at MLH Init

Hello hackers! Learn how to use REST APIs with Twilio during INIT by following the steps in this repository. You can submit the challenges each day at [https://init.mlh.io](https://init.mlh.io). In this README, you will find instructions to follow for each day.

## Contents

## Getting Help

If you have questions about Twilio or the MLH Init challenges, visit the `#twilio` channel in the [MLH Discord](https://discord.mlh.io/).

# Weekly challenge

## Summary

Twilio's weekly challenge is to play and learn with [TwilioQuest](https://twilio.com/quest). To complete the weekly challenge, simply download TwilioQuest, join the leaderboard, and play at least one mission. If you want to be in with a chance of winning a special TwilioQuest prize pack, rank top 5 in the leaderboard. Read on to learn more!

## What is TwilioQuest?

TwilioQuest is a free game that helps you learn to code. With TwilioQuest, you can learn Node.js, Python, Open source with Git & GitHub, REST APIs, and Twilio. In TwilioQuest, you learn by completing objectives, which are short tutorials with challenges. Each challenge earns you XP and items for your character.

You can download TwilioQuest for Windows, Linux, MacOS, and Raspberry Pi [here](https://twilio.com/quest/download).

## Completing the weekly challenge

Once you have downloaded TwilioQuest, here are the steps you need to complete to submit the weekly challenge:

- Launch TwilioQuest.
  - If this is your first time playing TwilioQuest, you will see an intro cinematic, create a character, and complete the tutorial prologue.
- Join the TwilioQuest operation.
  - Open settings by clicking on the icon of 3 sliders at the top of the screen.
  - On the left, select "Operations".
  - In the join code box, enter the code ` birds-popular-indeed`, and click "Join Operation".
  - Your character and XP will now be visible in the [leaderboard](https://www.twilio.com/quest/app/operations/Q1VJoMy3sCQCjADG1MrA).
- Complete a mission, from any of the following:
  - The Javascript Test Lab
  - The Pythonic Temple
  - The API Academy
  - The Forest of Open Source
  - Programmable Voice or Programmable SMS
    - You will have to complete API Setup to do either of these missions.
  - The Ducktypium Forge

## Winning a TwilioQuest Prize Pack

The top 5 players by XP on the leaderboard at the end of INIT will win a special TwilioQuest prize pack. Earn XP by completing more missions!

# Daily challenges

## What is an API? What is a REST API?

An Application Programming Interface (API) is provided by a service owner so that others may use the features and functions enabled by the service. APIs describe how a consumer will make requests of the servuce, and what they will receive in return. [Read more](https://www.twilio.com/docs/glossary/what-is-an-api).

A REST API allows software programs to expose functionality and data to other programs over the Internet in a consistent format. Generally speaking, when people use the term REST API, they are referring to an API that is accessed via the HTTP protocol at a predefined set of URLs (uniform resource locators) representing the various resources with which interactions can occur. [Read more](https://www.twilio.com/docs/glossary/what-is-a-rest-api).

Twilio is an example of a REST API. Twilio's communication APIs let you do things like send text messages and emails, make phone calls, and stream video. You can see all of the things you can do with Twilio on the [Twilio docs](https://www.twilio.com/docs).

During MLH INIT, you will learn how to **send and receive text messages** and **make and receive phone calls** with Twilio.

## Day 1: Get ready to hack with Twilio.

To complete the week's challenges, there's some setup we need to do first. Today you will:

- Create and upgrade your Twilio account with some free credit.
- Use your free credit to buy two Twilio numbers.
- Set up the Twilio Dev Phone to help test your Twilio number.
- Install `curl` to make requests to the Twilio API from the command line.

### Step 1: Create an account

If you don't already have a Twilio account, create one by visiting [this link](https://www.twilio.com/try-twilio?promo=mlh-twilio).

### Step 2: Upgrading your account

When you create an account with the above link, you will create a trial account. To complete the Twilio challenges during INIT, you will need to use 2 Twilio numbers, which requires an upgraded account. To upgrade your account:

- Visit the #twilio channel in the MLH Discord.
- Check the pinned messages for the channel.
- Find the promo code shared in the pinned message.
- Follow [this guide](https://www.twilio.com/blog/apply-promo-code) to apply the promo code to your account.

When you use this code, you will also get some free credit. If you did not create a new account, and are using an account you created in the past, you can still use this code to get extra credit to complete the INIT daily challenge.

### Step 3: Buy Two Twilio numbers

With your free credit, you can now buy your first Twilio numbers! With a Twilio number, you can send and receive calls and SMS.

We will buy two numbers:

- One number to use in our application.
- One number to test the other number, using the Dev Phone.

To buy a number, follow [this guide](https://support.twilio.com/hc/en-us/articles/223135247-How-to-Search-for-and-Buy-a-Twilio-Phone-Number-from-Console).

Buy a number with both SMS and Voice capabilities, so you can send/receive messages and phone calls. Phone numbers may not be available in your country, or may require extra identity documentation for your country. If this is the case, you can buy US numbers. This won't cost you any extra during testing, as we'll be using the Dev Phone to call/message the number, and not your local mobile number.

### Step 4: Installing the Twilio CLI

The Twilio CLI makes it easy to use Twilio from our command line interface. We will need the Twilio CLI to use the Dev Phone, which makes it easy (and free) to test our Twilio services from anywhere in the world.

To install the CLI, follow [this guide](https://www.twilio.com/docs/twilio-cli/quickstart).

### Step 5: Installing the Dev Phone

The Dev Phone lets us test our Twilio applications using a Twilio number, rather than your own mobile number. This means you can test your applications using only your Twilio credit, from anywhere in the world.

To install the Dev Phone, follow [this guide](https://www.twilio.com/docs/labs/dev-phone).

## Step 6: Installing `curl`

The last step today is to install `curl`. `curl` is a command line tool for getting data from URLs, and we'll use it to interact with the Twilio REST API.

You can learn more about `curl` [here](https://curl.se/).

To install `curl`, follow [this guide](https://everything.curl.dev/get).

## Step 7: Daily challenge complete! Time to submit.

You've completed the challenge for the day, high five! To submit the challenge, type `curl --version` into your terminal, and submit a screenshot.

## Day 2: Receive your first phone call using TwiML bins and Dev Phone.

[TwiML](https://www.twilio.com/docs/glossary/what-is-twilio-markup-language-twiml) (Twilio Markup Language) is a special markup language which you can use to program actions in Twilio.

Today you will:

- Create a TwiML bin to handle a phone call.
- Assign it to your Twilio number.
- Make a call using Dev Phone.

## Step 1: Create a TwiML bin to handle a phone call

A TwiML bin is a container for TwiML. We can fill the bin with TwiML to program Twilio to do certain actions, and then connect the bin to our phone number. Follow the instructions [here](https://www.twilio.com/docs/runtime/tutorials/twiml-bins#create-a-new-twiml-bin) to create a new TwiML bin to respond to a phone call with "hello world".

## Step 2: Link your TwiML bin to your Twilio number

Now that we have some TwiML to say "hello world", we need to connect it to our phone number. Choose one of the two numbers you purchased in day 1, and follow [this guide](https://www.twilio.com/docs/runtime/tutorials/twiml-bins#wire-your-twiml-bin-up-to-an-incoming-phone-call) to do that.

Remember which number you chose! In the next step, we will use the other number.

## Step 3: Test it using Dev Phone

Open your terminal and start the Dev Phone with `twilio dev-phone`.

After starting up, the terminal will tell you the address of the Dev Phone interface, usually `https://localhost:3001`. Go here in your browser to use the Dev Phone.

From here, you can select a phone number. Choose the number that you didn't use in the previous step. The Dev Phone will then show you a dialler to call a number. Enter your other phone number, the one with the TwiML bin, and hit call. You should hear "Hello World" spoken back to you.

## Step 4: Daily challenge complete! Time to submit.

You've completed day 2, high five! To submit, take a screenshot of your Dev Phone call history.

## Day 3: Make your first outbound phone call using `curl`.

Today you will:

- Create a TwiML bin that contains a script for a phone call.
- Learn how to use `curl` to make HTTP requests.
- Make a call from your Twilio number to your Dev Phone.

## Day 4: Setting up a web application with ngrok and webhooks.

Today you will:

- Set up a basic Node.js or Python web application.
- Download ngrok to make the application accessible from the web.
- Set up a Twilio webhook to the application.

## Day 5: Receiving SMS messages with our web application.

Today you will:

- Add an endpoint to your web application to handle Twilio webhooks.
- Handle a webhook containing an SMS message.
- Send your first SMS from the Dev Phone.

## Day 6: Replying to SMS messages with our web application.

Today you will:

- Write TwiML to respond to a text message.
- Return that TwiML in response to a webhook.
- Receive your reply on the Dev Phone.

## Day 7: Join Twilio Field Operators to keep learning!

Thanks for hacking with Twilio during INIT! Keep learning with Twilio Field Operators.

# Frequently Asked Questions

## I have an existing account with Twilio credit, what do I do?

## I have completed TwilioQuest in the past, can I do the weekly challenge?

## I have completed TwilioQuest in the past, can I still win a prize on the leaderboard?

## My Twilio account was suspended
