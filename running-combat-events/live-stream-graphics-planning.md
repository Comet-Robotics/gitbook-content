# Live Stream  / Graphics Planning

{% embed url="https://www.figma.com/board/gEfSkfhj31eD1XMoWmmaTs/Comet-Clash-Broadcast-Diagram?node-id=0-1&t=84tFMUeo5ZFh9UNc-1" %}

there are GIFs for FRC game win animations in that figjam that don't play in the embed - here's the link to access it outside of this embed: [https://www.figma.com/board/gEfSkfhj31eD1XMoWmmaTs/Comet-Clash-Broadcast-Diagram?node-id=0-1\&t=84tFMUeo5ZFh9UNc-1](https://www.figma.com/board/gEfSkfhj31eD1XMoWmmaTs/Comet-Clash-Broadcast-Diagram?node-id=0-1\&t=84tFMUeo5ZFh9UNc-1)

## Scenes

* Match Scene
  * Large view of box cam w/ overlays for time remaining in match and robot names. think regular live tv sports broadcast stuff
* Team Win
  * Make cool animations for orange/green win like the ones on FRC streams
  * thought: maybe we change the team colors, this is just what the box colors for each team currently are
* Matches Overview
  * Upcoming matches on one side, prev. match results on the other
* Pre Match Overview
  * For each robot in the upcoming match, display robot name, picture, school/team affiliation, W/L record for the event
  * Can pull most data off of RCE and/or Challonge via API
  * maybe have a photo booth at the event for robot pictures. could be super cool to put each robot on a carousel and record a loop of it spinning 360 degrees instead of using a simple robot picture on the slide
* Slideshow w/ Misc. Media (for use between matches)
  * Comet Clash Banner
  * Thank you to our sponsors
  * Matches Overview
  * QR Code with link to website (has links to challonge, RCE, etc)

semi uncoordinated technical thoughts below proceed at your own risk :p

***

## Content Destinations

* YT Live Stream
* Video Wall (atrium, main comp. area)
  * Has 16:9 area that we can definitely push content to via HDMI (port on wall under green staircase), and an additional strip on the right side that I don't know the aspect ratio of but would absolutely love if we could push content to that whole area. Idk if we send them 2 separate inputs, or 1 input with a weird aspect ratio, but either way it would be super cool to have box cam/whatever other content on the 16:9 portion, and use the right strip to always display the schedule or other info that's really only pertinent to in person people&#x20;
* Projector (Birds' Nest, competitor pit area)
  * how to get video up here? my first thought is run a (long) ethernet cable from the streaming machine to the birds nest, then get another computer in the birds next with NDI Studio Monitor or vdo.ninja or something we set up w livekit to display video
  * want to avoid using yt stream for latency sake&#x20;

## Audio/Video Sources

* Box Camera
  * Can't check out iPhones from ATEC anymore :( maybe i'll send some emails and see who i have to beg to make this happen because there's no way they straight up don't have them anymore, right??
  * can apparently check out 90D w fisheye lens from ATEC - need to see if this is a decent option for the box in terms of framing - a typical DSLR 18-55mm is not able to capture the full box in the same way we could w the iphone ultrawide at widest focal length
    * never mind i faked this i must have heard fisheye lenses were an option somewhere else
* Zoom H6
  * Check out from ATEC, send tracks into OBS via USB cable
  * the kit is supposed to include the USB cable but doesn't always. double check this at the ATEC checkout desk but also be prepared with own mini USB-B to USB A cable just in case.
  * inputs
    * onboard mic - room/box noise
    * music (need to convert from 1/4 in to 1/8in)
    * mic from media services (unknown but will probably use 1/4in or XLR so no conversion needed)
    * battlebox controller (need to convert from 1/4 in to 1/8in)
  * still not 100% sure on audio situation since we are hopefully getting PA + wireless mic from media services. I would like to be able to adjust levels for stream vs birds nest vs atrium separately, we'll see what they provide and figure everything else out later

## Misc. Notes

* Will likely need to involve something like [CasparCG](https://casparcg.com) ([less preferable](https://github.com/CasparCG/help/wiki/Media%3A-HTML-Templates#the-caveats)) or [SPX-GC](https://www.spx.graphics) (seems to be better suited for our use case) for the scenes which have dynamic data stuff. Authoring templates is done via HTML and/or via tools like [Loopic](https://www.loopic.io). Bringing these graphics into OBS is trivial.
  * need to start designing this stuff soon (now!)
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
  * on second thoughts, 'status indicator' implies that state is saved somewhere, which i don't really want to deal with so nvm lol
* Pressing victory buttons could trigger OBS Team Win scenes and maybe auto update Challonge via API&#x20;
* Starting/unpausing/changing duration of a match should send a message with the amount of millliseconds remaining in the match (used to display a count down timer on stream)
* Pausing a match should send a message which we use to stop the countdown timer



