# Tweet from your Phone without the Twitter App

How to Tweet from your phone without having the Twitter App?

Or even tweet with clicking a SINGLE BUTTON?

The Twitter app is too distracting but I still wanted to tweet so I figured out a FREE and SIMPLE solution. 

Here are the steps:

1.  Go to https://developer.twitter.com and sign up for a free account.

2. Create a Free account and get your API keys (Bearer Token, consumer_key, access_token, token_secret, etc)

3. Download Shortcuts on your iPhone

4. Create a new shortcut and click on "Add Action"

5. Search for "Get Contents of URL" and in the URL section, copy this: "https://api.twitter.com/2/tweets"

6. Change these settings

- Method to POST
- Headers have two fields (Key and Text)
For Key: Authorization

For Text: 

OAuth oauth_consumer_key="YOUR_API_KEY", oauth_token="YOUR_ACCESS_TOKEN", oauth_signature_method="HMAC-SHA1", oauth_timestamp="TIMESTAMP", oauth_nonce="NONCE", oauth_version="1.0", oauth_signature="SIGNATURE"

How do you get the timestamp, the nonce, and the signature?

It's messy so I'll give you a hack so all you will need to do is copy the entire thing.


Let's use a tool called Postman. It's easy so here are the steps.

🏃‍♂️Go here (https://t.co/twitter-api-postman)
🏃‍♂️Click on "Fork"
🏃‍♂️Click on the "Twitter API v2" folder, find the "Manage Tweets" folder, and click on "Create Tweets"
🏃‍♂️Click on Authorization and copy your API keys

And lastly

🏃‍♂️Click the blue button "Send" and verify it works.

📳 Go to your Twitter account and you will see it has automatically tweeted for you. 

Now, Let's go back to STEP 6

6.1 Go to Postman and click on "Headers"

- Copy the Authorization Value that starts with Oauth
- Copy the entire thing and paste it on the Shortcuts app next to the Authorization Value as the text

7. Request Body

- Add "new field" and click on Text
- For Key: text
- For Text: your tweet

DONE. 

**NOW YOU ARE ABLE TO TWEET WITHOUT THE TWITTER APP!!!!**

8. How can you make it easier to use?

- Find the "Ask for Input" and place it on top/before the "Get Contents of" block. Select to ask for "Text" with "whatever title you want"

- In the Request Body, click on Text value, and "Provided Input" will show up. 

And now, we're done.


## Future Improvements?

Want to contribute?

Images/Videos and Threads!!!

For Threads, here are some initial thoughts:

1. We get the ID of the tweet you want to reply to. 
2. Use the "in_reply_to_status_id" parameter.


## Inspiration
I used to use IFTTT but after Twitter's API changes, my applet was canceled so I decided to make my own version using the TWITTER API!!!

## Contact
For more cool projects and interesting essays: https://juandavidcampolargo.com/newsletter
