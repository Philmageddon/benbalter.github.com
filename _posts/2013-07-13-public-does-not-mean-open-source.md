---
layout: post
comments: true
author: Ben Balter
title: Public ≠ Open Source
category: technology
excerpt: ""
tags: []

---

The Estonian National Electoral Committee [recently published](http://news.err.ee/politics/0233b688-b116-44c3-98ca-89a4057acad8) the source code that underlies their nation-wide Internet-based voting system, the first of its kind in the world. Don't get me wrong, this is a great step toward transparency, but it's also a textbook example of how, especially when it comes to government, simply publishing a project's source code [does not an open source project make](http://ben.balter.com/2012/10/15/open-source-is-not-a-verb/).

## Documentation

![Estonian voting machine readme](https://f.cloud.github.com/assets/282759/792947/bae3313a-ebd0-11e2-8f14-7bcc2324eefa.png)

[That's it](https://github.com/vvk-ehk/evalimine/blob/7efb02364b08717259cdea3933a43448cd94f4ab/README.md). No information on what the software does, what its requirements are, how to run it, how to contribute to it, what you can and can't do with it, or even who wrote it. The entire thing's a black box, and digging into the code itself doesn't help much, as there's not much documentation there, other than a ubiquitous copyright notice (more on that in a moment). As [@pietercolpaert](http://github.com/pietercolpaert) noted in [vvk-ehk/evalimine#4](https://github.com/vvk-ehk/evalimine/issues/4), this isn't just about making things easier for geeks. This is a voting machine we're talking about here. Proper documentation is the first step to empowering civic-hackers to setup test environments to discover potential issues, for technical experts to verify that the software actually does what it says it does, and more broadly to allowing others governments to repurpose the system for their own, more evolved elections.

## License

![No derrivative works](https://f.cloud.github.com/assets/282759/792994/f9d52f92-ebd5-11e2-883c-876e14f84474.png)

The project is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivs license](http://creativecommons.org/licenses/by-nc-nd/3.0/). This is problematic for two reasons:

First, as [@boamaod](http://github.com/boamaod) rightly points out, in [vvk-ehk/evalimine#1](https://github.com/vvk-ehk/evalimine/issues/1), the project misapropriates a licence designed for text-based works, rather than using one of the [many well-known, generally accepted, and industry-standard open-source licenses](http://opensource.org/licenses). Heck, even Creative Commons themselves, the authors and maintainers of the project's chosen license [explicitly states](http://wiki.creativecommons.org/Frequently_Asked_Questions#Can_I_apply_a_Creative_Commons_license_to_software.3F) that *"Creative Commons licenses should not be used for software. We strongly encourage you to use one of the very good software licenses which are already available"* So why does this seemingly technical distinction matter? For one, the license is, by definition, not an open-source license. It makes no mention of software-specific considerations like distinctions between object and source code, and makes no effort to achieve compatability with other open-source licenses so that it can be integrated with existing open-source projects.

Second, and more importantly, the license explicitly [forbids the creation of derivative works](https://github.com/vvk-ehk/evalimine/issues/2), meaning open-source developers may not *"alter, transform, or build upon"* the software. That's the whole point of open source. Growing communities around shared challenges. Without the ability to legally modify the software, let alone the opportunity to submit those improvements back as proposed changes, the source code is simply published. There's nothing open about it. It may as well be a PDF. It's a one-way street.

## A one-way code dump

![Pulse graph](https://f.cloud.github.com/assets/282759/793008/2dc7f78e-ebd7-11e2-9059-8b1811429a96.png)

The last indication here that makes this a great example of distinguishing code-publisng from open source is its developer workflow. For a project to be open source, there simply cannot be two classes of developers. Issues and priorities must be out in the open and commits need to freely flow across the firewall so that everyone has access to the same information, and thus, the same opportuntiy to contribute. That's [not the case here](https://github.com/vvk-ehk/evalimine/issues/3). *"[T]his is not the repo that is used for active development. The active development takes place in the private repositories of the software developer".* Wat?

*"Yes, this repo will be maintained. The next milestone is mid-august. NEC (National Electoral Committee) plans to publish the final source version also in this repo"*

https://github.com/vvk-ehk/evalimine/issues/3#issuecomment-20871325

## Why it matters

This isn't a simple mobile app or a public-facing website we're talking about here. This software plays a fundamental role in determining a country's future. It should be the best of the best, and we should expect no less. Yet due to culture, procurement, lack of institutional knowledge, or other constraints, the software with which we entrust the day-to-day workings of our country (Estonia or elsewhere) sadly doesn't always rise to the level that may otherwise be freely avaialable. As [@andris9](http://github.com/andris9) optimisticly comments, *"I'm sure a lot of people would love to help you out with the code, which currently does not look very good (no tests, no docs, no code comments, no nothing - and thus, not very trustworthy).("* What scares me, is if this is the code that we can see, how much should we trust the code that we can't?

Don't get me wrong. Nothing here is intended to criticize the Estonian Election Comittee or the work they're doing. Transparency is an admirable goal and publishing the code to the underlying software that powers the country's electoral system is a great thing. But it's not open source. Open source is about more than simply hitting publish. It's about growing a community. It's about sharing. And in the government context, it's about forcing well-entrenched burocuracy to give way to the Internet's meritocracy for its own benefit. As [@andris9](http://github.com/andris9) [put it](https://github.com/vvk-ehk/evalimine/issues/2#issuecomment-20917195) best, *"[t]his project is 'view source', not 'open source.'"*
