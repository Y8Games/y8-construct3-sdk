# y8-construct3-sdk

Construct3 (C3) Y8 Plugin
Test Link: https://storage-direct.y8.com/Gani/html5/c3example/

**Getting Started**

- open your game/new construct3
- Right click in a Scripts folder and click Add Script
- Copy the contents of c3Example_y8/main.js and paste them into your project's main.js file.
- Copy the y8API event sheet from c3Example_y8 and paste it into your project.
  - Note: Update the App ID global constant string in the Construct 3 Event Sheet with your Y8 Application ID.
  - You can create or find your App ID by registering a new application here: https://account.y8.com/applications/
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
Please replace the game id into global constant string GameID (Note: The test example uses let GameID = '270893'; — replace it with your assigned Game ID before going live.)

**Banners**

Banners are display ads that stay on screen during play. Sizes: 728x90, 300x250, 320x50, 468x60, 320x100.

In-game banner ads need Y8 approval for each game. While the game is in draft or in review, banners show test ads, so you can build the placement first; once it is released, they appear only if Y8 approved them (otherwise `bannersUnavailable`). See [Banners](https://docs.y8.com/sdk/advertising/#banners) for what Y8 approves.

1. Add an object where the banner should go (an invisible Sprite works), sized at least as large as the banner on screen. The banner is shown over the game canvas, centred on it.
2. Request it from a script action, passing a banner id of your choice, the size and the object type name:

   ```js
   requestBanner("bottom", 728, 90, "BannerSpot");
   ```

3. Add event sheet functions `onBannerShown(id)` and `onBannerFailed(id, errorCode)` to hear the result. Error codes include `bannerCooldown` (a banner of that size was requested too recently; the current one stays), `unfilled` (no ad this time), `invalidSize` (the object is smaller on screen than the banner) and `notVisible`.
4. If the object moves, call `moveBanner("bottom", "BannerSpot")`. Remove banners with `clearBanner("bottom")` or `clearAllBanners()`.

Each size gets at most one new banner every 180 seconds by default (never under 30), whether requested or refreshed automatically. Requires Y8 SDK 2.13.0, which `main.js` loads from the CDN.

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
- requestBanner(id, width, height, objectName) - Show a banner centred on an object (see Banners)
- moveBanner(id, objectName) - Move a banner to where its object is now
- clearBanner(id) / clearAllBanners() - Remove banners
- function onBannerShown(id) / onBannerFailed(id, errorCode) - Banner results
- function openProfile() - open the players profile
- function sendScreenshot() - Submit a screenshot of the game

**Important Variables**

- gameName - Game Name
- blacklistSite - if blacklistSite = 1 then show blacklist layout 
- userNameY8 - You can call userNameY8 variable to show Player's username.

**Need More Help**

There is a awesome community of devs and players on the id.net forum. Leave a message, we will try to reply.
