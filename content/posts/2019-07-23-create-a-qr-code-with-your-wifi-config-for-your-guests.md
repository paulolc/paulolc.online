---
template: post
title: Create a QR code with your WIFI config for your guests
slug: QR code with your WIFI config FTW!
draft: false
date: 2019-07-23T06:44:48.200Z
description: >-
  A special crafted QR code is interpreted by Android and iOS as configuration
  for a wifi network
category: tips
---
If you throw a party and you want to conveniently share your guest wifi network details with your guests just create a QR code with the wifi configuration. You could also do this if you own a public place with free-wifi and spare your customers/visitors of the hassle of configuring the wifi. The QR code would do it for them.

It's easy. Just use your favorite QR code generator with a crafted string having the following pattern:

`WIFI:T:WPA;S:mynetwork;P:mypass;;`


| Parameter | Example | Description |
|---|---|---|
| T | WPA | Authentication type; can be WEP or WPA, or 'nopass' for no password. Or, omit for no password. |
| S | mynetwork | Network SSID. Required. Enclose in double quotes if it is an ASCII name, but could be interpreted as hex (i.e. "ABCD")
 |
| P | mypass | Password, ignored if T is "nopass" (in which case it may be omitted). Enclose in double quotes if it is an ASCII name, but could be interpreted as hex (i.e. "ABCD")
 |
| H | true |Optional. True if the network SSID is hidden. |

source: [Wi-Fi Network config (Android, iOS 11+)](https://github.com/zxing/zxing/wiki/Barcode-Contents#wi-fi-network-config-android-ios-11)

HN thread: [Pure JavaScript WiFi QR Code Generator](https://news.ycombinator.com/item?id=20494730)

