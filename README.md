Web Optimization Project
==================
#####Udacity FE Web Developer Nanodegree - Project 4#####
---

Contents
--------

1. [How to Run / Test](#chapter-1)  
2. [Optimizations Performed](#chapter-2)  
3. [Resources Used](#chapter-3)    

How to Run / Test <a id="chapter-1"></a>
-----------------
There are two ways for you to test/demo my Web Optimization work:    

1. Simply visit the [live version](http://www.sweetwaterhandball/opt/index.html "Web Optimization Project") hosted on my web server.  
2. Download the Git ZIP, extract, and run maps.html on your favorite browser. 

Each page has optimized to achieve a 90+ Google PageSpeed score. In addition, the views/pizza.html page and its associated Javascript have optimized to achieve a 60+ FPS rendering speed. I have included two versions of each HTML page: a production version and a development version.  
- The production versions include minified CSS and Javascript, and run optimally. They are the .html files (e.g. index.html).
- The development versions include no minification, so that you can more easily read through the code and understand what's happening. Theey are the _dev.html files (e.g. index_dev.html). 

Optimizations Performed <a id="chapter-2"></a>
----------
<table>
<tr><th>Page</th><th>Optimizations</th><th>New PageSpeed Speed Score (Mobile/Desktop)</th></tr>
<tr><td>index.html, project-2048.html, project-webperf.html</td>
<td>
- Optimized all images  
- Inlined CSS and Javascript  
- Minified CSS and Javascript  
- Moved Javascript files to end of mark-up  
- Added "asynch" tag to Google Analytics script
</td>
<td>97/97</td></tr>
<tr><td>project-mobile.html</td>
<td>
- Optimized all images  
- Inlined CSS and Javascript  
- Minified CSS and Javascript  
- Moved Javascript files to end of mark-up  
- Added "asynch" tag to Google Analytics script  
</td>
<td>96/97</td></tr>
<tr><td>views/pizza.html</td>
<td>
- Optimized all images  
- Inlined CSS and Javascript  
- Minified CSS and Javascript  
- Moved Javascript files to end of mark-up  
</td>
<td>95/96</td></tr>
<tr><td>views/js/main.js</td>
<td>
- Minimized DOM updates by consolidating innerHTML  
- Prevented superfluous DOM elements from being rendered  
- See comments on lines 346, 414, 435, 474, 505, 519  
</td>
<td>Consistent FPS of 60+</td></tr>
</table>

Resources Used <a id="chapter-3"></a>
---------
<dl><dt>Google Maps API</dt>
<dd>I used the Google Maps API to create the map that serves as the primary application view in both the desktop and mobile version of the application. I wrote custom Knockout JS binding handlers that link the markers on the map (both search results and favorites) to observable arrays.</dd>  

<dt>Yelp! API</dt>
<dd>Of all the business search APIs I researched, Yelp was my favorite. The Yelp Development Guide recommends creating a server-side script (e.g. in PHP) to handle AJAX calls rather than making calls directly from Javascript, so I wrote a PHP script that the application calls (see the PHP folder in this Github project). I used the Yelp API to retrieve rating, review, and location information about businesses.</dd>

<dt>Open Weather</dt>
<dd>Open Weather is a simple, open-source API that I used to create Weather Widgets for the various neighborhoods. An initial AJAX call (at app start-up) fetches the weather information for each neighborhood from Open Weather. That information is then data-bound to the neighborhood selector (via Knockout) so that the appropriate weather is displayed when the user toggles between neighborhoods.</dd>

<dt>Google Streetview</dt>
<dd>This simple API (which doesn't even require AJAX) was used to add Streetview images for each of the locations in the search and/or favorites arrays.</dd></dl>

Additional Notes <a id="chapter-4"></a>
----------------
Libraries used in this application included:  
- Knockout JS
- jQuery
- Bootstrap

I also learned quite a bit about custom Knockout JS data binding by reviewing [this very helpful article] (http://www.codeproject.com/Articles/351298/KnockoutJS-and-Google-Maps-binding "KnockoutJS and Google Maps Binding").  

Finally, I should note that the Development Guide for the Yelp API encourages developers to use a server-side script (e.g. PHP) rather than Javascript. I followed this advice and created my own PHP script, which I've included in this project (under the PHP folder).  

Because Internet Explorer does not accept cross-origin browser requests, if you want to demo this application in IE you'll need to either (1) install the PHP script on your server (or whichever server you plan to run the project from), or (2) simply use the live link I've provided at the top of this article.

