---
title: Creating personalised data stories with GPT-3
date: 2022-05-13 14:03:00 Z
categories:
- Tech
author: ceberhardt
summary: asdasd asd asd asd as d
Field name: 
---

In this post I demonstrate how GPT-3, a new and advanced language model, can construct engaging and unique stories from user-specific data, with relative ease …

This is a [test link](https://blog.scottlogic.com/2021/12/08/narrative-dashboard.html).

> quote

* testing

* lists 

* editing

## Storytelling with data

You can tell powerful stories with data, but so often we are faced with raw data (albeit beautifully presented), and are left to create our own narratives.

If you already have some form of connection to the data, for example it might be the product sales at the company you work for, you are motivated to create your own narrative. In this context, the raw data, effectively presented, is enough. Company performance dashboards, website traffic and application performance metrics are presented in the form of charts and data, with very little supporting text. Because you have a connection to the data, and additional context, you can spot patterns and tell your own stories - for example, how a change in pricing structure affected renewal rates.

However, if you don’t have a strong connection to the data, you are not motivated to invest the time to explore, and create your own stories.

One way to motivate exploration is to make the data visually interesting; even playful. The OECD Better Life Index is an interesting example that allows you to explore data based on the relative weighting of topics. This certainly does makes the experience feel more personal.

The power of combining data and narrative is well understood in the journalism industry. Combining both narrative and data takes up a lot of screen estate, which is why they are often presented as a long-scroll, a story that unfolds with interactive elements triggered as you progress. You’ve likely seen articles in this form from the likes of the BBC, New York Times or Bloomberg. Considering this post is about AI, somewhat topically, here is a story which tracks the usage of an image familiar to people who have studies image processing, and another which provides an introduction to machine learning. There’s even a term that describes this specific presentation style; scrollytelling.

All of the above examples have a single dataset, and a single story. What if the data were more personal? How could we create an accompanying narrative?

Many online services understand that we are interested in our own data, giving us a better understanding of our own behaviours and preferences. Services such as Spotify and Strava (a fitness tracked) allow you to create ‘year in review’ reports at the end of the each year; a fun way to look back on, for example, the music you’ve listened to, or where you’ve run. However, in all cases, they present the raw data itself. Having said that, Strava’s most recent effort was particularly beautiful, as seen in this video.

## Running Report Card - v1. Procedural

Last year I wanted to explore the possibility of creating bespoke stories based on personal data, and as a Strava user, I had a go at creating a running ‘report card’. The app, which I launched last year, uses the Strava API to extract the raw data from an individual user’s account. This data undergoes a process of number crunching to extract information such as total mileage, and total elevation gain. It also runs some simple classification logic, for example a user might be rated as a recreational runner if their mileage is relatively low, or a dedicated runner if it is quite high. The app also throws in the odd comparison, for example, comparing their elevation gain to the height of Everest.

This data analysis creates a number of facts, the narrative itself is simply composed of passages of text, with tokens that represent where these facts should be inserted. Here’s a section of the report that describes when the Strava athlete tends to go for runs (e.g. time of day, day of week):