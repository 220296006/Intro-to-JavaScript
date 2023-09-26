# General Website Optimization

## What is gzip used for?

Gzip, the most popular compression method, is used by web servers and browsers to seamlessly compress and decompress content as it's transmitted over the Internet. Used mostly on code and text files, gzip can reduce the size of JavaScript, CSS, and HTML files by up to 90%.

## Minification

Minification is the process of minimizing code and markup in your web pages and script files. It's one of the main methods used to reduce load times and bandwidth usage on websites. Minification dramatically improves site speed and accessibility, directly translating into a better user experience.

## Browser-Caching

How does browser caching work?
Caching is a process in which data is kept in a cache. A cache is simply a storage area that stores data for a short time. Browser caching is a process that involves the temporary storage of resources in web browsers. A visitor's web browser downloads various website resources and stores them in the local drive.

## Content Distribution Network

 CDN (content delivery network), also called a content distribution network, is a group of geographically distributed and interconnected servers. They provide cached internet content from a network location closest to a user to speed up its delivery.

## Miscellaneous

Here’s a couple more tips to squeeze out even more juice:

Optimize your website to load “above-the-fold” content first to increase the perceived performance of your site. One common way to do this is by lazy-loading images that don’t show up on the landing page.
Unless your application depends on Javascript to render HTML, such as a website built with Angular or React, then it is likely safe to load your script tags at the bottom of the body section of your HTML file. This could affect your time-to-interactive, however, so it is NOT a technique I would recommend for every situation.

