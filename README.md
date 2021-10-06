# windows_spotlight_scrapper
Get images from Windows Spotlight, Location Names, and try to append coordinates using location names and OpenStreetMaps search


## https://github.com/ORelio/Spotlight-Downloader#spotlight-api

#Spotlight API
The Spotlight API is located on the following endpoint:

https://arc.msn.com/v3/Delivery/Placement?pid=209567&fmt=json&rafb=0&ua=WindowsShellClient%2F0&cdm=1&disphorzres=9999&dispvertres=9999&lo=80217&pl=en-US&lc=en-US&ctry=us&time=2017-12-31T23:59:59Z

Where the expected arguments are:

pid : Public subscription ID for Windows lockscreens. Do not change this value
fmt : Output format, e.g. json
rafb : Purpose currently unknown, optional
ua : Client user agent string
cdm : Purpose currently unknown, cdm=1
disphorzres: Screen width in pixels
dispvertres: Screen height in pixels
lo : Purpose currently unknown, optional
pl : Locale, e.g. en-US
lc : Language, e.g. en-US
ctry : Country, e.g. us
time : Time, e.g. 2017-12-31T23:59:59Z
The JSON response contains details for one or more image(s) including image url, title, sha256, ads, etc.

Spotlight API URL was originally found in this file and up to date API URL in this file, thanks to the authors for their findings!
