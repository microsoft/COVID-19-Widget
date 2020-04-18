
# Bing COVID-19 Widget 
As the coronavirus impacts the world, we recognize the need to share the latest information outside of Bing. This widget will allow any site to easily add an outbreak map, the latest case counts, and a chart displaying the spread over time. These elements are modular, giving sites the ability to customize them. 

**By adding the widget to your site, you agree to be subject to the terms of use [listed here](../blob/master/LICENSE)**

## How can I implement the widget on my site?
You will simply need to add two lines of HTML code, a <div> including various widget parameters, and a <script>. At the bottom of this readme are code examples for the various supported configurations. Each configuration is a combination of three supported modules: an **Outbreak Map Module** showing the worldwide spread of the virus, a **Data Stats Module**, which displays the case count information for a given location, and a **Trends Chart Module** showing the spread of the virus in a location over time. 

## How do I select a widget configuration?
You are able to select your widget configuration with the data-type parameter. We support the following values:

| Description   | data-type Parameter |
| --------- |:---------------------:|
| Default – includes all three modules: Outbreak Map module, Trends Chart module, and Data Stats module | covid19 |
| Map – includes only the Outbreak Map module | covid19_map |
| Trends – includes only the Trends Chart module | covid19_trends |
| Stats and Map – includes the Data Stats module and Outbreak Map module | covid19_stats_map |
| Stats and Trends – includes the Data Stats module and Trends Chart module | covid19_stats_trends |


In addition to these data-type options, you can also stack multiple widget on top of each other by including multiple <div> lines and only one <script>. 
	
We are working on an additional data-type that will allow further module customization, but it is not currently available. This will allow you to have multiple sets of the three module types. The documentation will be updated with further instructions when it's available. 

## How do I select the market and language?
The data-market and data-language parameters control the market and language of the widget respectively. The data-market parameter controls the country/region the widget will optimize for. The data-language parameter controls the UI display language in which the widget will display the UI string resources. Typically you will have the data-market and data-language parameters set to the same parameter value, however, there are cases where they would differ. For example, you can have a user in United States who speaks Spanish. In this case you can set the data-market to en-US and the data-language to es-ES. We support the following values for ata-market and data-language:

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
| South Korea | ko-KR |
| Spain | es-ES |
| UK | en-GB |
| US | en-US |


  
| Language   | data--language Parameter |
| --------- |:---------------------:|
| English in Australia | en-AU |
| English in Canada	| en-CA |
| English in India	| en-IN |
| English in | UK 	en-GB |
| English in | US	en-US | 
| French  | 	fr-FR |
| French in Canada  | 	fr-CA |
| German | 	de-DE |
| Italian | 	it-IT |
| Japanese | 	ja-JP |
| Korean | 	ko-KR |
| Spanish | 	es-ES |


## How do I specify a location for the widget to load?
The data-location-id allows you to set location following the format of “/Country/Region.” There are hunderds of valid combinations which can be found in the AllLocation.txt file on the widget GitHub page. 

In the future we plan to also support location selection by latitude and longitude values. 

**By adding the widget to your site, you agree to be subject to the terms of use [listed here](../blob/master/LICENSE)**

## Widget examples

**Widget Default**
```
<div class="bingwidget" data-type="covid19" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget Default - specifying language and market to Japanese in Japan**
```
<div class="bingwidget" data-type="covid19" data-market="ja-jp" data-language="ja-jp"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget with only Map**
See it live [here]()
```
<div class="bingwidget" data-type="covid19_map" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget with only Map - specifying location of Italy**
See it live [here]()
```
<div class="bingwidget" data-type="covid19_map" data-market="en-us" data-language="en-us" data-location-id="/Italy"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget with only Trends**
Se it live [here]()
```
<div class="bingwidget" data-type="covid19_trends" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget with Stats and Map - specifying location of United States**
See it live [here]()
```
<div class="bingwidget" data-type="covid19_stats_map" data-market="en-us" data-language="en-us" data-location-id="/United States"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

**Widget with Stats and Trends, specifying location of Texas**
See it live [here]()
```
<div class="bingwidget" data-type="covid19_stats_trends" data-market="en-us" data-language="en-us" data-location-id="/United States/Texas"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

