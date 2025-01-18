# Live Stream / Graphics Planning

## TASKS FOR LIVE STREAMING -&#x20;

* Setup Cameras (Day of)
* Select Music Theme and create a youtube playlist (DUE NEXT FRIDAY)
* Bernard can double check copyright of each music
* Create a "We'll be right back" video using slides or pptx.&#x20;
* Setup Audio (Day of)
* RTSP Key (Day before)
* Bring bernard a monitor (Day Before)
* Map of Event&#x20;

## Scenes

* Match Scene \[Bernard]
  * Large view of box cam w/ overlays for time remaining in match and robot names. think regular live tv sports broadcast stuff
    * Using only 1 top down camera per field.
    * If we want, we can create a scene where we split screen both fields.
* Team Win \[Bernard]
  * Enable studio mode in controls
  * have a winner screen with "Enter Winning Robot name here'
  * Edit the text
  * click transition
* Matches Overview \[Bernard]
  * Upcoming matches on one side, prev. match results on the other
  * Scene will use a Window Capture source on a browser and display from Challonge
  * Chat Included
  * Maybe announcer bottom window
* Pre Match Overview (Too difficult to Implement)
  * For each robot in the upcoming match, display robot name, picture, school/team affiliation, W/L record for the event
  * Can pull most data off of RCE and/or Challonge via API
  * maybe have a photo booth at the event for robot pictures. could be super cool to put each robot on a carousel and record a loop of it spinning 360 degrees instead of using a simple robot picture on the slide
* Announcer View \[Bernard]
  * For Interviews or just for announcer solo to talk about things
  * Announcer in full frame, no fields on each frame
  * Includes Chat
* Slideshow w/ Misc. Media (for use between matches) \[Jason]
  * Comet Clash Banner
  * Thank you to our sponsors
  * Matches Overview
  * QR Code with link to website (has links to challonge, RCE, etc)

## Scene & Graphics Colors

