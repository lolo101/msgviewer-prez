---
theme: the-unnamed
title: MsgViewer
info: |
  # MsgViewer
  An email utility to read and convert between .msg .eml .mbox

  See https://github.com/lolo101/MsgViewer
transition: slide-up
mdc: true
layout: cover
background: https://cover.sli.dev
---

# MsgViewer

---
layout: cover
background: /images/kelly-jean-cKjbI0Y00X0-unsplash.jpg
---

# Back in 2017

<img v-click src="/images/juju-cea.png" style="width: 50%;">

<!--
Back in 2017 I had a friend working at the CEA (french atomic energy reserch lab)
-->
---
transition: none
layout: center
background: "#f3eff5"
---

<img src="/images/email-db.png" style="width: 75%;">

<!--
He was working on a project where they needed to keep a record of mails exchanged.
The mails had to be accessible from any computer in the lab.
Science teams where using Linux boxes
-->
---
transition: none
layout: center
background: "#f3eff5"
---

<img src="/images/email-db-2.png" style="width: 75%;">

<!--
Mails in standard format were finely readable
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/email-db-3.png" style="width: 75%;">

<!--
However mails from Outlook could not be read on the Linux computers!
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/convert.png" style="width: 75%;">

<!--
The proposed idea was to automatically convert Outlook messages into a standard format before adding them to the database
-->
---
transition: none
layout: center
background: "#f3eff5"
---

<img src="/images/free.png" >

<!--
To help my friend I searched the Internet for existing solution but could not find any free software
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/no-free.png" >

---
transition: none
layout: center
background: "#f3eff5"
---

<img src="/images/ms-spec.png" style="width: 50%;">

<!--
However the Microsoft specification of the MSG format was freely avaiable!
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/ms-spec-free.png" style="width: 50%;">

---
layout: about-me
helloMsg: Who am I ?
name: Loïc Broquet
imageSrc: /images/about-me.jpg
job: Principal Engineer @ Sipios
social1: whileitcompiles.substack.com
social2: github.com/lolo101
social3: medium.com/@lolo101
---
<!--
My name is Loïc Broquet
I am the Principal Engineer at Sipios
Author of While it Compiles -- Because it's the best time to read it
GitHub account
Couple articles on Medium
-->
---
transition: none
layout: center
background: "#f3eff5"
---

<img src="/images/sourceforge.png" >

<!--
During my research for my friend I stumbled upon this open-source project on Sourceforge
The project did almost all that was needed
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/sourceforge-last-update.png" >

<!--
However the project seemed abandonned...
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/one-way.png" >

<!--
...And only allowed one-way conversion
Since the documentation was available I thought it would not be too difficult to fork and extend the project
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/github-fork.png" >

<!--
So I started a fork
I Mavenized the project, updated some dependencies and fixed some issues
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/sourceforge-marketing.png" >

<!--
Then I did some marketing
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/tools.png" >

<!--
This project allows me to try some tools
Some which I dropped, some I kept, some I dived into:
- CodeScene -- for which I did a friday presentation @ Sipios
- Qodana -- for which I conducted a comparison with Sonar with the help of Vanya Popkov
- Renovate -- Also used @ BPI
-->
---
layout: section
background: "#f3eff5"
---

# Let's get a little technical

---
layout: center
background: "#f3eff5"
---

<img src="/images/base-principle.png">

<!--
The CLI uses two main parts: a parser and a saver.
Based on the chosen conversion, the parser may be the JavaMailParser or the MsgParser.
In both case the file is converted to an intermediary Message object
The saver then saves the Message into the  chosen format.

The project makes use of two major libraries: jakarta.mail to handle standard mails, and Apache POI for msg format
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/gui.png">

<!--
The project has also a GUI that uses the same parser
and shows up the message with all features you may expect from a modern email client like embedded images,
links, attachments...

Note the langage is germain
-->
---
layout: center
background: "#f3eff5"
---

<img src="/images/contributors.png">

<!--
I have a small bunch of contributors
and also issue reporters
Some of them are regulars

Many of them come from Germany where the project seem to have some base of users
-->
---
layout: center
background: "#f3eff5"
---

# HTML Messages

<!--
In msg format, HTML is transcripted into RTF
-->
---
layout: section
background: https://cover.sli.dev
---

# Demo time

---

# Truc nerd en annexe

- JavaCC les détails

---

# Demander des ⭐

# Il y a des issues à prendre pour ceux qui veulent