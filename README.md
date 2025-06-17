# y8-construct3-sdk

Construct3 (C3) Y8 Plugin
Test Link: https://storage-direct.y8.com/Gani/html5/c3example/

**Getting Started**

- open your game/new construct3
- Right click in a Script folder and click add script
- Copy the c3Example_y8 main.js and paste into your main.js of the game.
  - Note: in main.js line number 33 please replace your app Id, 
  - You can create and find your App ID by registering a new application here: https://account.y8.com/applications/
- Then copy the y8API sheet from c3Example_y8 and paste into your game.
- Now Y8 functions should be available in the event tabs

**Example**

We provide the c3Example_y8.c3p file to show the basics of how to use the plugin. Give it a glace, it's easier to understand compared to text only instructions.

**Important Notes**

Purpose of the main.js in properties should be select to "Import for events". Without choosing purpose results as not working y8 SDK.

**Ads**

If you are an **AFP partner**, replace the AdSense ID in the main.js
- var AdsenseId = "YOUR_ADSENSE_ID";
- set activateAFP to true (var activateAFP = true;)

If you are **not an AFP partner**, replace the Channel ID
- var ChannelId = "YOUR_CHANNEL_ID";
- Set activateAFP to false (var activateAFP = false;) Contact us if you want to become an AFP partner or if you need a Channel ID.

**Available Functions**

- function Login() - Show a dialog prompting the user to login with an account
- function submitScore() - Submit a high score
- function showLeaderboard() - Show high score menu
- function showAchievment() - Show Achievments menu
- function unlockAchievment() - Unlock Achievments
- function saveData() - Save a progress 
- function loadData() - Load a progress
- function showAds() - Show Ads
- function showRewardAds() - Show Rewarded Ads
- function rewardAdDismissed() - Skip ad, no reward, watch next time
- function RewardAdGained() - Reward earned, action completed.
- function No Reward Ads() - No ads available, try again later.
- function openProfile() - open the players profile
- function sendScreenshot() - Submit a screenshot of the game

**Important Variables**

- gameName - Game Name
- SponsoredSite -  if SponsoredSite = 1 then y8 Logo's are not clickable
- blacklistSite - if blacklistSite = 1 then show blacklist layout 
- userNameY8 - You can call userNameY8 variable to show Player's username.

**Need More Help**

There is a awesome community of devs and players on the id.net forum. Leave a message, we will try to reply.
