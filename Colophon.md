---
layout: page
title: Colophon
weight: 10
---
# Colophon

Sites like this are, across multiple dimensions, labors of love: people take the time to build them because they like playing with technology, because they like sharing what they have learned or what they are working on, or because they like spending entirely too much time deep in the weeds of the technologies that lie behind the thing we call the *Intarweb*. 

The current version of this site is built entirely using open source technologies and I wanted to do that in order to explore ways of building websites that would be useful, and as cheap as possible, for interested students and colleagues.[^1] The site before you now runs on [GitHub pages][]. It is built "code-less": I do not run Ruby locally and then "deploy" the site to a web server. Rather, I write everything in plain text, markdown for the posts and pages you see here, and then I push the repository in which all those plain documents reside up to GitHub, which then processes them into the HTML that you are reading right now. (Like Moliere's gentleman discovering he already spoke prose, perhaps you have just now discovered that you read HTML! *All the time.*) 

The work I have done is to develop templates and style sheets -- along with some Amazon AWS scribbles to deliver media --  to make the actual running of this website "code-less". If that interests you, then you are welcome to step into the equipment shed and see how this thing is held together with licks, promises, bailing wire, and assorted other miscellany from old folk sayings: [GitHub repo][].

The template for this site is based on Hyde, an adaptation of the Poole template for Jekyll. The basic mechanics have remained largely undisturbed, though I have the ability to *pin a post* as a function I would like to add.

For those interested in the site's design, or at least the design impulse behind what you see here, I have always been an advocate for simplicity coupled with generous white space. Whether designing a document like a syllabus, a website, or a journal article, I never want a user/reader/viewer to wonder where they are or what they are looking at. I want, so far as such things are possible, the user to be immersed and for any available controls to feel "natural" -- there's probably not enough quotation marks for *natural*, but there you have it.

As someone who spent time on an undergraduate editorial team in college and later put themselves through graduate school doing graphic design, I am familiar with some of the basics of design for reading, and using a sans serif type face like the one used on this website slows reading. However, since I didn't find any of the [websafe type faces][] very appealling, I wanted to keep the font loads to a minimum, so I chose one type face that I felt provided a compelling display/titling appearance and also seemed *fairly* readable. The winner was Roboto Condensed designed by Christian Robertson and available (for free) via [Google Fonts][]. (I did look into purchasing fonts from designers offering type faces via the SIL license, but, at least for me, GitHub pages were not happy with the `.woff` files.)

Live and learn.

[^1]: Since 2004, I have maintained a WordPress [weblog][]. Over the years, I tried other setups, but WordPress remained incredibly reliable. And, too, I was spoiled by my first ISP, A Small Orange, which was eventually bought and lost its magic. I will be forever grateful to [CynderHost][] to coming to the rescue when I asked about WordPress hosting. They offer an incredible deal for anyone interested in hosting a WordPress site on their own. It's just that my time with WordPress, which had become a behemoth *all things to all people* application, came to an end. I posted a lot of material to that blog over the years, but, to be honest, the technical material gets the most attention: e.g., the most popular post at this point is about how to [Append a Python List Using a List Comprehension][append]. As 2023 unfolds, I will migrate its archive to this site.

[GitHub pages]: https://pages.github.com
[GitHub repo]: https://github.com/johnlaudun/blog
[websafe type faces]: https://www.w3schools.com/csSref/css_websafe_fonts.php
[Google Fonts]: https://fonts.google.com
[weblog]: https://johnlaudun.org/
[CynderHost]: https://cynderhost.com
[append]: http://johnlaudun.org/20170928-append-python-list-using-list-comprehension/

