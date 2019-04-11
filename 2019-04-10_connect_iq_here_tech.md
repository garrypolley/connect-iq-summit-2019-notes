# Here Tech Talk

World's leading location technology company. Started up in the 80s.

I am an idiot. (Did not start my watch when in Spain on a mountain) -- Richard talked about how good his Fenix 5 was and how he used it.

Talk is about how does the Maps API work. And how can you put content on the map and make it extra awesome like Crackers.

Places API, Public Transit API, and how can they be used in the Connect IQ apps to be the best of the maps.

`Class: Toybox::WatchUi::MapView`

Seven new methods:

* `getMapMode(mode)`
* `getMapMode()`
* `clear()`
* `setMapMarker(markers)`
* `setPolyline(polyline)`
* `setMapVisibleArea(topLeft, bottomRight)`
* `setScreenVisibleArea(topLeftX, topLeftY, bottomRightX, bottomRightY)`

`Toybox::WatchUI::MapTrackView` <-- from map view

No new methods -- it has minor different behavior than the MapView.  A MapTrackView shows where you are at on the map, and is always centered on where the user is at.

## Tips and Tricks

* The MapView cannot be the first view in the app -- fixed with 3.1 update
* Use the `getProjected` to set a more custom "zoom level", default is a bounding box that auto centers
* Map view is always full screen
    * You can set the screen visible area and it can push the map higher
    * Use a full "override" to show the map above some text, or actionable deal
* Map markers 
    * Need `MapView.setMapMarker(marker)` <-- need array
    * `.setIcon`
    * `.setLabel`
    * `new Ui.MapMarker`
    * Polyline is a set of `Position.Location` 
        * `.setColor`
        * `.setWidth`
* `.clear()` removes all the things -- need to keep track if you want to remove one thing at a time, a full redraw of all the things
* Max JSON size is 16kb that the device can handle

## Here doc

* https://developer.here.com
* Places API for finding points of interest
* Use it via the REST calls
* Use `Communications.makeWebRequest` or `Communications.MakeImageRequest` -- this will help with my recipe loading
* https://github.com/leopectus/connectiq-workshop -- example of loading a Map from Here
