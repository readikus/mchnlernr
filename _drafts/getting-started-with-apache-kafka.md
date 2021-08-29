---
title: Getting started with Apache Kafka
description: In this tutorial we will look at recording data into Apache Kafka so we can start to build a dataset for spotting trends.
date: 2021-07-14
tags:
  - kafka
  - python
  - streaming platforms
layout: layouts/post.njk
---

Since I built `royston` as an in-memory, single node python package, I've been thinking about what the best approach would be to run it at scale. With a recent increase in the number of data feeds my main application uses, the single node has started to hit performance issues. I have been hearing a lot recently about Kafka and streaming platforms for handling events. At first, it wasn't immediately obvious how `royston` would migrate to this, but after a little reading, it was all about events.

# Kafka 101



Apache Kafka


A streaming platform used to collect, process, store, and integrate data events at scale.

Event = a record of something that happened. Be it a user hover over a button, a temperature reading from an IoT sensor, a share price was recorded, or something of that nature. Immutable - it happened, you ain't changing it, bro.

Topics = a log of events i.e. database tables. A collection of events that are similar. Create lots of topics for specific events. Then we have filtered topics. So we could have all thermostat readings, then only the ones from kitchens, hot places etc.
Topics can be referred to as queues, but not precise. A topic is a log of events.
Append only.
Can only seek to offset, not indexed.

Data is write-only.


Partitioning

- splitting a log of events into parts, each of which can live on a separate node.
- how do we decide which does which?! 



Single node performance - kafka gets a lot out of a little, as there isn't too mich going on. Replication always makes it easier to replicate around a cluster.









# What is an "event"?

For detecting news trends, there are a number of events going on. Firstly, the crawler/scraper triggers an event when it finds a new URL to process.





https://docs.confluent.io/platform/current/quickstart/ce-docker-quickstart.html?utm_medium=sem&utm_source=google&utm_campaign=ch.sem_br.nonbrand_tp.prs_tgt.kafka_mt.mbm_rgn.emea_lng.eng_dv.all_con.kafka-docker&utm_term=%2Bkafka%20%2Bdocker&creative=&device=c&placement=&gclid=CjwKCAjwlrqHBhByEiwAnLmYUJOgOWBwcBVEMFCX38ZcLaS3OBHl34c0mAdzdie0tK2bV_gX2DzlFBoC-2YQAvD_BwE




finds a article


In the example I am working with, one of the key events is a new news item is found.





I've been hearing

I've found Andrew Ng's explanations are great for how the underlying algorithms work, and whilst over places skim over details then get into using Tensorflow, I don't feel satistfied just plugging a CSV file in and some hyperparameters.s