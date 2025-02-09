# Stockstir
Instantly and easily gather stock data in real time of any company in any of your Python scripts (V2)

![stockstir-logo](https://github.com/PatzEdi/Stockstir/raw/main/READMEassets/stockstirlogoV2.jpg)

<p align="center">
	<img src="https://img.shields.io/badge/License-MIT-brightgreen"
		height="23">
	<img src="https://img.shields.io/badge/Creator-PatzEdi-brightgreen"
		height="23">
	<img src="https://readthedocs.org/projects/stockstir/badge/?version=latest"
		height="23">
	<img src="https://img.shields.io/badge/Version-Latest-brightgreen"
		height="23">
</p>

## Thank you to the Starrers!
[@rawberg](https://github.com/rawberg), [@z1001123](https://github.com/z1001123), [@soundtrackgeek](https://github.com/soundtrackgeek), [@Giddu](https://github.com/Giddu), [@T31M](https://github.com/T31M), [@somas1](https://github.com/somas1), [@rexzhang](https://github.com/rexzhang), [@arturo-zarzilla](https://github.com/arturo-zarzilla), [@dfd](https://github.com/dfd), [@ArcturusMajere](https://github.com/ArcturusMajere), [@LambertusDekker](https://github.com/LambertusDekker), [@508chris](https://github.com/508chris), [@PandaStacker](https://github.com/PandaStacker), [@piksu](https://github.com/piksu), [@cameronhptdev](https://github.com/cameronhptdev), [@bazfire](https://github.com/bazfire), [@AceofSpades5757](https://github.com/AceofSpades5757), [@georgettica](https://github.com/georgettica), [@LeonardPuettmann](https://github.com/LeonardPuettmann), [@Shrhawk](https://github.com/Shrhawk), [@builderjer](https://github.com/builderjer), [@mikudae](https://github.com/mikudae) 

**Thank you for 20+ Stars!**
If you do not wish to be in the list above, please let me know by either creating an issue or messaging me through reddit (linked on my website https://patzedi.github.io). Also, it may take me a while (depending on the time) to put new stargazers on the README, but it will be done nonetheless :)

## Important Note:
If you would like to see the full changelog of V2 and new features, you can look at the [CHANGELOG.md](/CHANGELOG.md) file.

**Documentation:**
Access the [Stockstir ReadtheDocs Documentation](https://stockstir.readthedocs.io/en/latest/index.html) to explore the features of Stockstir and how to use them, as well as getting to know how Stockstir works in a detailed way. The documentation is now updated to the latest version (V2).

## **Stockstir V2 allows the instant gathering of any stock company value from any of your Python scripts, now with a new fail-safe system with more than one provider, and more features (some yet to come), enhancements, and fixes.** 
____________________________________________________________________________
## **CHANGELOG INFO**
- The changelog for Stockstir starting from December 30, 2023, version 2.0.0 onward, will be stored in the [Changelog](/CHANGELOG.md) file under the project files.

## **Quick Usage**

Installation:
```
pip3 install Stockstir
```

Importing:
```
import Stockstir
```
Simple example to gather stock data from any website:
```
Stockstir.Tools.getSinglePrice("ticker/stockSymbol")
```
Since this library has many more features (too many to explain here in a neat way), you can take a look at the [Documentation](https://stockstir.readthedocs.io/en/latest/index.html) hosted by readthedocs.io.

## **Features**
- With V2, a new fail-safe system and new providers are implemented, as well as other features, enhancements, and fixes.
- Instantly gather stock prices from any company in real time.
- Includes a single price gathering tool to get the price of any company once.
- Includes a multi data gathering tool which has features like anti ban, random user agents, delay for each request, and of course how much data to gather.  
- Useful tools such as getting the trend of the gathered data determining whether the stock price went up, down, or stayed neutral throughout that time period.
- Ability to return the time spent in the total process of gathering the data. This can be useful in order to analyze data and comparing it to the time spent overall. Not only that, but getting the trend also comes with an optional option to get the change between the first and the last value of the gathered data.
- Includes a useful tool to create logs of the data gathered if needed, and does so by writing the data in a neat way to a file at a specified directory of your choice.
- Includes the ability to make requests with random user agents (up to 24 different agents).
- Very easy to use.
- In case you accidentally put the wrong ticker/stock symbol as a parameter, an exception will occur and warns of the incorrect input.
- Fast and efficient, no time to waste. Stockstir will save you time.
- In terms of code... Comments are included to guide you through what the script does. The code is split into four classes: The Tools, Providers, API and the gatherInfo classes. The only ones you really need are under the Tools, Providers, and API classes, as those classes (especially Tools) combine what is in the gatherInfo class to make a complete set of tools.
____________________________________________________________________________
## **Why?**
- Gathering stock data is definitely something that can be useful to many in their Python scripts. 
- Real time stock data can be used to look at a specific price of any company and determine what to do with that data later on. For example, if you wanted to get notified one the price of stock goes above or below a value, it is now easier than ever to do something like that. 
____________________________________________________________________________
## **How?**
- Using many useful libraries (credits below), I was able to get what I needed to make a library like this one. 
- The way it works is very interesting. I basically gathered the source code of the webpage of the providers in the providers dictionary under the Providers class and added to the url of a provider the ticker/stock symbol. I made a request to that URL, got the source code, and created a regex pattern that suited the provider website. I figured out that the regex pattern I used was universal for any company and its source. Using the regex, I could instantly find the value of the price. So overall, this script basically sends a request to the selected provider and analyzes the source in order to gather the price.
____________________________________________________________________________
## **User notice**
- Please be aware that using a rotating IP address (for example a VPN with a rotating IP) could help you not get banned from a provider when making a lot of requests. If you want to use the multi data gathering tool, you can use the anti ban function to try to avoid getting banned from the website and being recognized as a potential "bot" making automatic requests.
- This project is still a work in progress. Adding new features is very easy, but so far I have started with it simple. 
- Please note that the README file briefly goes into the details of how the project works. If you want more in depth details of what each and every function and parameter does, take a look at the [Documentation](https://stockstir.readthedocs.io/en/latest/index.html) file in the project files.
- Also, I am not responsible for any inappropriate use of this library, such as being used for spam or mass-collection purposes.
____________________________________________________________________________
## **Services used (Credits):**
- [Requests module](https://requests.readthedocs.io/en/latest/)
- [URLLib module](https://docs.python.org/3/library/urllib.html)
- [Re module](https://docs.python.org/3/library/re.html)
- [Time module](https://docs.python.org/3/library/time.html)
- [Random module](https://docs.python.org/3/library/random.html)

____________________________________________________________________________
## **Make sure to leave a star!**
- If you like this project, leaving a star is what motivates me in doing more. Thank you, and I hope this is useful in order to gather the stock data you need.
