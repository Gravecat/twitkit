# TwitKit

These are some Python tools I've written for interacting with the Twitter website. You will need to provide your own API key and access token to make full use of the scripts here. If you do not already have an API key, you'll have to sign up for [a developer account](https://developer.twitter.com/en/docs/twitter-api/getting-started/getting-access-to-the-twitter-api). Alternatively, you can use some of the scripts below by providing your own following/followers lists in a text file.

`tweets_only.py` -- Given either a command-line argument of one (or more) usernames, or individual usernames typed one at a time in the console if no command-line argument is given, will open a web browser to a search page showing only that user's tweets, and not their retweets.

`twitkit_common.py` -- Shared code used by the other script files. Does nothing on its own.

`twitter_check_followers.py` -- Retrieves a list of people following you on Twitter, and stores it in a text file. Subsequent runs of this script will compare your current followers to the last time you checked, and inform you of any new followers/unfollowers. *(API keys required.)*

`twitter_compare_followers.py` -- Takes the text-file output from **twitter_check_followers.py** and **twitter_update_following.py** and compares followers, listing which accounts are not following you back, and which ones you are not following back.

`twitter_random.py` -- Picks a random user from a text file (either generated by twitter_update_followers.py, or you can provide your own) and opens their Twitter page in the default web browser.

`twitter_update_following.py` -- Usng the Twitter APIs, retrieves a list of the people you are currently following and stores them in a text file. *(API keys required.)*
