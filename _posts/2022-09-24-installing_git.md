---
layout: post
title: Installing Git
---

It's good to be reminded that things are not easy when it comes to things like analytics. For those already deep into it with well-established setups, it's easy to forget how hard-won that setup might have been.

I was handed just such a reminder today when I decided that, as part of my effort to re-build my website using GitHub Pages -- after a decade and a half on WordPress -- that instead of waiting for the web infrastructure to build the site so I could check changes, I would run it locally. This may strike many GH Pages users as obvious, but I was genuinely trying to develop a code-free website that I could then share with colleagues and students to get them started using a text editor and Git. What's more gratifying than a website? Instant publishing.

GitHub Pages run on Ruby and use the Jekyll gem. A quick web search revealed that the best way to install Ruby on macOS was Homebrew, which is itself written in Ruby. Fine. I use `conda` to maintain my Python stack. It makes sense. And as an added bonus, people love Homebrew and I know it does a whole lot more.

The convention for installing homebrew is:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Only that reveals that I have forgotten to install the Xcode Command Line Tools. That's not so strange to me: when I used to use MacPorts for package management, it was the first step to install MacPorts -- which became an almost annual task as Apple increased the frequency with which is released major versions of macOS. 

```bash
xcode-select --install
```

Installation done. I re-ran the bash command above. *Oops!* I forgot to sign the license.

```bash
sudo xcodebuild -license
```

License agreed to, I re-ran the homebrew installation command again. You agree to a few things ... and *fail*. Something about `git`. I do a few casual web searches that do not solve the problem until I remember to do the obvious: excerpt the error code into the search: `xcode-select: Failed to locate 'git'`. At some point I stumbled upon the solution:

```bash
xcodebuild -runFirstLaunch
```

I also ended up clearing out the previous homebrew failed installs and starting somewhat from scratch:

```bash
sudo rm -rf /usr/local/Homebrew
```

That's a bit of a winding path for me, and I have a reasonable amount of patience and an almost reasonable amount of awareness, if not actual knowledge. This would be overwhelming for a lot of new users. I understand now why so many courses in which the basics are taught feature such installations as part of a class meeting. They are just so many weird things that can go wrong, and it helps to have someone who can help you troubleshoot and who can also re-assure you that eventually you will have a working installation and you will not need to worry about any of this ... until next time.