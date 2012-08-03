---
title: I2C Pinbelegung
date: '2012-07-22'
description:
categories: bachelor
---


Pinbelegung für die I2C Hirschmann Stecker:  

![Pinbelegung](http://dl.dropbox.com/u/18993829/bachelor/document/hirschmann.png)

| Pin |  I2C  |  Arduino | BMA180 | Farbe |
|:----:|:-------:|:-----------:|:------------:|:--------:|
| 1    |  3.3V |     3.3V   |    VDD    |   Rot   |
| 2    |           |                |                 |            |
| 3    |  SDA |     A4       |     SDI     |  Gelb  |
| 4    |  SCL |     A5       |     SCK    |  Grün  |
| 5    |          |                 |                 |             |
| 6    |           |                |                 |             |
| 7    | GND |   GND    |    GND    | Schwarz |