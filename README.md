# Twitter Mute Chain
This is a browser extension to mute all followers of a user on Twitter.
The idea is to mitigate harassment silently, so as not to encourage dog-piling.

The main challenge is that Twitter has rate limiting for 'muting' API calls, whereas it appears to not enforce these limits for blocks.
So the maximum rate for muting is about once per 5 seconds.
(Leave it running in a tab before bed, or perhaps before a long weekend for a large number of mutes.)

There is also a Block->Mute Chain feature, which will convert your account's blocks to mutes (including unblocking the account after it is muted).
The same rate limit applies, so settle in.

My own contributions to this extension are minimal and mainly involve changing the word `block` to `mute` in several places.
Please direct all praise to the original authors of [Twitter Block Chain](https://github.com/satsukitv/twitter-block-chain).

# Original: Twitter Block Chain

This browser extension helps users who are likely to be, or currently are being dog-piled.
By navigating to a user's followers (or following) page and activating the 
plugin, you can block all users on that page.

# Installation

Chrome users can install the extension here: [Chrome Web Store](https://chrome.google.com/webstore/detail/twitter-block-chain/dkkfampndkdnjffkleokegfnibnnjfah?hl=en)

Firefox users can install the extension here: [Mozilla Add-ons](https://addons.mozilla.org/en-US/firefox/addon/twitter-block-chain/)

# Build Instructions

* Building requires `grunt` and `grunt-cli`
* Chrome: `grunt build-chrome`
* Firefox: `grunt build-firefox`

# FAQs 

I'm trying to use this as an unpacked extension and it isn't working?

Run `bower install` first to pull down the dependencies.

How do I activate the plugin?

Browse to a following/followers page on twitter and click the icon in the 
toolbar on Chrome. If it says you're not on a following/followers page, try 
refreshing first.

How do I stop the blocking?

Click the X in the top right corner of the blocking report to stop all 
blocking. Note that this will not unblock any users you have already blocked.

How do I figure out who I blocked, and who they were following/followed by?

Right click the extension icon in Chrome and click Options. You can view all 
blocks made on this page, including searching by username. Blocks are stored 
locally, and not synced to the cloud.

# To Do / Possible Features

* Output a JSON object of users from a page, to later feed into the extension.
* Option to mute users instead of blocking them.
