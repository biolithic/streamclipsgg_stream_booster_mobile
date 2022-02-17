# streamclipsgg_stream_booster_mobile
StreamBooster extra features for mobile devices for live streams

----


## SOURCE

This source can be found at: 

Radicle.xyz (Web3.0) biolithic@hydjcpzkkofigwozykxmyew8ofua1co7ix77x4hu7jh8j8g5b36fnc

Gitlab: Streamclipsgg https://gitlab.com/streamclipsgg

Bitbucket: Streamclipsgg https://bitbucket.org/streamclipsgg


## Streamclips.GG StreamBooster browser extension for mobile devices


## Basic Overview

Installing this in your browser will enhance the streaming and chatting experience on livestreams on mobile Android devices for the Kiwi browser.


## How to use this

This free extension is an add-on or plugin or extension to mobile Android devices using Kiwi browser. It can be completely added or removed at any time, and the site will continue to work separately. You can find Kiwi browser in the Google Play Store or F-Droid Store or APKpure.com , it is based on Google Chrome browser with some extra features you can turn on or off.


## Which websites does it work on now?
Youtube.com, Odysee.com, Glimesh.tv. Coming soon in 2022: EntropyStream, Theta.tv, Rumble.com/Locals.com


## 🔧 Install it!

1. Download & extract the [latest🧪version] 

2. _Go to your Browser's Extensions page (kiwi://extensions/)_ 

3. _Activate "Developer mode"_ (top right)

4. _Click the "Load unpacked" button <br>_

_& Select the extracted folder_


## Tracking/Security

This extension saves information to your browser locally if you choose such your options/preferences, chat, browser version which you can export out to yourself via CSV file and is deleted when you uninstall the extension. We save none of your options/preferences "in the cloud" at this time.  Optionally, you can take voice notes, screencaps and video clips and save them to the cloud and the data send/saved with them are your username, stream title, game title, date, stream category, browser version and product key code which are needed to search and find the media to view again afterwards. We currently use no tracking or advertising or cookies at this time of 9/2021. This may change and you will be notified if it does. We are currently a very small team and do not have time or resources for large privacy policy scope or legal/public relations/social/customer service policy other than to provide the basic technical features needed to the streamers for their usage.


## Does this work on iPhones, iPads, Windows Phones, Firefox, or something you haven't mentioned here?

No.


## How to get he;p with using this or questions or issues

How to get help is described at the website streamclips.gg at the bottom of the page.
You may email us at: support@streameranalytics.com or file a bug on here.
This help document might help you: https://github.com/ImprovedTube/YouTube-Extension/discussions/753
This help document might help you: https://github.com/ParticleCore/Particle/wiki/Report-a-problem


## Option Menu

- This extension adds an option menu to the website where you can save options for yourself which will happen on each page load. For example, you can watch the stream and click the options cog icon to open it change the chat background in real time as you watch. The options/preferences are saved to your computer and not sent out to the internet.


## Export / Offline

- This extension can export chat logs from live streams in CSV form.  These can be viewed in a spreadsheet program, imported into the browser extension, or imported into the https://www.streameranalytics.com/offline application to view offline if later you do not have the internet.


## Interoperability

- This browser extension works with import/export features of the Streamclips.GG StreamBooster browser extension for mobile so that you can import/export between each. As a simple example, you can export your stream chat from Glimesh on your computer so that people can import it on their phones and see the chat scroll by next to the video archive on Youtube or Odysee.


## Be Featured

- If you use this browser extension in your streaming and would like to be featured on one of our webpages, reach out to us and let us know!  Thanks!


## Source/Funding/Leadership/etc

This is currently funded/hosted 100% by the creator/developer, who is a person not associated with any live streaming or video company in any formal way. 
This is not funded or associated with any major corporation such as Amazon, Youtube, Microsoft, etc...
We have had many people and groups contribute to this idea as it grew over time and give feedback on it online and in person. This ranges from conventions like Pax, Vidcon and TwitchCon, universities like University of Cincinnati and M.I.T., local nerding meetups and cons, and conversations over Discord, Guilded, and Zoom with other streamers. The full list of thanks is on the website http://streamclips.gg at the bottom of the page.


## License

This is released under [GNU 3 license] . Copyright (c) 2022 [biolithic]


## How To Help Make This Better

The browser extension is created as such:
- The extension currently uses 2 third-party JS libraries: Dexie (Apache 2.0), and JQuery (MIT).
- The styles for the extension are all in styles.css
- The "background" JS for the extension is in background.js
- The "foreground" or DOM/page speciic JS for the extension is in foreground.js
- The HTML for the extra page menus this extension provides are found in HTML files named like this: options_menu.html.
- socialmedia.json is an editable file which has the sharing options for the user for social media. Maybe be added to or removed from.
- The namespace for this is scgg and so added elements will be named with ids such as scggOptionsMenu
- for html ids, we are using camel case such as scggOptionsMenuForm
- for html classes, we are using dashes such as social-media-icon
- in the styles.css file, we break the css up into the styles needed for each html file or section
- we use the following html id template names for making html elements
- scggOptionsMenu -- this is a menu wrapper
- scggOptionsMenuForm -- this is a form id inside the options menu
- scggOptionsInputText -- this is input type = text inside the options menu
- scggOptionsInputSearch -- this is input type = search inside the options menu
- scggOptionsButton -- this is a button inside the options menu
- scggOptionsWrapper -- this is a wrapper for a page area


