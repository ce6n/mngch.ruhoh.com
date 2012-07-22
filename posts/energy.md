---
title: energy usage
date: '2012-07-21'
description:
categories:
---

# Live Energy Consumption

I've done it. I started measuring my consumption of electrical energy. It's a little project that started out of boredom and curiosity (as do so many) and now I hope it's helping to find the source of energy waste and reduce the usage.
The consumption is recorded 24/7 with one measurement every few seconds, so it's possible to track individual consumers. This is called smart metering which is a good thing and a bad thing too. This I want to point out later.

Also a little documentation on how the system works is planned, but first some impressions:

<img class="aligncenter" src="{{urls.media}}/energy_opening.jpg">

As we got a three phase energy system here, there are three channels which are measured seperately. Now the quest is to identify the different devices in the data. Let's have look at channel 1. You can identify the fridge very well, due to the periodical intervals of about 100W, which are the times it is actually cooling. The Spikes up to 1800W are from the electric kettle (me preparing some tea) and the at nine o' clock (2700W) probably from taking a shower. 

<div class="widget-container-nc">
	<h2>Energy explorer</h2>
	<iframe frameborder="0" marginheight="0" marginwidth="0" scrolling="no" src="http://vis.openenergymonitor.org/emoncms3/Vis/kWhdZoomer/kwhdzoomer.php?
          apikey=3852be4e90508b29dfcec350a79582e9&amp;kwhd=1534&amp;power=1530&amp;currency=euro&amp;pricekwh=0.22" style="width:645px; height:470px;"></iframe></div>



And here finally the live data from my flat:


## Total
<iframe style="width:100%; height:400px;" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="http://vis.openenergymonitor.org/emoncms3/Vis/realtime.php?apikey=297e4daec5ed48e202f4c1eedf2dded8&feedid=1530"></iframe>

## Channel 1
<iframe style="width:100%; height:400px;" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="http://vis.openenergymonitor.org/emoncms3/Vis/realtime.php?apikey=297e4daec5ed48e202f4c1eedf2dded8&feedid=1528"></iframe>

## Channel 2
<iframe style="width:100%; height:400px;" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="http://vis.openenergymonitor.org/emoncms3/Vis/realtime.php?apikey=297e4daec5ed48e202f4c1eedf2dded8&feedid=1531"></iframe>

## Channel 3
<iframe style="width:100%; height:400px;" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="http://vis.openenergymonitor.org/emoncms3/Vis/realtime.php?apikey=297e4daec5ed48e202f4c1eedf2dded8&feedid=1529"></iframe>




## Temperature
<iframe style="width:100%; height:400px;" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="http://vis.openenergymonitor.org/emoncms3/Vis/realtime.php?apikey=297e4daec5ed48e202f4c1eedf2dded8&feedid=1532"></iframe>

