---
template: blog-post
title: Product driven data science
slug: /product-driven-data-science-and-web-development
date: 2021-01-23 16:35
description: "Using data science to develop, build and improve products. "
featuredImage: /assets/annie-spratt-hx_hf2lppuu-unsplash.jpg
---
## Overview

Most people (especially people from the technical background) seem to have a disconnect with data science, the problems it solves and how to approach it in their organization.

I personally faced this problem when after a few months of learning this very interesting subject on my own, I realized i got stuck in a rut unable to "Apply" anything at my current job with respect to data science. 

However, after going on forums, listening to podcasts, and listening to a lot of experienced people, I realized I am approaching the problem wrong.

## The problem

A quote comes to mind:

> Ask not what your country can do for you, Ask what you can do for your country

Confused? Let me explain. A lot of people, especially those coming from a technical background tend to think of data science as a "skill" they have gained which they would apply and benefit to for their organization, or their current project.

However, i think this is not how one should approach problems or products. I believe the first rule to "applying" data science is to identify a problem. ( This is also a good general strategy for building products. Once you identify a problem that is not being solved yet, you are probably on the track for creating a good product, IF it solves the problem.

## An example

Let's think about a website, which was the case for me. After recently studying and learning data science and analytics, I kept on thinking where i can apply these machine learning algorithms. 

The translation from theory to product is not a one step , easy process. Real world problems have a lot of noise, in terms of problem statement, relevant stakeholders, data access, etc.

## The solution

I found an opportunity when i came across our server logs. Working at a company which had a solid userbase, i realized we were generating a lot of error logs at my organization. However, these were only being used for error analysis in case our production servers failed / or stopped responding.

Since we had many levels of cache failovers, and Disaster recovery systems, these were rarely utilized, except when needed. Now this is a problem.

I realized i can solve this problem using my newly acquired skills! After toying around with my log files (generated using javascript and node on the server side), I converted these to csv using python, performed simple EDA(Exploratory data analysis) and came up with a bunch of issues which we were facing which were going **unnoticed** for our website.\
\
Voila! 

> The problem **turns into an oppurtunity** to improve your product using data science.



Why stop here? I generated a python script, which performed this conversion and log analysis automatically weekly, and emailed reports to our team. This helped in keeping our [bounce rate](https://en.wikipedia.org/wiki/Bounce_rate) low and identify errors where they occur quickly.



\## The Conclusion

You need business knowledge first. Coming from a technical background you can have tunnel vision when it comes towards the growth of the product.

\> Always think product first



What metrics can be improved for your application ? Where are you struggling  ? - ***Areas for improvement***

Where are you showing growth ? - ***Areas for possible marketing***

What does your audience look like? Where are you lacking ? - **Understand Demographics and how you can improve**

Is there an intersection of technology you already know and your newly developed skills that you can apply? - ***For me this is web development and javascript. Some answers for me are A/B testing, log analysis (above) recommendation engines, demographics eda, analytic tools for the web and much more***



Hope you found all this insightful, and helped you approach problems differently.