## Javascript structure

We are using Google Chrome browser manifest_version 3.

Chrome.storage.sync works for saving user preferences.
LocalStorage works for saving social media options.

There are rate limits for each. This is why we are using both to save a large number of options and preferences.

We are using underscores for function names such as function create_annotation

We are using camelCase for variable names such isModalOpen

We are using the variable object window.scggOptions for the user options/preferences

We are using the following function name standards to help understand the code: 
get_ (get_db_name)
This type of function will get some data/setting and return it to another function.

helper_ (helper_build_all_dbs)
This type of function will help another function by things like building an html menu or doing a calculation.

set_ (set_refresh_voice_done)
This type of function will set/store some data/setting from another function.

user_ (user_do_at_chats)
This type of function happens from direct action by the user.

The code is laid out in function names alphabetically top to bottom in this order of sections:
HELPERS - utility functions
BUILD - build processes on page load
RECORDED CHAT - functions to record and show chat
KEYBIND TOGGLES - function to handle chat toggles and keybinds for them
OPTIONS - options functions for this browser extension

Code can happen based on 2 selectors which can activate on page load: 
window.scggIsGlimesh is true or false (or whatever platform it is you are inquiring that we support).
window.scggIsMobile is true or false for the user device type.
window.scggIsDesktop is true or false for the user device type.

We don't do DOM selecting for elements over and over.
At extension load, we select each DOM element from the extension we use and assign it to a variable like this window.scggSnackbarRef.
Then, to window.scggSnackbarRef we do whatever we want with it - show/hide, give it some text to show, paint it black, whatever. 
Where window.scggSnackbarRef refers to the DOM element id scggSnackbar.

API FOR THIRD-PARTY INTEGRATION
When the page loads, the extension adds these classes to the body element of which you can hook on to yourself.
scgg-glimesh (or whatever platform it is you are inquiring that we support).
scgg-mobile or scgg-desktop for the user device type.

HIDE/SHOW
Elements are added to the page hidden to the user.
To show them, we add class scgg-bl or scgg-fl (block or flex). 
To hide them, we remove those classes.

SEARCH THIS CHAT/SEARCH PAST CHATS
To search the current stream chat, we verify class scgg-multiple is NOT on the button.
To search the previous saved chats, we look for class scgg-multiple on the button.


## Glimesh Real Time Highlights

- When a streamer purchases code(s) for taking/posting media (annotations, caps, clips) from the stream, anyone with this free base extension can view the media which appears in a pull down menu from the top of screen or by pressing the "🎥" button on the drop-down menu of the extension.


## Glimesh Real Time Highlights API

- We will provide API endpoints for 3rd parties to access a stream's media. This is not live yet.


## Glimesh User Actions

- Users can make an action happen in 3 ways on the stream.  Pressing a menu button with the mouse, pressing a keybind with the keyboard, and saying a voice command with their mouth. We are researching how to connect this to foot pedals as well to add another way to help the streamer. 


## Glimesh External resources

- this extension can optionally call out to the Glimesh.TV API for user account validation.
- this extension can optionally call out to MixCloud and Spotify for its playlist feature.
- this extension can optionally call out to the our API for saving notes, caps, clips.
- items/media are moved to CDN's and permanent storage and not stored on Streameranalytics.com or Glimesh.TV. 


## Voice Commands and Text To Speech

- This uses a library that users can optionally use voice commands to make things happen on stream or can read chat out loud which applies to the user's preferences. This is optional to the user by saving preferences in the extension menu at the top of the screen.


## Public 

- this extension can post text, images, and short video clips which can be also publicly viewed by everyone at:
- streamclips.gg/glimesh/screencaps/category/*
- streamclips.gg/glimesh/screencaps/createdBy/*
- streamclips.gg/glimesh/screencaps/streamer/*
- streamclips.gg/glimesh/screencaps/tag/*
- streamclips.gg/glimesh/screencaps/type/*
- streamclips.gg/glimesh/screencaps/votes/*

- streamclips.gg/glimesh/screenclips/category/*
- streamclips.gg/glimesh/screenclips/createdBy/*
- streamclips.gg/glimesh/screenclips/streamer/*
- streamclips.gg/glimesh/screenclips/tag/*
- streamclips.gg/glimesh/screenclips/type/*
- streamclips.gg/glimesh/screenclips/votes/*

- the streamer can access their own admin dashboard at streamclips.gg and login at the top of page to change, download, share or delete their media.


## Caps/Clips Redundancy

One of the features that separates this cap/clip service from other services like Mixer, DLive, Twitch, Youtube is redundancy. Since this is a paid feature, streamers have the option to save their caps/clips to up to 4 different locations and services  around the world.  This is so if you think "Oh no, XYZ service/locale/area went down/was deleted" you potentially have the same file/video on 3 other services on 3 other continents on earth which may or may not have been affected since they have different owners. We are looking to expand the number of redundant backups to more than 4 in the future.
