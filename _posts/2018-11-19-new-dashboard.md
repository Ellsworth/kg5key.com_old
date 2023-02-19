---
layout: post
title: "New Dashboard"
date:   2018-11-19 00:00:00 +0000
categories:
  - RepeaterPi
---

> Out with the old, in with the new...
# Introducing the InfluxDB and Grafana powered dashboard for RepeaterPi.

With the release RepeaterPi `v2.5`, the use of AdafruitIO has been removed completely due to restrictions of the amount of available feeds. In order to resolve these growing pains, I've decided to go with the option of setting up a InfluxDB and Grafana instance.

### Why the switch?
The change to InfluxDB & Grafana is entirely a software change. However, the addition of a *Telewave Inc.* `PM-2A-150` power monitor to the sensor board puts us over the maximum 10 feeds for AdafruitIO. The power monitor serves as an inline wattmeter for the repeaters. This allows us to remotely measure the forward and reflected power.

### Why InfluxDB?
InfluxDB is specifically designed to handle sensor measurements, making it the easiest option to use. It's extremely fast and has more than enough features for our use case.

Influx serves as the database and backend for data management. Meanwhile, Grafana interprets and displays the data from InfluxDB.

### How does this effect users?
The AdafruitIO dashboard will be disabled as soon as both the Georgetown and Taylor repeaters are equipped with the hardware and software changes. After this, you must access the Grafana dashboard with the `Repeater Dashboard` link above.

### Is there any cost of the new system?
The biggest advantage of AdafruitIO is that it is hosted and managed by Adafruit, so not only was it free to use, it was easy it implement. With InfluxDB & Grafana, I had to spin up a *DigitalOcean* VPS along buying this domain. The cost is relatively cheap, as it comes out to being ~$72/year before taxes and fees.


#### That's all folks,
##### 73 de Erich KG5KEY
