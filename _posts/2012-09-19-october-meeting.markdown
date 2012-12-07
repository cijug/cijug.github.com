---
layout: post
title: "October 2nd"
date: 2012-09-19 15:10
comments: true
categories: meeting
---

October's meeting has [Ryan Bergman] of John Deere Intelligent Solutions talking about designing for instability.

On his my.deere.com project, they have a very distributed architecture (too much). With scores of teams working all over the world on different components and different schedules, some challenging stability issues have arisen. Particularly in the testing and staging environments, but occasionaly production. The result has been that our system is designed for dependencies to fail. With GUI switches for simulating failure, turning then on/off, simulating slow-downs and even a "Chaos Monkey".

Part of this is also extensive use of Google Guava caches with custom MemcacheD backings.

Pizza will be provided by John Deere.

[Ryan Bergman]: http://twitter.com/ryber
[Meredith]: https://maps.google.com/maps?q=1716+locust+des+moines&hnear=1716+Locust+St,+Des+Moines,+Iowa+50309&gl=us&t=h&z=16

