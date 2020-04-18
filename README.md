
# Bing COVID-19 Widget 

All widget configurations will have two lines of HTML code, a <div> including various parameters, and a <script>. 



## What is the data-type parameter used for?
The data-type parameter sets the widget configuration. There are five options:
Description 	data-type
Parameter
Default – includes all three modules: Outbreak Map module, Trends Chart module, and Data Stats module
	covid19
Map – includes only the Outbreak Map module	covid19_map
Trends – includes only the Trends Chart module
	covid19_trends
	_stats
Stats and Map – includes the Data Stats module and Outbreak Map module
	covid19_stats_map
Stats and Trends – includes the Data Stats module and Trends Chart module

	covid19_stats_trends
	Multiple example

What markets and languages does the widget support?
The data-market and data-language parameters can be customized using these values:

| Country   | data-market Parameter |
| --------- |:---------------------:|
| Australia | en-AU                 |
| Brazil    | pt-BR                 |
| Canada | en-CA |
| Canada | fr-CA |
| China | zh-CN |
| France | fr-FR |
| Germany | de-DE |
| India | en-IN |
| Italy | it-IT |
| Japan | ja-JP |
| Spain | es-ES |
| UK | en-GB |
| US | en-US |


	Language
	data-language Parameter
  
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


How do I specify a location for the widget to load?
The data-location-id id and data-location-latlon are two options you have for specifying which location the widget will load data for. Note that currently only the data-location-id id option is supported. Support for data-location-latlon will be added soon. You only need to set one location parameter, either data-location-id or data-location-latlon. If you set both parameters, the data-location-id will take precedence. When no location is specified, the default data shown is global. 
The data-location-id allows you to set location following the format of “/Country/Region.” There are over 3,000 possible values which can be found in the AllLocation.txt file on the widget GitHub page. 
The data-location-latlon allows you to set location by the latitude and longitude values. Note that data-location-latlon is not yet supported. 

What else can I customize on the widget?
We are working on an additional data-type that will allow further module customization, but it is not currently available. This will allow you to have multiple sets of the three module types. The documentation will be updated with further instructions when it's available. 


This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.

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



