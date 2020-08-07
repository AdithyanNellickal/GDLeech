# GDLeech
GDleech is a second feature made by GDBypass.host for websites owner that need to host their own files on google drive.
GDleech will give webmasters these features:

 - They can enjoy the unlimited files hosing offered by google drive.
 - They can hide their own links location using this server protecting them from bots and bad access.
 - Using this service will make your files always online , no more daily download limit.
 - No ads, just direct download.
 - Running under your own domain or subdomain.
 - Low running cost starting from free.
# Requirements:
In order to make this service running you need the following:
 - You own domain or subdomain running on cloudflare DNS.
 - Google drive account (Unlimited preferred).
 - Cloudflare worker, (Free is good as long as you have a daily download limit up-to 20K.
 - Access to https://gdbypass.host

# Installation:
Installation is very simple just follow these steps:

 1. download [downloader.js](https://github.com/GDBypass/GDLeech/blob/master/downloader.js "downloader.js") & [verify.js](https://github.com/GDBypass/GDLeech/blob/master/verify.js "verify.js") files on your PC.
 2. Login to cloudflare worker panel and make a new 2 worker named them with `downloader` & `verify`.
 3. Paste the [verify.js](https://github.com/GDBypass/GDLeech/blob/master/verify.js "verify.js") contents into the worker named verify and save.
 4. Paste the [downloader.js](https://github.com/GDBypass/GDLeech/blob/master/downloader.js "downloader.js") contents into the worker named downloader and save.
 5. Go back to the cloudflare worker panel and make a new 2 route, assuming that you need to run the download service in this domain `https://downloader.mydomain.com` Press in `Add route` and in Route fields submit `*downloader.mydomain.com/verify*` and choose the `verify` as a worker from the list, hit save. Repeat again, press `Add route` and in Route fields submit `*downloader.mydomain.com/download*` and choose the `downloader` as a worker from the list, hit save. 
 6. Wait a few minutes then go to [https://gdbypass.host/webmasters_tool](https://gdbypass.host/webmasters_tool) to encrypt your links.
 7. On Webmaster Tool webpage submit your google drive links (upto 10 a time) and submit `https://downloader.mydomain.com` as your download domain and hit `Encrypt` button.
 8. Test the generated links to be sure every thing worker very well.

# Why cloudflare:

 - Cloudflare protect our servers from been exposed.
 - By using cloudflare your server will be intact and all the work done on-fly.
 - Cloudflare offer a free worker plan with 100K daily request limit , according to my stats the 100K limit give you about 20K downloads per day.
 - You can always pay 5$ to Cloudflare per month and get 5 million request per month and extra 1 million request cost 50 cents.

# How this work:
As you know, https://gdbypass.host made as a solution for google drive files that had a daily download limit and it prove it self as a working solution. BUT many webmaster need a white labeled solution to run on their own domain, and this what the above do.
You submit your google drive links and we give you encrypted link under your own domain to share.
You links will packed with our unlimited feature , we surf google drive files as usual through our servers and cloudflare worker will reroute the download using your own domain or subdomain.
# How can you help:
You can always help make the system a life by donating using our donation wallet listed on my website : https://gdbypass.host .

**Happy leech**
