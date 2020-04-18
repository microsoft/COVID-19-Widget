
# Bing COVID-19 Widget 
As the coronavirus impacts the world, we recognize the need to share the latest information outside of Bing. This widget will allow any site to easily add an outbreak map, the latest case counts, and a chart displaying the spread over time. These elements are modular, giving sites the ability to customize them. 

To add the widget to your site, you must first agree to the terms of use [listed here](../blob/master/LICENSE)


## How can I implement the widget on my site?
To add the widget to your site, you must first agree to the terms of use here. Then you'll just need to add two lines of HTML code. All widget configurations will have two lines of HTML code, a <div> including various parameters, and a <script>. 

## Widget examples

<b>Widget Default</b>
```
<div class="bingwidget" data-type="covid19" data-market="en-us" data-language="en-us" data-aop="bingwidget"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

<b>Widget with only Map</b>
```
<div class="bingwidget" data-type="covid19_map" data-market="en-us" data-language="en-us" data-aop="bingwidget" data-location-latlon="48.84,-43.59"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```


<b>Widget with only Trends</b>
```
<div class="bingwidget" data-type="covid19_trends" data-market="en-us" data-language="en-us" data-aop="bingwidget"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

<b>Widget with Stats and Map</b>
```
<div class="bingwidget" data-type="covid19_stats_map" data-market="en-us" data-language="en-us" data-aop="bingwidget" data-location-id="/United States/New York"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```


<b>Widget with Stats and Trends</b>
```
<div class="bingwidget" data-type="covid19_stats_trends" data-market="en-us" data-language="en-us" data-aop="bingwidget" data-location-id="/United States/New York" data-location-latlon="48.84,-43.59"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```





## What is the data-type parameter used for?
The data-type parameter sets the widget configuration. There are five options:

| Description   | data-type Parameter |
| --------- |:---------------------:|
| Default – includes all three modules: Outbreak Map module, Trends Chart module, and Data Stats module | covid19 |
| Map – includes only the Outbreak Map module | covid19_map |
| Trends – includes only the Trends Chart module | covid19_trends |
| Stats and Map – includes the Data Stats module and Outbreak Map module | covid19_stats_map |
| Stats and Trends – includes the Data Stats module and Trends Chart module | covid19_stats_trends |


In addition to these data-type options, you can also stack multiple widget on top of each other by including multiple <div> lines and only one <script>. 


	
## What markets and languages does the widget support?
The data-market and data-language parameters can be customized using these values:

| Country   | data-market Parameter |
| --------- |:---------------------:|
| Australia | en-AU                 |
| Canada | en-CA |
| Canada | fr-CA |
| France | fr-FR |
| Germany | de-DE |
| India | en-IN |
| Italy | it-IT |
| Japan | ja-JP |
| Spain | es-ES |
| UK | en-GB |
| US | en-US |


  
| Language   | data--language Parameter |
| --------- |:---------------------:|
| English in | Australia	en-AU |
| English in Canada	| en-CA |
| English in India	| en-IN |
| English in | UK 	en-GB |
| English in | US	en-US | 
| French  | 	fr-FR |
| German | 	de-DE |
| Italian | 	it-IT |
| Japanese | 	ja-JP |
| Korean | 	ko-KR |
| Spanish | 	es-ES |


## How do I specify a location for the widget to load?
The data-location-id id and data-location-latlon are two options you have for specifying which location the widget will load data for. Note that currently only the data-location-id id option is supported. Support for data-location-latlon will be added soon. You only need to set one location parameter, either data-location-id or data-location-latlon. If you set both parameters, the data-location-id will take precedence. When no location is specified, the default data shown is global. 
The data-location-id allows you to set location following the format of “/Country/Region.” There are over 3,000 possible values which can be found in the AllLocation.txt file on the widget GitHub page. 
The data-location-latlon allows you to set location by the latitude and longitude values. Note that data-location-latlon is not yet supported. 

## What else can I customize on the widget?
We are working on an additional data-type that will allow further module customization, but it is not currently available. This will allow you to have multiple sets of the three module types. The documentation will be updated with further instructions when it's available. 


All widget configurations will have two lines of HTML code, a <div> including various parameters, and a <script>.

