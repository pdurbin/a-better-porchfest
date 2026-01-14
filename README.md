# Goals

The goal of this project is to make an improved interactive map for [Porchfest](https://en.wikipedia.org/wiki/Porchfest) events. Porches can be far apart. We don't want to spend a ton of time digging through the schedule and optimizing our decisions. We want to be able to pull up the website on our phone and quickly figure out where to go next!

At a high level, what goals do we have, including uses cases?

* Playing next?
* Playing near me?
* Band list view.
* Bands near me!
* Keep it simple and snappy for all users!
* Mobile first!

# Proposed Features

## Demo Data (for development)

- [ ] Set the time for the demo data

* Use the real current time
* Change the set times such that the user is in the very middle of Porchfest.
* Quantize events to a half hour for realism.

- [ ] Import Brookline data

* [KML file](https://osdc.zulipchat.com/user_uploads/56571/DyPRiIUIU0yvHf69cf1vQJBn/brookline.kml)
* [Website to see how it looks](https://www.brooklineporchfest.org/)

## Other

- [ ] Color code markers

* One colors for "shows in the future", "show imminent/just starting", "shows over for the day"
    * Idea 1: Yellow=future, Green=imminent, Red=Over
    * Idea 2: Green=future, Bright Green=imminent, Transparent=Over

- [ ] Color-coding by genre

* Markers?
* Schedule?

- [ ] Time slider

* The schedule has a marker for "now" so that the user knows where in the schedule they are.
* Let the user change the slider, which will change the colors of the markers
    * Perhaps just by scrolling through the schedule, this happens?
        * Downside: you can't see what's on later without changing the time slider.
    * Otherwise a switch
        * Downside: Too many moving parts!

- [ ] Show schedule based on visible markers

* Have the schedule show up according to what's in the window.
    * Toggle full schedule / window view schedule
* Alt idea - instead of hiding items, just grey them out. That way it's one view.

- [ ] Action for clicking on gig in schedule

* Want to handle both "Get band info" and also "Find on map"
* Proposal: When you click, you get a popup "more about band", "find on map"
    * If you click "find on map" only then it scrolls to the right place (if necessary) and blinks
        * We particularly don't want to mess up the map view if the user just clicks on the schedule
        * Downside: if you scroll (even with the user's explicit expectation) it will change the window-view dynamic schedule. Bad UX probably.

- [ ] Action for clicking on marker

* Show address
* Show schedule at that location?
* Ideas...

- [ ] "Favorite" a gig

* In the schedule view, you click a star to indicate you want to see the show
    * Save to local storage
    * Marker becomes a star if the show is imminent
    * Danger: If the admins ever change the data, the user may lose a "favorite"
        * Warn the user?
        * Warn the admins?

- [ ] Band info

- [ ] Filters

* "I'm only interested in folk music", for example
* "I'm only interested in music from 2pm-4pm", for example

- [ ] Indicate genre by shape of marker

* This may not be necessary if we use colors for genre
    * Idea 1: Circle=Rock, Square=Alternative, Triangle=Hip-Hop, etc.

( think this through... )

# Files

* [index.html](master/index.html) - of course you'll want to "view source" when you get here
  * Has the main javascript for now. We could split it out.

* [data.js](master/data.js)
  * Contains demo data.
  * I pulled this from the old porchfest website (link below).

# Reference

* [The old porchfest website](https://web.archive.org/web/20250524170604/https://maldenporchfest.org/map/#schedule) for comparison.
* [FOSDEM's schedule](https://fosdem.org/2025/schedule/mobile/) for comparison

# Contributing

First, please get in touch via [Zulip](https://osdc.zulipchat.com/#narrow/stream/406743-boston) or [Signal](https://signal.group/#CjQKIGoh9--iomqNWoG9reLXz9RaAnDC_O1bw1BOk3gZlexUEhDy9Tes9s26HYi_bg5voUBE) and give us the public (not private!) half of your ssh key. Then you can clone the repo like this:

```
git clone dev@66.228.40.225:~/a-better-porchfest
```
