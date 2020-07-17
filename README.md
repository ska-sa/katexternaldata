# katexternaldata

KAT system package with data from sources external to SKA SA that is updated automatically on a daily basis by the HEAD Node on site (e.g. TLEs and Earth orientation parameters)..

This directory contains catalogue of sources that is accessible with a list of targets, which are assumed to be unique, but may have the same name. These targets are grouped in tags, and the currently available tags are:
['BEIDOU', 'GALILEO',  'GEO', 'GPS', 'GLONASS', 'INTELSAT', 'Iridium', 'Iridium-NEXT', 'SCIENCE', 'ZOA']

The catalogues directory contains the source files ('.txt') to the satellites, with '_keep.txt' serving as filter filess to the '.txt' files that only keep the satellites listed in the '_keep.txt' files.

# URLs used for satellite downloads 

 - [BEIDOU](http://celestrak.com/NORAD/elements/beidou.txt)
 - [GALILEO](http://celestrak.com/NORAD/elements/galileo.txt)
 - [GEO](http://celestrak.com/NORAD/elements/geo.txt)
 - [GPS](http://www.celestrak.com/NORAD/elements/gps-ops.txt)
 - [GLONASS](http://www.celestrak.com/NORAD/elements/glo-ops.txt)
 - [INTELSAT](http://celestrak.com/NORAD/elements/supplemental/intelsat.txt)
 - [Iridium](http://www.celestrak.com/NORAD/elements/iridium.txt)
 - [Iridium-NEXT](http://www.celestrak.com/NORAD/elements/iridium-NEXT.txt)
 - [SCIENCE](http://celestrak.com/NORAD/elements/science.txt)