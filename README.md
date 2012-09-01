# python-osm-time-domain

[![Build Status](https://secure.travis-ci.org/martinfilliau/osm-opening-hours.png?branch=master)](http://travis-ci.org/martinfilliau/osm-opening-hours)

Set of classes to parse opening hours, service time and collection time from OpenStreetMap nodes.

## Example

Below is a simple example of using the module for opening hours, see tests for more examples.

    from osm_time.opening_hours import OpeningHours

    definition = OpeningHours("Mo-Fr 12:00-22:00; Sa-Su 10:00-18:00")
    
    print definition.is_open("tu", "15:00")     # check if it's open on Tuesday at 3pm

    print definition.minutes_to_closing("Fr", "21:30")  # get a number of minutes to the closing

## More information

Contributing opening hours to OpenStreetMap

Objectives:

 * Provide an UI allowing to contribute opening hours to POI in OpenStreetMaps (à la wheelmap.org)
 * Provide a simple API to allow manipulation of opening hours
 * Propose a way of storing/indexing opening hours in Solr and querying them
