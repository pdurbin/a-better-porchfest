# License

MIT good?

# Files

* [index.html](index.html) - of course you'll want to "view source" when you get here
  * Has javascript for now. We could split it out.

* [data.js](data.js) - of course you'll want to "view source" when you get here
  * Contains demo data.
  * I pulled this from the old porchfest website (link below).

# Goals

At a high level, what goals do we have, including uses cases?

* Playing next?
* Playing near me?
* Band list view.
* Bands near me!
* Keep it simple and snappy for all users!
* Mobile first!

# Proposed Features

[ ] - Set time for demo data

* Use the real current time
* Change the set times such that the user is in the very middle of Porchfest.
* Quantize events to a half hour for realism.

[ ] - Color code markers

* One colors for "shows in the future", "show imminent/just starting", "shows over for the day"
    * Idea 1: Yellow=future, Green=imminent, Red=Over
    * Idea 2: Green=future, Bright Green=imminent, Transparent=Over

[ ] - Toggle full schedule / window view schedule

[ ] - Time slider

* The schedule has a marker for "now" so that the user knows where in the schedule they are.
* Let the user change the slider, which will change the colors of the markers
    * Perhaps just by scrolling through the schedule, this happens?
        * Downside: you can't see what's on later without changing the time slider.
    * Otherwise a switch
        * Downside: Too many moving parts!

[ ] - Show schedule based on visible markers

* Have the schedule show up according to what's in the window.

[ ] - Action for clicking on gig in schedule

* Want to handle both "Get band info" and also "Find on map"
* Proposal: When you click, you get a popup "more about band", "find on map"
    * If you click "find on map" only then it scrolls to the right place (if necessary) and blinks
        * We particularly don't want to mess up the map view if the user just clicks on the schedule
        * Downside: if you scroll (even with the user's explicit expectation) it will change the window-view dynamic schedule. Bad UX probably.

[ ] - Action for clicking on marker

* Show address
* Show schedule at that location?
* Ideas...

[ ] - "Favorite" a gig

* In the schedule view, you click a star to indicate you want to see the show
    * Save to local storage
    * Marker becomes a star if the show is imminent

[ ] - Band info

( think this through... )

# Reference

[The old porchfest website](https://web.archive.org/web/20250524170604/https://maldenporchfest.org/map/#schedule) for comparison.
[FOSDEM's schedule](https://fosdem.org/2025/schedule/mobile/) for comparison
