# Quotes-Discord-Bot

This bot manages a "quotes" system for discord servers. Users can put quotes into a channel, the bot records the quotes, and then users can recall a random quote with "+randomquote". Also has a few more smaller features.

To use the bot you need to have Python 3 installed along with a MongoDB database. By default, the database needs to be named discordbot with two collections, quotes and servers. The earliest python version I tested it with was 3.8.5, however discord.py should work with 3.5 and later but I cannot guarantee anything. First run `pip3 install -r requirements.txt` to get the required libraries. Next, paste your bot key from the Discord dev portal into bot_token.py and fill in your MongoDB connection link in main.py. Finally, run `python3 main.py` to start the bot.

My hosted implementation of this bot (up 24/7): [Add to your server](https://top.gg/bot/799028695368073255)

## Commands:

### +mostquoted 
Outputs the person with the most quotes attributed to them
### +randomquote (optionally @user)
Outputs a random quote from the user-specified quotes channel. Optionally, mention a user to get a random quote attributed to them.
### +numquotes @user
Outputs the number of quotes that the person mentioned has attributed to them.
### +setquoteschannel
Type this in the channel you wish to be your servers quotes channel. In order to run this command, you must have the role "QuotesBot Admin"
### +delquoteschannel 
Type this in the channel your quotes channel if you wish for it to no longer be a quotes channel. In order to run this command, you must have the role "QuotesBot Admin"
### +togglementions
Toggles whether a the author of the quote is mentioned or not when randomquote and numquotes are run. On by default, but turn off to avoid excessive mentions in large servers. In order to run this command, you must have the role "QuotesBot Admin"
### All quotes in your designated quotes channel must be formated as "quote here" @author. Otherwise, they will be rejected by the bot and deleted from the channel.
