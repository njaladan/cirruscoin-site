# CirrusCoin website

This repository contains the code for the official CirrusCoin token sale website developed by me.

## Technologies Used:
* jquery
* Bootstrap
* Paperkit (this was new for me)
* Zapier
* Pageclip

## Extra
I wanted to host the site on Github Pages due to simplicity and a high bandwidth limit (100gb for free?!), but the problem was that gh-pages supports purely static websites. This led to a challenge, since collecting user "registration" data is generally a feature for most ICO websites.

To get around this, I took advantage of [Pageclip](https://pageclip.co), which is a service that provides forms for static websites by causing the POST request to be handled through their endpoint. The interface and customization options are truly wonderful, and I think it's something that I'll continue to use in the future.

It was necessary for the company to be able to see the data, however, so I needed a way to export the data real-time to an easily accessible location. I took advantage of the Pageclip Webhooks feature, which sends a JSON POST request to an endpoint of choice as soon as it's received, sort of like passing on a baton in a track race.

I connected this endpoint to the integrations available in [Zapier](https://zapier.com), which is basically but IFTTT but designed for a more corporate setting. I used the Webhook to Google Sheets "Zap", which posted parsed data onto a Google Sheets document as soon as data was posted to the Webhook.

It worked perfectly, and very well! The company was able to easily access data through a shared Google Sheets for their mailing list and customer contact purposes, and I had full access over the data transfer pipeline through easily scalable apps. 
