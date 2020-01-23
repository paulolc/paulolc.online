---
template: post
title: Hacking Lego Clone Bluetooth Power Brick
slug: hacking-lego-clone-bluetooth-power-brick
draft: true
date: 2020-01-23T11:38:56.844Z
description: >-
  Hacking a Lego Clone Bluetooth Power Brick with the objective of controlling
  it using an high level programming language like Python or Javacript
category: tinkering4good
---
The Power Brick bluetooth device is apparently not being listed when scanning for devices via bluetooth. Either in Windows and in the Raspberry Pi. So it seems the Power Brick is in undiscoverable mode.

This means we need to find it's bluetooth MAC Address in order to, at least, try to contact and connect to it.

I've turned on the bluetooth HCI logging on my Vivo NEX phone and did some successful maneuvering actions on the lego clone rc buggy. However when I retrieved the hci log dump, I didn't found other entries besides messages between the "host" and the "controller". Weird!!

If the bluetooth hci log didn't reveal much, let's see if get more information from the the bluetooth_manager information.

```
 adb.exe shell dumpsys bluetooth_manager
```