Are we going with Comet Clash colors or do you have something else in mind? Need 5 colors for graphics work to begin, see [https://color.adobe.com/create/color-wheel](https://color.adobe.com/create/color-wheel)

## Music

Music should be copyright free or copyright reduced. Copyright free is any song listed as "Copyright Free" by the author. "Copyright Reduced" is music past 10+ years where enforcement is difficult to identify, usually fan covers of video game music or abandonware video game music.

Bernard Has a couple playlists of "Copyright Reduced" music, see&#x20;

Scifi & Tech Themed - [https://www.youtube.com/watch?v=PNg7ua9\_Mjo\&list=PLRSUXJk77YEAoO-AvqN\_cG\_7wAFrHQRKe\&index=1](https://www.youtube.com/watch?v=PNg7ua9_Mjo\&list=PLRSUXJk77YEAoO-AvqN_cG_7wAFrHQRKe\&index=1)

100% Copyright Free Music -&#x20;

[https://www.youtube.com/watch?v=tDexBj46oNI\&list=PLRSUXJk77YEDOsWF5WwnNYkuR3pos7PnU\&index=1](https://www.youtube.com/watch?v=tDexBj46oNI\&list=PLRSUXJk77YEDOsWF5WwnNYkuR3pos7PnU\&index=1)&#x20;

&#x20;Jazz Music, pre 1927 (Copyright expiration date) -&#x20;

[https://www.youtube.com/watch?v=bqkEJG\_Lnag\&list=PLwKJ7rQxCefIGhMZeCP5XtKLcTY5c3JlF\&index=1](https://www.youtube.com/watch?v=bqkEJG_Lnag\&list=PLwKJ7rQxCefIGhMZeCP5XtKLcTY5c3JlF\&index=1)&#x20;

We can probably pick a theme and stick with it.

## Stream Setup System

Where do we place commentators, do commentators get a table, long power strips for power control for Streamers, etc.



<img src="../.gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">

| Equipment                                        | Source                   | Description             | Placement        |
| ------------------------------------------------ | ------------------------ | ----------------------- | ---------------- |
| HyperX Solocast & Microphone Rig (Mic)           | Limited Technologies LLC | Desk mounted Microphone | Announcer's Desk |
| Gopro Hero 3 (Cam, Action)                       | Limited Technologies LLC | Action Camera           | Field 2 Top      |
| Gopro Hero 10 (Cam, Action)                      | Limited Technologies LLC | Action Camera           | Field 1 Top      |
| Canon Rebel T3i (Cam, DSLR) + Lavalier mic (Mic) | Limited Technologies LLC | Point camera            | Announcer's Desk |
| MSI G65 Streamer Setup (Laptop)                  | Limited Technologies LLC | Main Streamer Laptop    | Announcer's Desk |
|                                                  |                          |                         |                  |

***

semi uncoordinated technical thoughts below proceed at your own risk :p

***

## Content Destinations

* YT Live Stream through RTSP YT
* Video Wall (atrium, main comp. area)
  * Has 16:9 area that we can definitely push content to via HDMI (port on wall under green staircase), and an additional strip on the right side that I don't know the aspect ratio of but would absolutely love if we could push content to that whole area. Idk if we send them 2 separate inputs, or 1 input with a weird aspect ratio, but either way it would be super cool to have box cam/whatever other content on the 16:9 portion, and use the right strip to always display the schedule or other info that's really only pertinent to in person people
* Projector (Birds' Nest, competitor pit area)
  * how to get video up here? my first thought is run a (long) ethernet cable from the streaming machine to the birds nest, then get another computer in the birds next with NDI Studio Monitor or vdo.ninja or something we set up w livekit to display video
  * \~\~want to avoid using yt stream for latency sake\~\~ YouTube's stream is only about 3min behind, and you should not be using YT as live match updates for the competitors, just public. Using something like Google Docs/Google Sheets to update the competitors on next match is more effective and useful.

## Audio/Video Sources & Current Equipment List

* Box Camera (Cam?) =
  * Can't check out iPhones from ATEC anymore :( maybe i'll send some emails and see who i have to beg to make this happen because there's no way they straight up don't have them anymore, right??
  * can apparently check out 90D w fisheye lens from ATEC - need to see if this is a decent option for the box in terms of framing - a typical DSLR 18-55mm is not able to capture the full box in the same way we could w the iphone ultrawide at widest focal length
    * A Canon 90D needs CANON EOS WEBCAM Utility to plug in, but can be plugged in directly via USB. my streamer laptop is setup for this already.
  * never mind i faked this i must have heard fisheye lenses were an option somewhere else
* Zoom H6 (Mic)
  * Check out from ATEC, send tracks into OBS via USB cable
  * the kit is supposed to include the USB cable but doesn't always. double check this at the ATEC checkout desk but also be prepared with own mini USB-B to USB A cable just in case.
  * inputs
    * onboard mic - room/box noise
    * music (need to convert from 1/4 in to 1/8in)
    * mic from media services (unknown but will probably use 1/4in or XLR so no conversion needed)
    * battlebox controller (need to convert from 1/4 in to 1/8in)
  * still not 100% sure on audio situation since we are hopefully getting PA + wireless mic from media services. I would like to be able to adjust levels for stream vs birds nest vs atrium separately, we'll see what they provide and figure everything else out later
    * OBS Can handle quick disconnect and quick reconnect. Are we putting this mic for the announcers or are we putting it in front of the competitors?
* HyperX Solocast & Microphone Rig (Mic)
  * (On loan from Limited Technologies LLC - ASK BERNARD TO BRING)
  * Really nice statically mounted microphone for presenters, commentators, etc.
* Canon Rebel T3i (Cam, DSLR) + Lavalier mic (Mic)
  * (On loan from Limited Technologies LLC - ASK BERNARD TO BRING)
  * Requires the EOS Webcam Utility to work, but produces 1080p
  * Works with OBS fine at 720p
  * Comes with Tripod
  * Really good for static close ups and some wide shots.
  * Comes with a Lavalier Microphone for Interviews&#x20;
* Gopro Hero 10 (Cam, Action)
  *
* Gopro Hero 3 (Cam, Action)
  * (On loan from Limited Technologies LLC - ASK BERNARD TO BRING)
  * Requires a USB Dongle (which I will bring if reminded) to MicroHDMI into cam
  * [https://www.youtube.com/watch?v=uS-XHBf\_raE](https://www.youtube.com/watch?v=uS-XHBf_raE) (tutorial)
  * Really good for high angle - top down view
* Misc USB Webcams (Cam, Fixed)
  * Multiple small USB webcams can be chained together to create action camera looks, view in certain areas.
*   MSI G65 Streamer Setup (Laptop)

    * (On loan from Limited Technologies LLC - ASK BERNARD TO BRING)
    * OBS Setup and ready to go
    * EOS Webcam utility setup and ready
    * Tested with Limited Technologies Streaming equipment



## Misc. Notes

* Will likely need to involve something like [CasparCG](https://casparcg.com) ([less preferable](https://github.com/CasparCG/help/wiki/Media%3A-HTML-Templates#the-caveats)) or [SPX-GC](https://www.spx.graphics) (seems to be better suited for our use case) for the scenes which have dynamic data stuff. Authoring templates is done via HTML and/or via tools like [Loopic](https://www.loopic.io). Bringing these graphics into OBS is trivial.
  * need to start designing this stuff soon (now!)
    * Is there a reason we're not thinking of just creating Stock OBS graphics? Like static vids and stuff? Nobody will complain about us not having news-sports style graphics if we look decently professional with good lighting. -B
  * one advantage that casparcg has over SPX that I hadn't considered previously - since CasparCG supports NDI output, we can actually receive the graphics with an alpha channel. SPX does playout on a web page, so to include the graphics in OBS we need to use a browser source and then key out whatever background color is used
    * NVM. SPX also supports CasparCG playout. will need to do more research on if it makes sense to use casparcg directly then, because otherwise we'd probably run SPX with Caspar.
  * if we end up using casparcg directly we will likely also want to use smth like [https://github.com/SuperFlyTV/SuperConductor?tab=readme-ov-file](https://github.com/SuperFlyTV/SuperConductor?tab=readme-ov-file)
* something something bitfocus companion
* Should only need 2 machines to run everything
  * Marketing Mac mini - run OBS Studio for streaming/compositing tasks + graphics playout
    * Use onboard HDMI output for operator monitor
    * need USB-C dongle for additional HDMI output to video wall
  * Some random other computer (one of the ericsson's or even a Pi?) - birds' nest playback
  * Really don't want to move RoboPC since that runs a bunch of other services and I'm afraid things will break if its not on our network, although it unfortunately currently holds my DeckLink :/ so can't use that for video capture
    * if we need to offload a task from the Mac mini, both solutions we plan to use for graphics are accessible over internet / tailscale maybe?
    * Both use some sort of web-based/TCP control solution so we can still control from the mac. as far as operator is concerned it may as well be on the local machine
    * CasparCG has a window, NDI and an FFMPEG output method. AFAIK NDI gets weird with VPNs/running over the internet, but FFMPEG could send an RTMP stream over the internet to smth like LiveKit that we can bring into the stream easily. or we can use the window output method with vdo.ninja, similar idea but feels more scuffed
    * SPX serves a web app for playout and control which we can super easily access over Tailscale.
* OBS 30.2 adds a new 'hybrid MP4' recording format type that 'supports inserting chapter markers into the file via a hotkey or API' - we should try to use this and add markers for each match so it's hopefully easier to edit down
  * If possible we should try to record the box camera raw with no overlays but not a huge deal if we can't

### Battle Box Controller stuff

* Rough idea is to add a new peer to the battlebox controller's ESP NOW network, which just dumps those messages over USB serial to a machine
* Each team's assist/ready/tapout events could trigger a little pop up or status indicator on the stream
  * on second thoughts, 'status indicator' implies that state is saved somewhere, which i don't really want to deal with so nvm lol&#x20;
  * This is a beautifully complicated idea, I advise instead just including a clock next to the camera footage so we can see the live match time and can work backwards xD - B
* Pressing victory buttons could trigger OBS Team Win scenes and maybe auto update Challonge via API
* Starting/unpausing/changing duration of a match should send a message with the amount of millliseconds remaining in the match (used to display a count down timer on stream)
* Pausing a match should send a message which we use to stop the countdown timer
