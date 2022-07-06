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

### Step 6: Installing `curl`

The last step today is to install `curl`. `curl` is a command line tool for getting data from URLs, and we'll use it to interact with the Twilio REST API.

You can learn more about `curl` [here](https://curl.se/).

To install `curl`, follow [this guide](https://everything.curl.dev/get).

`curl` comes pre-installed on Windows, and can be accessed through Powershell. Use `curl.exe` when giving commands, i.e. `curl.exe --version`.

### Step 7: Daily challenge complete! Time to submit.

You've completed the challenge for the day, high five! To submit the challenge, type `curl --version` into your terminal, and submit a screenshot [on the DevPost](https://ghw-init-day-1.devpost.com/)

## Day 2: Receive your first phone call using TwiML bins and Dev Phone.

[TwiML](https://www.twilio.com/docs/glossary/what-is-twilio-markup-language-twiml) (Twilio Markup Language) is a special markup language which you can use to program actions in Twilio.

Today you will:

- Create a TwiML bin to handle a phone call.
- Assign it to your Twilio number.
- Make a call using Dev Phone.

### Step 1: Create a TwiML bin to handle a phone call

A TwiML bin is a container for TwiML. We can fill the bin with TwiML to program Twilio to do certain actions, and then connect the bin to our phone number. Follow the instructions [here](https://www.twilio.com/docs/runtime/tutorials/twiml-bins#create-a-new-twiml-bin) to create a new TwiML bin to respond to a phone call with "hello world".

### Step 2: Link your TwiML bin to your Twilio number

Now that we have some TwiML to say "hello world", we need to connect it to our phone number. Choose one of the two numbers you purchased in day 1, and follow [this guide](https://www.twilio.com/docs/runtime/tutorials/twiml-bins#wire-your-twiml-bin-up-to-an-incoming-phone-call) to do that.

Remember which number you chose! In the next step, we will use the other number.

### Step 3: Test it using Dev Phone

Open your terminal and start the Dev Phone with `twilio dev-phone`.

After starting up, the terminal will tell you the address of the Dev Phone interface, usually `https://localhost:3001`. Go here in your browser to use the Dev Phone.

From here, you can select a phone number. Choose the number that you didn't use in the previous step. The Dev Phone will then show you a dialler to call a number. Enter your other phone number, the one with the TwiML bin, and hit call. You should hear "Hello World" spoken back to you.

### Step 4: Daily challenge complete! Time to submit.

You've completed day 2, high five! To submit, take a screenshot of your Dev Phone call history and submit to [DevPost](https://hackp.ac/dailydevpost).

## Day 3: Make your first outbound phone call using `curl`.

Yesterday, we set up our Twilio number to RECEIVE phone calls. Today we will make an outbound phone call, from our Twilio number.

Today you will:

- Learn how to use `curl` to make HTTP requests.
- Build a `curl` request that will make a phone call using the Twilio API.
- Make a call from your Twilio number to your Dev Phone.

### Step 1: Check out the Twilio documentation on making calls

The [Twilio documentation for making calls](https://www.twilio.com/docs/voice/make-calls) offers examples in several languages and tools. This is useful if you are using the Twilio API from your favourite programming language, but it also has examples in `curl`, making it easy for us to test each endpoint from the command line.

In the code editor on the right of the page, select `curl` to bring up the example. It will look like this:

```
curl -X POST https://api.twilio.com/2010-04-01/Accounts/$TWILIO_ACCOUNT_SID/Calls.json \
--data-urlencode "Url=http://demo.twilio.com/docs/voice.xml" \
--data-urlencode "To=+14155551212" \
--data-urlencode "From=+15017122661" \
-u $TWILIO_ACCOUNT_SID:$TWILIO_AUTH_TOKEN
```

Let's break this down.

### Step 2: Understanding the `curl` command

Let's go through the example command bit by bit.

- `curl`: we're using the command curl! That bit is easy.
- `-X POST`: `-X` specifies the method for the request to the URL. By default, `curl` makes a `GET` request, to simply fetch the contents of the URL. Here we are making a `POST` request, as we want to send some data to the Twilio API with our request.
- `https://api.twilio.com/2010-04-01/Accounts/$TWILIO_ACCOUNT_SID/Calls.json`: this is the URL we are sending the request to, it is an endpoint on the Twilio API for making calls.
  - `$TWILIO_ACCOUNT_SID`: This is not actually part of the URL, we can tell from the leading `$` that this is a variable that our command line will substitute when it makes the request. We will have to set this variable before we make the request, we'll deal with that in the next step!
- `--data-urlencode`: This lets us encode data for `curl` to send in the `POST` body. We are sending 3 pieces of data to the API with our POST request:
  - `Url`: This is the URL of the TwiML that we want to use in the call. We can use a TwiML bin URL for this!
  - `To`: This is the number we want to call, we'll set this to the number of our Dev Phone.
  - `From`: This is the number we want to use to make the call. This will be our other Twilio number.
- `-u $TWILIO_ACCOUNT_SID:$TWILIO_AUTH_TOKEN`: It's those variables again! `-u` sets the authentication method. This is where we tell the Twilio API to make the request from our account. There are two variables here:
  - `TWILIO_ACCOUNT_SID`: This is the unique identifier for our account, kind of like a username.
  - `TWILIO_AUTH_TOKEN`: The auth token is kind of like the password for our account when we make an API request. You want to keep this secret!

Phew! That was a lot. Some of that might be confusing. Don't forget that you can ask questions, or ask for help, in the `#twilio` channel in the MLH Discord.

### Step 3: Building our `curl` request

We can use this example from the docs almost as is, there is just a couple of things we need to do:

1. Set our `TWILIO_ACCOUNT_SID` and `TWILIO_AUTH_TOKEN` variables.
2. Replace the `To` and `From` numbers with our Twilio numbers.
3. Replace the `Url` with the URL of our TwiML bin.

It will be easier to edit the `curl` command if you copy it into a text editor.

**To set your environment variables:**

- Go to your [Twilio console](https://console.twilio.com), and check out account info. Copy the account SID and auth token.
- Follow [this guide](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html) to set those as environment variables in your shell, for MacOS, Linux, and Windows.

**To replace the numbers:**

- Set the `To` number to the Twilio phone number that you are using in the Dev Phone. NOT the number that we have used for the TwiML bin earlier in the week.
- Set the `From` number to be the Twilio phone number that you have used for the TwiML bins in previous days.

**To replace the URL:**

- In day 2, we set up a TwiML bin to say "hello world" when we called our phone number. We can reuse that TwiML bin for our outbound call, so that when we phone someone, it will say "hello world".
- In your [Twilio console](https://console.twilio.com), find the TwiML bin you created yesterday. At the top of the page, you will see a `url` field. Copy this URL.
- Set the `Url` in our `curl` request to the TwiML bin URL.

Once you've done those three things, our `curl` request is ready to go!

### Step 4: Make the request

Make sure your Twilio Dev Phone is running and open it in your browser. In a new terminal, paste the edited `curl` command, and press enter. Your Dev Phone should ring and you should hear "hello world".

### Step 5: Daily challenge complete! Time to submit.

Congratulations on completing the day 3 challenge! To submit, take a screenshot of your Dev Phone call log to show you received the call.

## Day 4: Setting up a web application with ngrok and webhooks.

So far, we have used Twilio via TwiML bins and `curl`. That makes it really easy to experiment with the API or to complete small tasks, like forwarding a number, but at some point you might want to use Twilio in a bigger application. Over the next three days, we'll learn to use Twilio from a Node.js or Python web application.

Today you will:

- Set up a basic Node.js or Python web application.
- Download ngrok to make the application accessible from the web.
- Set up a Twilio webhook to the application.

### Step 1: Create a Node.js or Python web application

Node.js `express` and Python `flask` are both great choices for web applications. Follow the guides below to create an application in whichever you prefer:

- [Node.js](https://www.twilio.com/docs/usage/tutorials/how-to-set-up-your-node-js-and-express-development-environment)
- [Python](https://www.twilio.com/docs/usage/tutorials/how-to-set-up-your-python-and-flask-development-environment)

### Step 2: Install ngrok

To use Twilio with our web application, Twilio will have to be able to send a HTTP request to the application.

When we create a web application on our own machine, it will use the `localhost` URL. This is a URL accessible only from the machine, usually for testing purposes, and so will be inaccessible to Twilio. We can expose our web applications to the internet, but it can be complicated, and insecure once we're done. `ngrok` is an easier way to expose our web applications to the internet, temporarily.

If you followed the guides in step 1, you may have seen instructions to install `ngrok` already. Continue following those instructions. `ngrok` has recently made some changes in a newer version, if you experience any problems, check out [this guide](https://www.twilio.com/blog/using-ngrok-2022).

### Step 3: Set your Twilio webhook

When you have installed and started `ngrok`, it will create a URL for your application. This is the URL that Twilio will be able to reach.

We will use this URL to set what is called a "webhook". This is a HTTP request that Twilio will send in response to an event. For the rest of the week, we are going to be adding the ability to receive and reply to SMS messages to our application, so the event we will want to set a webhook for is when a new message is received.

Go to your [Twilio console](https://console.twilio.com), and go to the settings for your Twilio number, in "Phone Numbers" -> "Manage" -> "Active numbers". Find the "Messaging" section, and look for the dropdown that says "When a message comes in". Select "Webhook", and insert your URL in the box. Save your settings.

With your web application and ngrok running, if you now send a message to your Twilio number, you will see a request come from Twilio to your web app. This won't do anything yet, as we haven't written the code to handle the request. That's a job for tomorrow!

### Step 4: Daily challenge complete! Time to submit.

Congratulations on completing day 4, high five! To submit, take a screenshot of your `ngrok` or application terminal showing the receipt of a request from Twilio.

## Day 5: Receiving SMS messages with our web application.

The web application we created yesterday does not currently handle the webhook from Twilio. Today we will add a new endpoint to handle the webhook, and receive SMS messages.

Today you will:

- Add an endpoint to your web application to handle Twilio webhooks.
- Handle a webhook containing an SMS message.
- Send your first SMS from the Dev Phone.

### Step 1: Add a new endpoint

The Twilio webhook will be a `POST` request, so we will need to add a handler for `POST` requests. The below tutorials contain code samples you can use for Node.js and Python:

- [Node.js](https://www.twilio.com/blog/2017/10/how-to-receive-and-respond-to-a-text-message-with-node-js-express-and-twilio.html)
- [Python](https://www.twilio.com/blog/2016/09/how-to-receive-and-respond-to-a-text-message-with-python-flask-and-twilio.html)

In Node.js, the endpoint starts with:

```
app.post('/sms', (req, res) => {
```

In Python, it starts with:

```
@app.route('/sms', methods=['POST'])
```

Note the `/sms` in both versions. You will need to add `/sms` to the end of the URL in your webhook configuration for your phone number.

### Step 2: Getting the message contents

Once you have added the `/sms` POST endpoint to your application, you will be able to receive POST requests. A POST request has a body that contains the information sent with the request. The request we are receiving is from Twilio, telling us about a message we have received. The body will contain information about that message.

Let's get the sender and the message contents out of the request. Add the following to your `/sms` endpoint:

**Node.js**

```
let number = req.body.From;
let messageBody = req.body.Body;

console.log(`Message from ${number}, containing ${messageBody}`);
```

**Python**

```

number = request.form['From']
message_body = request.form['Body']

print('Message from {}, with contents: {}'.format(number, message_body))

```

These snippets get the information we're interested in our of the request object, and then print them to the terminal.

### Step 3: Send an SMS from the Dev Phone

Make sure your web application is running without errors, that ngrok is started, and that your phone number in Twilio has the full ngrok URL ending with `/sms`. Then enter your Twilio number in Dev Phone, and send a message!

In the terminal with the running web application, you should see output containing the sender number and the message body.

### Step 4: Daily challenge complete, time to submit!

Congratulations on completing day 5! To submit the challenge, take a screenshot of your terminal showing the output of receiving a message.

## Day 6: Replying to SMS messages with our web application.

Yesterday we pulled information out of a message we received. Today we will reply to the message! If you followed the linked tutorials yesterday, you may have already done this. If not, it will be a quick addition.

Today you will:

- Write TwiML to respond to a text message.
- Return that TwiML in response to a webhook.
- Receive your reply on the Dev Phone.

### Step 1: Writing a response

**Node.js:**

```

// Start our TwiML response.
const twiml = new MessagingResponse();

// Add a text message.
const msg = twiml.message(`Hello ${name}, you sent ${messageBody}`);

res.writeHead(200, {'Content-Type': 'text/xml'});
res.end(twiml.toString());

```

**Python:**

```

resp = twiml.Response()
resp.message('Hello {}, you said: {}'.format(number, message_body))
return str(resp)

```

## Day 7: Join Twilio Field Operators to keep learning!

Thanks for hacking with Twilio during INIT! Keep learning with Twilio Field Operators.

# Frequently Asked Questions

## I have an existing account with Twilio credit, what do I do?

If that account is a trial account, using the upgrade code will replace your trial credit with $25 of real credit. If you have trial credit you want to use, it's recommended you use this before using the upgrade code.

## I have completed TwilioQuest in the past, can I do the weekly challenge?

Please do not participate in the TwilioQuest leaderboard if you have completed TwilioQuest in the past. Twilio runs multiple challenges during GHW:INIT so that everyone can take part, even if they have previously completed a challenge.

## What is the maximum XP earnable in TwilioQuest? What is in the TwilioQuest Prize Pack? What happens if there's a draw?

We don't want to spoil the surprise :)

## My Twilio account was suspended

Please contact a Twilio team member in the Twilio channel in the GHW Discord.
