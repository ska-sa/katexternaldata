# katexternaldata

Karoo Array Telescope (KAT) system package with data from sources external to SARAO that is updated automatically
on a daily basis by the HEAD Node on site (e.g., TLEs and Earth orientation parameters).

## Usage

The `catalogues` directory contains catalogues of sources.  A subset of these are available at run-time in
MeerKAT's control and monitoring system as a [`katpoint.Catalogue`](https://github.com/ska-sa/katpoint/blob/65f7a18083b3d44c8abc69b5f5d7723ed8c1509d/katpoint/catalogue.py#L46) object.
Typically called `kat.sources` in observation scripts.  In the `katpoint.Catalogue` object, 
the satellite TLE targets can be filtered by tags.  The currently available tags are:
`BEIDOU`, `GALILEO`, `GEO`, `GPS`, `GLONASS`, `INTELSAT`, `Iridium`, `Iridium-NEXT`, `SCIENCE`, `ZoA`.
The tag names are maintained in a different repository, so check [this file](https://github.com/ska-sa/katcamconfig/blob/dff62c9aa4c5664ad792d3ac7b43ffe781d8f01c/systems/base_conf.conf#L258) for the latest details.

Not all sources are loaded automatically into the `kat.sources` objects.  For satellite TLEs, the catalogues
directory contains both the source files (`<type>.txt`) and corresponding filter files (`<type>_keep.txt`).
Only the satellites listed in the `_keep.txt` files are available in the `kat.sources` catalogue.
However, the full files could be loaded manually.

## URLs used for downloads

**NOTE:** The URLs for downloads are maintained in a different repository, so check
[this file](https://github.com/ska-sa/katcamconfig/blob/master/static/other/kat-downloader.conf) for the
latest details.  As a convenience, the URLs (possibly outdated) are repeated here:

### Earth orientation parameters
 - IERS daily EOP: ftp://ftp.iers.org/products/eop/rapid/daily/finals.daily
 - IERS daily EOP (2000A calculation method): ftp://ftp.iers.org/products/eop/rapid/daily/finals2000A.daily
 - IERS leap second data: https://hpiers.obspm.fr/iers/bul/bulc/Leap_Second.dat

### Medium to high orbit satellites (TLEs)
 - [beidou.txt](http://celestrak.com/NORAD/elements/beidou.txt)
 - [galileo.txt](http://celestrak.com/NORAD/elements/galileo.txt)
 - [geo.txt](http://www.celestrak.com/NORAD/elements/geo.txt)
 - [gps.txt](http://celestrak.com/NORAD/elements/supplemental/gps.txt)
 - [glonass.txt](http://celestrak.com/NORAD/elements/supplemental/glonass.txt)
 - [intelsat.txt](http://celestrak.com/NORAD/elements/supplemental/intelsat.txt)
 - [iridium.txt](http://www.celestrak.com/NORAD/elements/iridium.txt)
 - [iridium-NEXT.txt](http://www.celestrak.com/NORAD/elements/iridium-NEXT.txt)
 - [science.txt](http://celestrak.com/NORAD/elements/science.txt)
 - [stations.txt](http://www.celestrak.com/NORAD/elements/stations.txt)
 - [visual.txt](http://www.celestrak.com/NORAD/elements/visual.txt)

## Solar system objects and deep space satellites
- [Soft03Cmt.edb](http://www.minorplanetcenter.net/iau/Ephemerides/Comets/Soft03Cmt.txt)
- [Soft03CritList.ebd](http://www.minorplanetcenter.net/iau/Ephemerides/CritList/Soft03CritList.txt)
- [Soft03Distant.edb](http://www.minorplanetcenter.net/iau/Ephemerides/Distant/Soft03Distant.txt)
- [Soft03Unusual.edb](http://www.minorplanetcenter.net/iau/Ephemerides/Unusual/Soft03Unusual.txt)
