# blogger
My modified blogger theme
Here is summary of the general workflow of creating a website and how to optimize it *continuously*.

By Reiser Wang

## What To Do When Creating a Site

 1. Decide target audience/UX/business/monetization models
 2. Determine site framework and/or templates
    - Must be mobile-aware. >50% views are now from mobile devices! 
    > [Responsive Web Design (RWD)](https://en.wikipedia.org/wiki/Responsive_web_design)
    > [Accelerated Mobile Pages Project (AMP)](https://www.ampproject.org/) 
    - Scope browser compatiblity and draft test plans
    > [User-Agent Strings](http://www.useragentstring.com/pages/useragentstring.php)
 2. Implement front-end and back-end 
    - Be kind to eyes and brains. Use code formatter (example)[https://www.freeformatter.com/] to make your codes organized.
   - Mind [html encode](https://codebeautify.org/html-encode-string)
 3. Debug/Test
    - Page loading analsysis - find out performance bottleneck by using tools such as [Chrome DevTools](https://developer.chrome.com/devtools) and fix it by moving to local or remove redundent codes.
    - Security
        * Being skeptical - Check every external resources and links and its parameters
 4. Site optimization
	 - [Google Site Speed](https://developers.google.com/speed/pagespeed/insights/)
	 - Server optimization
     > [Set browser caching](https://developers.google.com/speed/docs/insights/LeverageBrowserCaching)

	 - Front-end JavaScript optimization
	 > When setting JavaScript code snippets to 
	 ```html
	 <script async='async' src='//ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js'/>
	 ```
	 >the delay loading of scripts may cause rendering or script execution errors when browser parse the target website while the script is not fully loaded.
	 - Compress [HTML/CSS/JavaScript](https://developers.google.com/speed/docs/insights/MinifyResources)
     - Optmize [CSS delivery](https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery)
	 - Image optimization
 5. Search Engine Optimization (Being corporative - feed preferred and structred data to search engines)
    - [Google Search Console](https://www.google.com/webmasters/tools/home)
    - [Open Graph (og) protocol](http://ogp.me/)
    > **To-Do: Add more SEO tips here.**
6. Social Network Service (SNS) Optmization
    - [Facebook API](https://developers.facebook.com/docs/plugins/share-button)
    - [Twitter API](https://dev.twitter.com/web/tweet-button)
