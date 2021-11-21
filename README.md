# windows_spotlight_scrapper
Get image URL from Windows Spotlight API, Location Names, and try to append coordinates using location names and OpenStreetMaps search (not working that great, since it located Mars and Orion nebula for example)

File: <code> slike.xlsx </code> ~ 1000 Locations
![image](https://user-images.githubusercontent.com/29605484/136181686-ca9f53be-8708-4d4c-a38a-2572e7fb72e1.png)


# Spotlight API
The Spotlight API is located on the following endpoint:


 <code>
https://arc.msn.com/v3/Delivery/Placement?pid=209567&fmt=json&rafb=0&ua=WindowsShellClient%2F0&cdm=1&disphorzres=9999&dispvertres=9999&lo=80217&pl=en-US&lc=en-US&ctry=us&time=2017-12-31T23:59:59Z
 </code>

Also there is a mini game, something like really simple version of geoguessr
![image](https://user-images.githubusercontent.com/29605484/142759423-ce728116-d455-46af-9542-056f5b91a510.png)

## Where the expected arguments are:
 
* <code>  pid </code> : Public subscription ID for Windows lockscreens. Do not change this value
* <code>  fmt </code> : Output format, e.g. json
* <code>  rafb </code> : Purpose currently unknown, optional
* <code>  ua </code> : Client user agent string
* <code>  cdm </code> : Purpose currently unknown, cdm=1
* <code>  disphorzres</code> : Screen width in pixels
* <code>  dispvertres</code> : Screen height in pixels
* <code>  lo </code> : Purpose currently unknown, optional
* <code>  pl </code> : Locale, e.g. en-US
* <code>  lc </code> : Language, e.g. en-US
* <code>  ctry </code> : Country, e.g. us
* <code>  time </code> : Time, e.g. 2017-12-31T23</code> :59</code> :59Z

The JSON response contains details for one or more image(s) including image url, title, sha256, ads, etc.

Spotlight API URL was originally found in this file and up to date API URL in this file, thanks to the authors for their findings!

###### https://github.com/ORelio/Spotlight-Downloader#spotlight-api
