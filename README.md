# y8-construct3-sdk

Construct3 (C3) Y8 Plugin
Test Link: https://storage-direct.y8.com/Gani/html5/c3example/

**Getting Started**

- open your game/new construct3
- Right click in a Scripts folder and click Add Script
- Copy the contents of c3Example_y8/main.js and paste them into your project's main.js file.
  - Note: Update your App ID in the line let _appId = 'YOUR_APP_ID';
  - You can create or find your App ID by registering a new application here: https://account.y8.com/applications/
- Copy the y8API event sheet from c3Example_y8 and paste it into your project.
- The Y8 SDK functions should now be available from your event sheets.

**Example**

We provide the c3Example_y8.c3p file to show the basics of how to use the plugin. Give it a glace, it's easier to understand compared to text only instructions.

**Important Notes**

Purpose of the main.js in properties should be select to "Import for events". Without choosing purpose results as not working y8 SDK.

**Ads**

Y8 offers two types of revenue share models:

- AFP (AdSense for Platforms) — You get paid directly by Google through your own AdSense account.

- Manual Revenue Share — You send Y8 invoices, and the payment is handled manually.

To apply for AFP, first create a Studio:

Visit https://www.y8.com/studios

Once your studio is approved, you’ll be able to apply for AFP directly from your studio page.

you can get the game Id from our team, once your game gets approved from us.
In main.js please replace the game id into let _gameId; (Note: The test example uses let _gameId = '249093'; — replace it with your assigned Game ID before going live.)

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
