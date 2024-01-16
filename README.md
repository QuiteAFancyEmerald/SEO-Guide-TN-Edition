# Holy Unblocker & Titanium Network SEO Guide
## Competitive Search Engine Optimization is a powerful skillset to learn. 

> **Created By Quite A Fancy Emerald, creator of Holy Unblocker a past popular web service with over 15M+ users monthly and zero sponsors**


This README goes through core concepts discovered through hosting various web proxy open-source projects.

## Table Of Contents:

- [Introduction](#introduction)
    - [Getting Started](#starting-steps)
        - [Sitemap Example](#sitemap-example)
        - [NGINX Example](#nginx-example)
    - [Source Structure](#source-structure)
      - [Overview](#overview)
      - [Head Tag SEO](#head-tag-seo)
      - [Navbar SEO](#body-tag-seo---navbar)
      - [Content SEO](#body-tag-seo---content)
      - [Footer SEO](#body-content-seo---footer--socials)
    - [Credits](#credits)

## Introduction

Want to create and maintain a popular proxy website? Or just a website in general and/or have almost near perfect visibility across search engines and easy discovery to a discord server?

Before we even BOTHER with the source you need to understand where to look. First off to those who are worried about SEO and web proxies hosting with keyword concerns (keywords can be used to source block); YOU NEED TO only apply this to an official domain. Do you really think you can have thousands of domains retain equal SEO? No. 

The idea is this: 

- First create a way to serve a SEO source to your official domain that ENDS in .net/.dev/.com/.org/.co (if your domain does not use these TLDs forget about getting good SEO. .app is possible but harder unless if you host a popular site)
- This serving can be done either through server-side functions by well checking if the domain is the official site and serving up the exclusive SEO source, considering fancy str.replace methods (cough cough source randomization) or well straight up have two sources that you host separately

**Source Randomization:** https://github.com/QuiteAFancyEmerald/Holy-Unblocker/blob/master/src/randomization.mjs

You might ask is this worth it? Wouldn't this be harder to maintain or setup? Well sadly if you wish to utilize competitive Search Engine Optimization you need to apply one of the serving methods in order to have a perfect source where you don't need to worry about keywords. Your official domain is going to get blocked almost instantly BUT it still serves as a gateway to your backlinks such as documentation, discord, social media and GitHub. It creates massive popularity. You might even ask yourself who is going to search this up? PEOPLE will search and SEO influences so much more than your classic distribution.

## Starting Steps

1) Create a search console account for Google: https://search.google.com/search-console/about
     Google should be your priority. You first need to actually get your site indexed and understand what Google is looking for. This tool will TELL you everything you need to know. Sure you will need to nerd about a bit but the steps below will make more sense once you see this console. On the actual console page ENSURE to type out the absolute path to index; example is "https://holyunblocker.net/" with your fancy /. Do this for every single page with the URL Inspection tool. Remember your paths need to be server side not straight up markdown files. Check the performance tab once your site gains users to see if your keywords and well below you will see if your descriptors are leaving good impressions on Google. With good SEO you should hold a spot from either 1-6.

---

2) Create a webmasters account for Bing: https://www.bing.com/webmasters/about
    Same concept above but for Bing. Bing is a bit more uh basic therefore focus on Google. Bing tends to eat off it anyways. Ensure that your source specifically with both NGINX and the actual source specifies Bing if you care more about it. Remember though less users. Regardless Bing tends to be a lot less picky when compared to Google. Everything from rich results, etc. is easier. Remember Bing is used by many search engines such as DuckDuckGo

---

3) Read over creating SCHEMAs JSON Modals: 

    Want to understand how to create "rich snippets" or results on Google? This is how. I am talking about those FAQ questions or fancy structures that you see for massive sites linking to other pages or just having questions. YOU can control it all. There are core attributes and structure priorities that you must follow. I give examples in my source below and consider re-using it. Use the rich results tool Google provides to test how it looks
   
   **Schemas:** https://schema.org/docs/schemas.html 
   
   **3b:** https://developers.google.com/search/docs/appearance/structured-data/search-gallery 
   
   **Test Schema:** https://search.google.com/test/rich-results

---

4) Create robots.txt and ensure its routed correctly: https://yoast.com/ultimate-guide-robots-txt/
    Touching into creating a source console account you will notice this is frequently talked about. You need to specify specific paths and also block paths. DONT JUST WHITELIST EVERYTHING. All search engines care about detailed robots.txt files. Will it downrank you? No but having a solid understanding of user agents give you an edge over the majority of basic sites.  

**Read over popular user agents:** https://www.whatismybrowser.com/guides/the-latest-user-agent/

---

5) Create a properly formatted sitemap even with poor paths but consider RICH paths for your service
   
    For this I could type out a guide but that is rather unneeded. I will instead upload an example. Notice how I specify the priority of content rich pages of importance that way Google or Bing can understand and create "Rich Results" better. Sometimes Google will ignore this however it is apart of the old web but still an essential SEO resource to have. This file will be in your root directory for served content. You will submit this to the Search Console for both Google and Bing.
   
**5a:** https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap 
   
**5b:** https://www.seerinteractive.com/insights/how-to-create-and-submit-a-xml-sitemap

---
### Sitemap Example
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset
      xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9
            http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd">
<!-- created with Free Online Sitemap Generator www.xml-sitemaps.com -->


<url>
  <loc>https://holyubofficial.net/</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>1.00</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/proxies</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.90</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/faq</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.90</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/documentation</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.90</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/games</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.80</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/youtube</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.80</priority>
  <changefreq>weekly</changefreq>
</url>
<url>
  <loc>https://holyubofficial.net/example</loc>
  <lastmod>2021-03-14T17:04:57+00:00</lastmod>
  <priority>0.80</priority>
  <changefreq>weekly</changefreq>
</url>

(keep going and list it ALL. every single page but remember to change the priority or the frequency tag as needed depending on how often you update your source or do cache purges.)

</urlset>
```


---

6) Creating and maintaining backlinks: Below I will provide source linking examples. Think about a spider web. You don't want just your site top ranking but the entire spider web on that Google/Bing page

    Before we even start touching the source you need to make sure you have some sort of social media accounts made as well as documentation. Having your project open-source is one of the easiest ways to maintain backlinks. Ensure your README is in-depth and full of important descriptors. Provide screenshots or even videos of your service this will all be indexed. Google and Bing will naturally take any GitHub results and index them building up your backlinks. Create social media accounts and upload on them. Or don't just ensure the descriptors are unique enough and link it on your README. THIS IS ESSENTIAL. If you don't do this you might as well be wasting your time with all these keyword changes. Without backlinks you cannot have a popular service.

Useful backlinks: GitHub, Docusaurus on a subdomain like "docs", Patreon account, YouTube account, Twitter account, Open Collective account, XDA Forums post, Quora post, Discord server with vanity or non-vanity, credible sponsors such as Medium or organizations, other projects on GitHub or wikis with your unique project name or optimized official site (optimized as in source)

**6a:** https://docusaurus.io/


---

7) Understanding Cache fundamentals and timestamping assets: 
   
```javascript
<script type="text/javascript" src="/somefile.js?123456789"></script>
```

Below I will example the importance of basic web security setup. TTL cache is a core metric for search engines to both crawl any updated content you have but also index faster. Save yourself and your users pain by ensuring your assets update fast enough. Markdown (HTML) will be nearly instant but stylesheets and other scripts will take time. That is where timestamping comes into play.

For my example I forced all my caching to Cloudflare which acted as my CDN by specifying the proxy_cache_bypass directive with NGINX. You can however use a different CDN or cache everything on your own server if you have a nice instance. Utilize the gzip directive fully.

**Cloudflare:** https://developers.cloudflare.com/cache/how-to/cache-rules/

**GZIP NGINX:** https://www.digitalocean.com/community/tutorials/how-to-improve-website-performance-using-gzip-and-nginx-on-ubuntu-20-04


---

8) Maintain a properly distributed NGINX reverse proxy setup and correct directives (will provide examples):

 THIS IS SUPER IMPORTANT. I'm talking **HTTP2, TLS, SSL, SECURITY HEADERS, ADDED HTTP HEADERS**

First off use NGINX and if you wish you can use CF for caching or whatever CDN. Maintain NGINX as your initial reverse proxy setup however. A lot of people don't understand the importance of modern web security and how Google or Bing actually account for this. They check for specific security headers, proper TLS/SSL settings and fingerprinting. Above and below I am providing various examples for what you should consider adding as well as my own server example from when I was hosting Holy Unblocker
   
**8a:** https://medium.com/@oryaacov/how-to-setup-a-secured-http-server-using-nginx-c7d8e85815a

**8b:** https://github.com/stylersnico/nginx-secure-config/blob/master/nginx.conf

**8c:** https://www.nginx.com/blog/improve-seo-https-nginx/

**8d:**  https://serverfault.com/questions/977825/setting-noindex-some-pages-on-nginx (think opposite on this)
  
**8e:** https://undabot.com/blog/how-to-boost-performance-and-technical-seo-just-by-tuning-nginx/

---

### Nginx Example
My source. I realize this is a wall but I actually commented out every essential thing you could possibly need. This is also good structure for those wanting a fast reverse proxy setup. I include all SEO essential nginx directives. I also include error pages. Note my formatting. Error pages are essential as well although I could not tell you the SEO impact it allows for a more rich server setup.
  
```nginx
 ##### Default Settings #####
    include /etc/nginx/mime.types;
    default_type application/octet-stream;
    map_hash_bucket_size 128;
    resolver 1.1.1.1;

	
    # Logging is very lame
    access_log off;
    error_log off;
    sendfile on;

    include /etc/nginx/conf.d/*.conf;
    include /etc/nginx/conf.d/blocklist.conf;

    limit_req_zone $binary_remote_addr zone=limitreq:20m rate=30r/s;
    limit_req zone=limitreq burst=500 nodelay;
    limit_req_status 444;
    limit_conn_zone $binary_remote_addr zone=limitconn:20m;
    limit_conn limitconn 10;

    # Optimize the amount of data that is being sent at once. Prevent Nginx from sending a partial frame. As a result it will increases the
    # throughput, since TCP frames will be filled up before being sent out.
    # You also need to activate the `sendfile` option.
    tcp_nopush on;

    # By default, the TCP stack implements a mechanism to delay sending the
    # data up to 200ms. To force a socket to send the data in its buffer
    # immediately we can turn this option on.
    tcp_nodelay on;

    reset_timedout_connection on;

    gzip on;
    
    # Gzip compression level (1-9).
    # 5 is a perfect compromise between size and CPU usage, offering about
    # 75% reduction for most ASCII files (almost identical to level 9).
    gzip_comp_level 5;

    # Don't compress a small file that is unlikely to shrink much. The small
    # file is also usually ended up in larger file sizes after gzipping.
    gzip_min_length 256;

    # Compress data even for a proxied connection.
    gzip_proxied any;

    # Cache both the regular and the gzipped versions of a resource whenever
    # client's Accept-Encoding capabilities header varies.
    gzip_vary on;

    # Compress all of the following mime-types, `text/html` is always
    # compressed.
    gzip_types
        application/atom+xml
        application/javascript
        application/json
        application/ld+json
        application/manifest+json
        application/rss+xml
        application/vnd.geo+json
        application/vnd.ms-fontobject
        application/x-font-ttf
        application/x-web-app-manifest+json
        application/xhtml+xml
        application/xml
        font/opentype
        image/bmp
        image/svg+xml
        image/x-icon
        text/cache-manifest
        text/css
        text/plain
        text/vcard
        text/vnd.rim.location.xloc
        text/vtt
        text/x-component
        text/x-cross-domain-policy;

	# websocket headers
    map $http_upgrade $connection_upgrade {
        default Upgrade;
        '' close;
    }

	# example for adding a universal header. you can remove this lmao
	add_header Service-Worker-Allowed /;

    upstream servermain {
        server 127.0.0.1:8078 weight=1;
    }

    upstream serverloadbalancealtorproxiesorwhatever {
        #server 127.0.0.1:6969 weight=2;
        server 127.0.0.1:6970 weight=2;
		#server 127.0.0.1:6971 weight=3;
        #server example.com:8080 weight=4;
    }

	########################
	#### EXAMPLE ####
	########################

    #### HTTP Server ####

	#### ENSURE ALL HTTP IS UPGRADED TO HTTPS ####
    server {
        listen 80;
        server_name holyubofficial.net www.holyubofficial.net;
        return 301 https://$host$request_uri;
    }

    server {
        listen 443 ssl http2;
        server_name holyubofficial.net www.holyubofficial.net;

        ### SSL Settings ###
        ssl_certificate /etc/letsencrypt/live/hutaocdn.net/fullchain.pem;
        ssl_certificate_key /etc/letsencrypt/live/hutaocdn.net/privkey.pem;

        #ssl_protocols TLSv1.2 TLSv1.3;
        #ssl_ciphers "EECDH+ECDSA+AESGCM EECDH+aRSA+AESGCM EECDH+ECDSA+SHA384 EECDH+ECDSA+SHA256 EECDH+aRSA+SHA384 EECDH+aRSA+SHA256 EECDH+aRSA+RC4 EECDH EDH+aRSA HIGH !RC4 !aNULL !eNULL !LOW !3DES !MD5 !EXP !PSK !SRP !DSS";
        #ssl_prefer_server_ciphers on;
        #ssl_dhparam  /etc/nginx/ssl/dhparams.pem;

        ### Options ###
        server_tokens off;

        location / {
            proxy_pass http://holyubofficial;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection $connection_upgrade;
            proxy_set_header Host $host;
            
            ### I leave the cache options to CF. You can cache here also. These are all performance options ###
            proxy_cache_bypass $http_upgrade;
            # fix "upstream sent too big header/body"
            proxy_buffer_size 16k;
            # proxy_buffer_size + 8k
            proxy_busy_buffers_size 24k;
            # numOfBuffers * bufferSize >= proxy_buffer_size
            proxy_buffers 4 16k; 
            # client can only upload files less than 100M
            client_max_body_size 100M;

            proxy_read_timeout 120s;

            ## Security Settings. These are crazy essential for SEO. Look these up to understand what they do
            add_header X-Robots-Tag "googlebot: all";
            add_header X-Robots-Tag "bingbot: all";
            add_header X-Robots-Tag "none";
            add_header X-XSS-Protection "1; mode=block";
            add_header X-Content-Type-Options "nosniff";
            add_header Content-Security-Policy "default-src 'self'; connect-src *; font-src *; frame-src *; img-src * data:; media-src *; object-src *; script-src * 'unsafe-inline' 'unsafe-eval'; style-src * 'unsafe-inline';";
            add_header Strict-Transport-Security "max-age=31536000;" always;

            # Google and Bing will care about referers. This prevents other NSFW or misconduct sites from having SEO impacts when linking to your site. Example someone uh doing bad stuff on your proxy or a bad site with an anchor. Google is smart enough to know with this referer that your site is trustworth and what site is doing misconduct
            if ( $http_referer ~* (babes|forsale|girl|jewelry|love|nudit|organic|poker|porn|sex|teen) ) {
               return 403;
            }
        }

        ### Error Pages ###
        error_page 500 502 503 504 521 =400 @proxy_down;
        location @proxy_down {
            add_header Content-Type text/html;
            default_type text/html;
            return 400 '<!DOCTYPE html><html><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no"><title>H&#8203;oly Unb&#8203;loc&#8203;ke&#8203;r | Error</title><meta name="description" content="Get past internet cen&#8203;sorsh&#8203;ip today! Enjoy safer, private internet access bypa&#8203;ssi&#8203;ng filters such as Securly or iboss. Supports Di&#8203;sc&#8203;or&#8203;d and more! :D" /><link rel="icon" type="image/png" sizes="32x32" href="/assets/img/i.png"><link rel="preconnect" href="https://fonts.googleapis.com"><link rel="dns-prefetch" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://arc.io"><link rel="dns-prefetch" href="https://arc.io"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700,400italic"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat+Alternates"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Titillium+Web:400,600,700"><link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous"> <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"></script> <script async src="https://arc.io/widget.min.js#2BzvQ1em"></script> </head><body> <span style=display:none data-cooking=cooks>Boost your confidence in the kitchen with our trusted tips, tricks and expert advice to master the basics and build upon your existing cooking skills and knowledge.</span><div class="text-center" style="margin: 10%;"><h1>502 Error</h1><h4>Sorry, might be doing some maintenance or the entire site is down.</h4><h5 style="padding: 1%;">Possible Solutions:</h5><p>If you are u<wbr>sing Stea<wbr>lth mode try right-clicking the page and doing "Rel<wbr>oad Fram<wbr>e" or simply re<wbr>load the page a few times (Around five times at the max, takes a bit sometimes).</p><p>In the case of ma<wbr>intenan<wbr>ce, please wait for the issue to be resolved. If the issue persists be sure to mention this in the Ti<wbr>ta<wbr>nium Net<wbr>work Dis<wbr>cor<wbr>d.</p><p>Be su<wbr>re to View the F<wbr>AQ page also if you have any quest<wbr>ions. Holy Unb<wbr>lock<wbr>er updates often so it is most likely a temporary issue.</p> <br><h5>More Details:<p>${request_method} ${uri}\n\upstream returned ${upstream_status}\n\connection lasted for ${upstream_connect_time}</p></h5></div><div class="footer-dark ft-bg" style="margin-top: 5%;"> <footer><div class="container"><div class="row"><div class="col-md-6 item text"><h3><a href="#">Ho<wbr>ly Unb<wbr>loc<wbr>ker</a></h3><p>Made by Stud<wbr>ents, For Stu<wbr>dents.&nbsp;</p><p class="copyright">Holy U<wbr>nblo<wbr>cke<wbr>r © 2021</p></div></div></div> </footer></div></body></html>';
        }

        error_page 401 403 @proxy_authbot;
        location @proxy_authbot {
            add_header Content-Type text/html;
            default_type text/html;
            return 400 '<!DOCTYPE html><html><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no"><title>H&#8203;oly Unb&#8203;loc&#8203;ke&#8203;r</title><meta name="description" content="G&#8203;et p&#8203;ast in&#8203;te&#8203;r&#8203;net ce&#8203;n&#8203;s&#8203;or&#8203;sh&#8203;ip tod&#8203;a&#8203;y!:D"><link rel="icon" type="image/png" sizes="32x32" href="/assets/img/i.png"><link rel="preconnect" href="https://fonts.googleapis.com"><link rel="dns-prefetch" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://unpkg.com"><link rel="dns-prefetch" href="https://unpkg.com"><link rel="preconnect" href="https://arc.io"><link rel="dns-prefetch" href="https://arc.io"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700,400italic"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat+Alternates"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Titillium+Web:400,600,700"><link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous"> <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"></script> <script async src="https://arc.io/widget.min.js#2BzvQ1em"></script> </head><body> <span style=display:none data-cooking=cooks>Boost your confidence in the kitchen with our trusted tips, tricks and expert advice to master the basics and build upon your existing cooking skills and knowledge.</span><div class="text-center" style="margin: 15%;"><h1>401 Error | Authorization Required</h1><p>Please access this page from the official site or view the <a href="#">FAQ page</a> for help.</p><p>This mainly serves as bot protection. Navigating to this page through the official site will resolve this.</p></div><div class="footer-dark ft-bg" style="margin-top: 5%;"> <footer><div class="container"><div class="row"><div class="col-md-6 item text"><h3><a href="#">Ho<wbr>ly Unb<wbr>loc<wbr>ker</a></h3><p>Made by Stud<wbr>ents, For Stu<wbr>dents.&nbsp;</p><p class="copyright">Holy U<wbr>nblo<wbr>cke<wbr>r © 2021</p></div></div></div> </footer></div></body></html>';
        }

        error_page 404 @proxy_pagenotfound;
        location @proxy_pagenotfound {
            add_header Content-Type text/html;
            default_type text/html;
            return 400 '<!DOCTYPE html><html><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no"><title>H&#8203;oly Unb&#8203;loc&#8203;ke&#8203;r | Error</title><meta name="description" content="Get past internet cen&#8203;sorsh&#8203;ip today! Enjoy safer, private internet access bypa&#8203;ssi&#8203;ng filters such as Securly or iboss. Supports Di&#8203;sc&#8203;or&#8203;d and more! :D" /><link rel="icon" type="image/png" sizes="32x32" href="/assets/img/i.png"><link rel="preconnect" href="https://fonts.googleapis.com"><link rel="dns-prefetch" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://unpkg.com"><link rel="dns-prefetch" href="https://unpkg.com"><link rel="preconnect" href="https://arc.io"><link rel="dns-prefetch" href="https://arc.io"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700,400italic"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat+Alternates"><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Titillium+Web:400,600,700"><link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous"> <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"></script> <script async src="https://arc.io/widget.min.js#2BzvQ1em"></script> </head><body> <span style=display:none data-cooking=cooks>Boost your confidence in the kitchen with our trusted tips, tricks and expert advice to master the basics and build upon your existing cooking skills and knowledge.</span><div class="text-center" style="margin: 15%;"><h1>404 Error</h1><p>Might be doing some maintenance or the web server is down.</p><p>In that case wait a bit until it is resolved.</p> <br><p>Invalid URL? View the <a href="#">FAQ page</a> for help!</p></div><div class="footer-dark ft-bg" style="margin-top: 5%;"> <footer><div class="container"><div class="row"><div class="col-md-6 item text"><h3><a href="#">Ho<wbr>ly Unb<wbr>loc<wbr>ker</a></h3><p>Made by Stud<wbr>ents, For Stu<wbr>dents.&nbsp;</p><p class="copyright">Holy U<wbr>nblo<wbr>cke<wbr>r © 2021</p></div></div></div> </footer></div></body></html>';
        }

        ### Deny Access ###
        location ~ /\.ht { 
        # deny access to .htaccess files, if Apache's document root
        # concurs with nginx's one
            deny all;
        }

    }
    
}
  
```

---

## Source Structure

### Overview
Having rich and well structured served web content is obviously one of the most important factors for Search Engine Optimization on top of optimized server-side changes and the starting steps above. This section will be split into both the core head tag structuring and body tag.

Below I list out your primary focuses as well as tricks I have learned along the way. Perhaps seeing is better than reading so I also provide my entire optimized source with explainations:

---

- **Rich Keywords** -
 
  Not the keywords meta name attribute but actually ensuring the majority your site has relevant keywords related to the description meta name attribute. Consider actually looking up some of these keywords and viewing what other sites use for this section or note competitor keyword usage on their sites. Consider using the example above if your service shares a similar niche.

  Notice the parallel keywords throughout my examples below. Currently in 2024, most search engines will ignore the keywords name attribute but it does have an impact on some search engines still and general structure. You want that universal ease for both Google, Bing and whatever. For the description I ensured that it would actually embed properly on both Google and Bing. Usually 150 characters or so.

---

- **Readable Structure** -

You are not using a framework that makes things unreadable. I hope not. Regardless these factors still apply. Have your served content be clean enough to read that way you can actually focus on the richness of included keywords. You want your site to be as textbook as possible source wise.

---

- **Accessibility** - 
  
  Google in particular (your primary focus) cares big time about accessibility. This factor you could argue is actually probably the second most important thing with this entire guide. Google will rank your site poorly if it suffers any language or readability issues. This entire area includes font size, CLS (Content Layout Shifts), source by the book responsiveness, etc. I will explain below that you can kinda "cheat" following regulations on mobile support HOWEVER having real mobile support is naturally great for a popular service.
  
  A very good tool to use for this is actual Google's own Page Insights utility or Lighthouse. Utilize both to your liking.

---

- **Performance** - 

Notice the optimization throughout the source. Leave animations to frameworks or JavaScript as most modern browsers are not very performant with CSS animations or keyframes. Keep things clean and minimal. This is a strong metric for Google search ranking. If your site is laggy or has network issues consider a proper hosting provider and/or a CDN. Lightspeed and generic devtools is a good way to analyze the paint time for your entire site and breakdown which assets are causing issues. Remember core practices such as always ensuring fonts are hosted on external CDNs and other similar assets.

---
  
- **Overall Sitemap** -
  
  This guide is not just saying you need this file or saying you need to organize your project folders in a certain way. It doesn't matter if this is done with nginx or whatever although have folder paths is preferable on google. (Still organize however) 
  
  By sitemap this guide talks about how you link to other pages on your navbar. Your navbar is incredibly important for actually contributing to the other pillars above. You want each page to retain the same readable structure and accessibility *but* need to ensure you switch up core keywords to give google a reason to index this page. Example is having descriptions separating the web proxies page from the home page or games page blah blah. You get it. 
  
  This overall connects back to readable structure with using the h1, h2, and so forth tags. Your core HTML tags are favored more by search engines in comparison over CSS structuring when it comes to markdown. Ensure you utilize these tags but still feel free to depend on CSS for every other design factor.

---

### Head Tag (SEO)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    
    <!-- Classic Accessibility-->
    <meta content="IE=edge" http-equiv="X-UA-Compatible" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no">
    <meta content="1.0.10" name="version" />
    <meta name="theme-color" media="(prefers-color-scheme: dark)" content="#434c5e">
    
    <!-- Consider Google Focus; Don't neglect Bing however source wise Bing will leech off Google -->
    <meta name="googlebot" content="index, follow, snippet" />
    <link rel="canonical" href="https://holyunblocker.net/" />
    
    <!-- Modern search engines don't care; Note modern ;D  -->
    <meta name="keywords" content="proxy, web proxy, unblock websites, unblock chromebook, free web proxy, proxy list, proxy sites, un block chromebook, online proxy, proxy server, proxysite, proxy youtube, bypass securly, bypass iboss, bypass lightspeed filter, holy unblocker, chromebooks, titanium network, unblock youtube, youtube proxy, unblocked youtube, youtube unblocked">
    <title>Holy Unblocker</title>
    <meta name="description" content="Holy Unblocker is a secure web proxy service with support for many sites. Bypass filters and freely enjoy a safer private browsing experience or unblock websites on devices such as Chromebooks and at places like school or work without downloading anything."
    />

	<!-- Embed Properties; readable rich structure. Notice my descriptor switches -->
	<meta property="og:site_name" content="Holy Unblocker">
	<meta property="og:url" content="https://holyunblocker.net/">
	<meta property="og:title" content="Holy Unblocker">
	<meta property="og:type" content="website">
	<meta property="og:description" content="Holy Unblocker is a web proxy service that helps you access websites that may be blocked by your network or browser. It does this securely and with additional features.">
	<meta property="og:image" content="/img/embedthingy.png">
	<meta property="og:image:secure_url" content="/img/embedthingy.png">
	<meta property="twitter:image" content="/img/embedthingy_alt.jpg">
	<meta name="twitter:site" content="@HU">
	<meta name="twitter:creator" content="@HU">
	<meta name="twitter:card" content="summary_large_image">
	<meta name="twitter:title" content="Holy Unblocker">
	<meta name="twitter:description" content="Holy Unblocker, an official flagship Titanium Network site, can bypass web filters regardless of whether it is an extension or network-based. Being a secure web proxy service, it supports numerous sites while being updated frequently and concentrating on detail with design, mechanics, and features.">
	
	<!-- Assets; readable rich structure -->
	<link rel="icon" type="image/png" href="[favicon.png](view-source:https://hutao.dev/favicon.png)">
	<link rel="apple-touch-icon" sizes="180x180" href="[apple-touch-icon.png](view-source:https://hutao.dev/apple-touch-icon.png)">
	<link rel="icon" type="image/png" sizes="32x32" href="[favicon-32x32.png](view-source:https://hutao.dev/favicon-32x32.png)">
	<link rel="icon" type="image/png" sizes="16x16" href="[favicon-16x16.png](view-source:https://hutao.dev/favicon-16x16.png)">
	<link rel="mask-icon" href="[safari-tab.svg](view-source:https://hutao.dev/safari-tab.svg)" color="#b4213b">
	
	<!-- Google loves manifest support even if it doesn't matter. Also note how I focus on internal same origin assets first then external after. It matters -->
	<meta name="msapplication-TileColor" content="#b4213b">
	<link rel="stylesheet" href="[css/styles.css](view-source:https://hutao.dev/css/styles.css)">
	<link rel="manifest" href="[manifest.json](view-source:https://hutao.dev/manifest.json)">
	<link rel="stylesheet" href="[https://unpkg.com/aos@next/dist/aos.css](view-source:https://unpkg.com/aos@next/dist/aos.css)" />
	
	<!-- YO JS Stuff -->
	<script defer="defer" src="https://cdn.jsdelivr.net/npm/tsparticles@1.39.2/tsparticles.min.js" integrity="sha256-FCz5ToEA27payrGYaVGRidiIA+68Z31TBXFzcIT1/gU=" crossorigin="anonymous"></script>

	<!-- SCHEMA -->
	<!-- https://schema.org/docs/schemas.html -->
	<script type="application/ld+json">
        {
            "@context": "https://schema.org",
            "@type": "Organization",
            "name": "Holy Unblocker",
            "alternateName": "Titanium Network (HU)",
            "url": "https://holyubofficial.net",
            "logo": "https://holyubofficial.net/assets/img/icon.png",
            "sameAs": [
                "https://github.com/titaniumnetwork-dev",
                "https://twitter.com/titaniumnetdev",
                "https://www.youtube.com/channel/UC6LaREFvs9L72SK1s2PcxNg",
                "https://holyubofficial.net"
            ]
        }
    </script>
    <script type="application/ld+json">
        {
            "@context": "https://schema.org",
            "@type": "FAQPage",
            "mainEntity": [{
                "@type": "Question",
                "name": "What is Holy Unblocker?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Holy Unblocker is a secure web proxy service supporting numerous sites while concentrating on detail with design, mechanics, and features. Bypass web filters regardless of whether it is an extension or network-based."
                }
            }, {
                "@type": "Question",
                "name": "How do I unblock websites at school?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Using Holy Unblocker, a free web proxy service with frequent updates and domain restocks, you can unblock sites at school! If a Holy Unblocker site gets blocked simply join the TN Discord to request for a newer site. Restocks occur monthly to prevent mass blocking."
                }
            }, {
                "@type": "Question",
                "name": "What sites can I unblock with Holy Unblocker?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "With Holy Unblocker you can access sites such as Discord, Spotify, YouTube and other game sites!"
                }
            }, {
                "@type": "Question",
                "name": "Is Holy Unblocker safe?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Yep! Check out our Privacy Policy for more information. We don't collect or log any information as it defeats our main moral with ending internet censorship and providing a more private experience without downloading anything. We are also open-source."
                }
            }, {
                "@type": "Question",
                "name": "Does Holy Unblocker hide my search history?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Yes! Change your Tab appearance via Settings > Tab Cloak and use Stealth mode when browsing."
                }
            }, {
                "@type": "Question",
                "name": "Where can I obtain more Holy Unblocker sites?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Be sure to join the Titanium Network discord at discord.gg/unblock! Then simply type \"/proxy\" in our bots channel for a site to be sent to you via DMs using our bot."
                }
            }, {
                "@type": "Question",
                "name": "Is Holy Unblocker open-source?",
                "acceptedAnswer": {
                    "@type": "Answer",
                    "text": "Yes! Check out our GitHub where you can deploy or host your own instance of Holy Unblocker."
                }
            }]
        }
    </script>
</head>
```

### Body Tag (SEO - NAVBAR)
It is essential that your `sitemap.xml` file and navbar match accordingly with page priority if you want to have correct Rich Results on Google or Bing. Ensuring you have a clean and rich page names is essential. For example I could have called the Web Proxies page just Proxies or something bland like Surf. However focusing on core keywords I decided to stick to Web Proxies. Same concept applies throughout the site for every page. Docs will be lengthened to Documentation, etc.

```html
<div id="header" class="fullwidth">
        <a href="/" class="brand">Holy Unblocker</a>
        <input id="mnavecb" type="checkbox">
        <label for="mnavecb" class="mnave"><span class="mnavebutton"></span></label>
        <ul class="navbar">
            <li><a title="Web Proxies" href="/?z">Web Proxies</a></li>
            <li><a title="Games (Unblocked)" href="/?g">Games</a></li>
            <li><a href="/spotify-proxy">Spotify</a></li>
            <li><a href="/youtube-proxy">YouTube</a></li>
            <li><a title="Discord (Unblocked)" href="/discord-proxy">Discord</a></li>
            <li><a href="/reddit-proxy">Reddit</a></li>
            <li class="dropdown-parent"><a href="#">More <i class="fas fa-ellipsis-v"></i></a>
                <div class="dropdown-child" tabindex="0">
                    <ul class="subnavbar">
                        <i class="fas fa-bars"></i>
                        <li><a href="/bookmarklets">Bookmarklets</a></li>
                        <li><a title="Documentation" href="/documentation">Documentation</a></li>
                        <li><a href="/faq">FAQ</a></li>
                        <li><a href="/credits">Credits</a></li>
                        <li><a title="Privacy Policy" href="/privacy-policy">TOS</a></li>
                    </ul>
                </div>
            </li>
        </ul>
    </div>
```

### Body Tag (SEO - Content)
The main takeaway here is my use of the (be sure not the abuse keywords):

- **title attribute** for deeper descriptions (essentially on hover after some time this information will appear over some elements; remember what I said about accessibility)
- Proper HTML markdown structuring for each respective element. Headers are headers and text is text. Code tag is code.
- **alt attribute** on images for accessibility
- **span attribute** for clarity when it comes to crawling
- Descriptive class names for stylesheets (ranking factor) or proper use of a framework (weirdly using a framework helps with SEO but for those vanilla site users you can have your own source remember; just keep the names descriptive and clean)
- Rich keyword usage relevant to the site which can help support backlinks

```html
<div id="mainbody" class="fullwidth">
        <div class="box-home text-center">
        <span id="overview"></span>
            <h1 title="Unblock websites at school or work and bypass filters with Holy Unblocker!">End Internet Censorship.</h1>
            <h1 title="Hide your search history via the Settings menu while using Stealth mode. Enjoy a private experience with Holy Unblocker.">Privacy right at your fingertips.</h1>
            <a title="Learn more?" class="hovermessage buttonlink startbutton" data-hover-text="Epic!" href="#scrollfix">Bypass now?</a>
        </div>
        <img id="logo" width="40px;" height="40px;" src="example" alt="Holy Unblocker's logo; an official flagship Titanium Network site, can bypass web filters."></img>
        <div id="scrollfix"><br></div>
        <div id="desc">
            <div id="info" class="box-info box-large text-center textm">
                <h2>What is Holy Unblocker?</h2>
                <p>Holy Unblocker, an official flagship Titanium Network site, can bypass web filters or "blockers" regardless of whether it is an extension or network-based.</p>
                <p>Being a secure web proxy service, it supports numerous sites while being updated frequently and concentrating on detail with design, mechanics, and features.</p>
                <h2>How do I unblock websites using Holy Unblocker?</h2>
                <p>Head to the <a href="/web-proxies">Web Proxies</a> page and select one of the proxies featured! Afterwards, type out the site you wish to access in the search box ("example.com").</p>
                <p>If you wish to explore the games featured on HU, check out the <a href="/games">game</a> pages.</p>
                <h2>Don't know the difference between each web proxy?</h2>
                <p>Check out the use case for each proxy in the page description. A quick overview:</p>
                <p>- Corrosion: Broad support for the majority of sites but slower (YouTube, now.gg, .io sites)
                    <br>- Womginx: Fast but has forward support for most sites (Discord, Bing and DuckDuckGo)
                </p>
                <h2>Are all sites supported? Why are some sites not loading?</h2>
                <p>As advanced as they are, web proxies are not perfect. This means that some sites may not be supported by any of the proxies listed here due to limitations or security measures.
                </p>
                <p>This also applies to speed; naturally things will be slower or broken under a proxy versus direct access.</p>
            </div>
        </div>
    </div>
```

### Body Content (SEO - FOOTER + SOCIALS)
This section might be the third most important factor. Properly setting up your backlinks is essential and a combination of both the navbar and overall the footer. Modern web design has the stereotype of having socials in the footer. For an open source project this can include a lot more than socials help building up that spider web.

The main takeaways here are to remember the use:

- Proper HTML structure as stated before to maintain. Header tags, list tags and anchors are used correctly
- Rich keywords are used again related to not just the brand but also various socials or in this case mostly open-source assets used. This method creates many backlinks further boosting site and project visibility
- Featuring linked socials that is readable
- Restating the obvious brand with a copyright charset 

```html
<div id="footer" class="fullwidth">
        <div class="footerflex">
            <div class="footerbrand">
                <h3><a href="/">Holy Unblocker</a></h3>
                <p>Made by Students, For Students.</p>
            </div>
            <div class="footerlist">
                <h3>Services</h3>
                <ul>
                    <li><a target="_blank" href="https://github.com/titaniumnetwork-dev">Ultraviolet</a></li>
                    <li><a target="_blank" href="https://discord.gg/VNT4E7gN5Y">Rammerhead</a></li>
                    <li><a target="_blank" href="https://github.com/binary-person/womginx">Womginx</a></li>
                </ul>
            </div>
            <div class="footerlist">
                <h3>About</h3>
                <ul>
                    <li><a target="_blank" href="https://github.com/titaniumnetwork-dev/Holy-Unblocker">GitHub</a></li>
                    <li><a href="/?t">Privacy and Terms of Service</a></li>
                    <li><a href="/?c">Credits</a></li>
                </ul>
            </div>
        </div>
        <div class="footersocials">
            <a target="_blank" class="soc-github" href="https://github.com/titaniumnetwork-dev/Holy-Unblocker"><i class="fab fa-github"></i></a>
            <a target="_blank" class="soc-patreon" href="https://www.patreon.com/holyunblocker"><i class="fab fa-patreon"></i></a>
        </div>
        <p class="copyright">Holy Unblocker &copy; 2024</p>
    </div>

<!-- Scripts required within the body tag here; remember structure -->

<script src="assets/js/common.js"></script>
<script src="assets/js/links.js"></script>
```

## External Links
- https://hutao.dev/
- https://holyunblocker.net/
- https://github.com/QuiteAFancyEmerald/Holy-Unblocker/
- https://github.com/titaniumnetwork-dev/
- https://titaniumnetwork.org/

## Credits
- Quite A Fancy Emerald (writer for this)
- OlyB (for the amazing v5 help, source randomization)
- Binary Person (for the NGINX configuration help in the past)
- Yoct (helped out with various documentation)
