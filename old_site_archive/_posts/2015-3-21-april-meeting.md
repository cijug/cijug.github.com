---
layout: post
title: "April 7th"
date: 2015-3-19 15:10
comments: true
categories: meeting
---

Unit testing is hard. That's why a lot of developers don't do it. What's harder than getting started in TDD? Working on someone else's bad unit tests.

Why do some tests age better than others? Why do some grow with the code while others are re-written or deleted at the first opportunity?

It's no coincidence that the ones that live exhibit certain positive characteristics. They provide enough context for future readers to understand what's happening, but keep the test [DRY] enough to avoid implementation overdose. Effective unit tests can't live on their own, they need good implementation code to make them effective.

[Dan Mullins] has written a lot of bad tests. Some are bad right away, some go bad 30 days later, and some go bad the second a second developer reviews them. After reading [Working Effectively with Unit Tests] by [Jay Fields], it became clear why some tests age better than others. Effective unit tests strike the right balance between context and clarity.

At April's CIJUG, [Dan Mullins] will walk through his personal unit testing evolution and discuss the implementation, why it seemed like a good idea, and why it aged poorly. He'll also talk about how good tests need good implementations.

[Working Effectively with Unit Tests]: https://leanpub.com/wewut
[Jay Fields]: https://twitter.com/thejayfields
[Dan Mullins]: https://twitter.com/dmullins
[DRY]: http://en.wikipedia.org/wiki/Don%27t_repeat_yourself


