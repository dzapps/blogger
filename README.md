# Responseive Blogger Theme with search engine and social network optimizations
## 
My modified blogger theme based on [Simmplify Responsive Blogger Template] (https://www.arlinadzgn.com/2016/06/simplify-2-responsive-blogger-template.html)

While optimizing the template, I put some notes here for what has been done for optmizations, and hopefully ends up it becomes a summary of general workflows and references for website optmizations.

> By Reiser Wang under [Apache License 2.0](https://github.com/reiserwang/blogger/blob/master/LICENSE)


- [Responseive Blogger Theme with search engine and social network optimizations](#responseive-blogger-theme-with-search-engine-and-social-network-optimizations)
    - [What To Do When Creating a Site](#what-to-do-when-creating-a-site)
        - [1. Decide target audience/UX/business/monetization models](#1-decide-target-audienceuxbusinessmonetization-models)
        - [2. Determine site framework and/or templates](#2-determine-site-framework-andor-templates)
            - [2.2 [RWD](https://en.wikipedia.org/wiki/Responsive_web_design)](#22-rwdhttpsenwikipediaorgwikiresponsivewebdesign)
            - [2.3 [AMP](https://www.ampproject.org/)](#23-amphttpswwwampprojectorg)
        - [3. Implement front-end and back-end](#3-implement-front-end-and-back-end)
        - [4. Debug/Test](#4-debugtest)
            - [Page loading analysis](#page-loading-analysis)
            - [Security](#security)
        - [5. Site optimization](#5-site-optimization)
            - [[Google Site Speed](https://developers.google.com/speed/pagespeed/insights/)](#google-site-speedhttpsdevelopersgooglecomspeedpagespeedinsights)
        - [6. Search Engine Optimization](#6-search-engine-optimization)
        - [7. Social Network Service (SNS) Optmization](#7-social-network-service-sns-optmization)

===
## What To Do When Creating a Site

### 1. Decide target audience/UX/business/monetization models
---
### 2. Determine site framework and/or templates
####2.1 Must be mobile-aware. >50% views are now from mobile devices!
#### 2.2 [RWD](https://en.wikipedia.org/wiki/Responsive_web_design)
#### 2.3 [AMP](https://www.ampproject.org/) 

Better to select * a template designed for AMP. The imgration from non-AMP to AMP may be a pain.

####2.4 Scope browser compatibility and draft test plans

[User-Agent Strings](http://www.useragentstring.com/pages/useragentstring.php)
    
 ---
### 3. Implement front-end and back-end 
- Be kind to eyes and brains. Use code formatter (example)[https://www.freeformatter.com/] to make your codes organized.
- Mind [html encode](https://codebeautify.org/html-encode-string)
 ---
### 4. Debug/Test
#### Page loading analysis

- Find out performance bottleneck by using tools such as [Chrome DevTools](https://developer.chrome.com/devtools) and fix it by moving to local or remove redundent codes.

#### Security

- Being skeptical - Check every external resources and links and its parameters
 ---
### 5. Site optimization
#### [Google Site Speed](https://developers.google.com/speed/pagespeed/insights/)

 **Some tricks**
 - Blogger automatically inserts widget_css_mobile_bundle.css that causes warning in [Google Page Speed Insights](https://developers.google.com/speed/pagespeed/insights/). To workaround it simply change 

``html
<head>
* YOUR HTML HERE *
</head>
```

to
            

```html
&lt;head&gt;
* YOUR HTML HERE
&lt;/head&gt;&lt;!--<head/>--&gt;
 ```


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
 ---
### 6. Search Engine Optimization 
    *Being corporative - feed preferred and structred data to search engines*
    - [Google Search Console](https://www.google.com/webmasters/tools/home)
        * Sitemap
        * [Structured Data](https://developers.google.com/search/docs/guides/intro-structured-data?) and Google [testing tool](https://search.google.com/structured-data/testing-tool））
        * [AMP](https://www.ampproject.org/docs/tutorials/create) [test tools](https://search.google.com/test/amp)
    - [Open Graph (og) protocol](http://ogp.me/) 
    > **To-Do: Add more SEO tips here.**
---
### 7. Social Network Service (SNS) Optmization
    - [Facebook API](https://developers.facebook.com/docs/plugins/share-button)
    - [Twitter API](https://dev.twitter.com/web/tweet-button)
    - [Line share button](https://media.line.me/en/how_to_install)
    - Make every page perfectly shareable by setting [Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters) and tested by SNS tools such as [Facebook](https://developers.facebook.com/docs/sharing/webmasters#testing)

    ```html
    <meta property="og:url"                content="https://ducalacafe.blogspot.tw/search/label/%E6%97%85%E9%81%8A?&max-results=7" />
    <meta property="og:type"               content="article" />
    <meta property="og:title"              content="Ducala's travel post" />
    <meta property="og:description"        content="Ducala's travel inforamtion?" />
    <meta property="og:image"              content="https://4.bp.blogspot.com/_fE69UaYHfCI/SkDyNrUfwPI/AAAAAAAAA0o/Fn8fk-KXjY8/S220/happydog.jpg" />
    ```

    This should be part of your publishing processes.
