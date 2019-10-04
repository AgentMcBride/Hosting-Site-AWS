# Hosting-Site-AWS

A quick and easy way to get familiar with AWS and static site hosting. AWS (Amazon Web Services) can be complicated to navigate and understand. In this repository you'll find all the necessary files and instructions to create a fully functioning static site on AWS!

## What are we doing?

So a basic outline of what we will accomplish today consists of the following

- Registering a domain using AWS Route 53.
- Setting up an AWS S3 mass storage bucket.
- Uploading some basic html files.
- Using CloudFlare to distribute cached versions of our website globally.

So, how are we going to do all this? What is it going to cost? And when can I get started? Here we go.

## Getting our custom domain

This is one of the easier parts of our tutorial. You're going to want to head over to the AWS console, make an account and get set up into the main dashboard. (insert pictures of main dashboard here)

Next, head up to the search bar and look for Route 53. This is the "application" Amazon uses for registering domains. I like using Route 53 since it is quite technical for expanding into other uses like mail servers, custom sub-domains, etc. yet it is not terribly difficult to integrate with other Amazon services like S3. (show pictures and instructions of route 53 here)

Route 53 costs about 12 dollars a year, depending on your domain. I tend to use the .com domains, but if something neat comes up, then I would go for it. Domain names are something you can keep for your entire life, and it's pretty cool to have one that represents your personal brand well.

## Setting up our S3 bucket

Here comes the meat and potatoes of our set up. Head over to the "S3" app on AWS, and start the process of creating your first S3 bucket. This bucket will house all of our files for our website, so keep that in mind when naming it. In the future, I think it would be cool to find a way to have this bucket mirror a GitHub repository so we don't have to deal with the uploading of files using this weird online console thing. (show pics of setup here, and how to setup instructions. "static website bucket"

## Creating a basic website

HTML and CSS are some of the easiest languages to grasp (though CSS can get quite complex if you don't keep everything organized). I'll provide my basic files so you can sift through those to understand how I use my website.

## Configuring CloudFlare

CloudFlare is an absolutely fantastic service. They manage a number of servers throughout the world that act as a CDN, or content delivery network. For an example, Netflix manages its own CDN which allows the very fast loading of video across the world. Think about a CDN like the branches of a tree gathering sunlight to build the main plant. We are going to use CloudFlare in this instance, for a few things. SSL encryption is increasingly visible on the consumer side of the web (iOS will actually note non-encrypted websites as "not secure" right in the address bar of Safari). Additionally, CloudFlare will give us basic analytics on our website, protect our website from DDoS and other attacks, and allow for the caching of our website worldwide (see the CDN note earlier).

So, to set up CloudFlare head over to the website and sign up for an account. Add your website, use the free platform (this provides the basics we need, however the higher up tiers allow for some really awesome stuff like CloudFlare workers that will help if you decide to do any client side javascript, or server side stuff like PHP or a database like mySQL). CloudFlare is going to ask for the domain name of your site, and then give you two nameservers that you are going to put into your Route 53 console. Head back over to AWS, then Route 53, and click on your hosted zone.

## You're Done!

That's it! You've built your own website in a very overly complex way... but hey... it only costs like 18 bucks a year. That's a steal. Plus, with an AWS account you can do so many fun things. Want to build a blog? Fire up an EC2 instance, and install Jekyll to run your own blog platform. Link up your current website to a subdomain called [blog.thomasmcb.com](http://blog.thomasmcb.com) (replace thomasmcb with your domain), and blam! You've got a great blogging platform that is separated from your main website, so it won't break if you decide to tinker around. Want to create a neat resume website to give to employers? Check out even more subdomains! WhoTheFuckis.thomasmcb.com! Who is he? Why should you hire him? Find out there.
