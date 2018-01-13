---
title: '"Reflections on trusting trust"'
lang: en
date: 2018-01-08 15:26:30
categories: 
- technologies
tags:
- software development
- software industry experience
thumbnail: /en/technologies/reflections-on-trusting-trust/thumbnail.jpg
---

I came across this topic “Thompson, Kenneth Lane – Reflections on trusting trust” (pdf link: http://vxer.org/lib/pdf/Reflections%20on%20Trusting%20Trust.pdf ) on an answer while I was reading quora. I can’t find that answer now, but the writer was talking about how he was having a hard time fixing a bunch of “out of nowhere” bugs on the deadline of his assignment, and then realized later that those were not his bugs – the problem was caused by the new version of the third-party software he was using.

His answer enlightened me in many ways. The article he mentioned was a really old one – which was written in 1983, but its main point will still be true for a long time I think, and will always be one of the “must read” for a junior developer like me right now.

## The problem rose from just upgrading Windows...

When Microsoft released Windows 10 Creator update, all of the computers in my office were informed to update Windows. No one experienced any problem, except for the reverse proxy server. It used “Bridge Adapter”, and not only us who were suffering from the issue with it, but lots of people on the VirtualBox forum got it too, so much that in some topics later the moderator didn’t even bother to reply anymore. (I even read one topic where the moderator expressed his anger for Windows and how dumb it is to cause these problems). Because this server is extremely important, my supervisor was suffering for the whole week from fixing it, but nothing worked. Pack it to a “hasn’t updated” PC, everything worked well. We even tried reversing the Windows version, but still not work. At last, to save time and our nearly depleted sanity, we decided to leave the server stay still in a “hasn’t updated” PC, and never attempted to update it again. Perhaps we may try again in the future, when the compatibility of Windows and Virtual Box got better, or who knows, maybe we will switch to Windows’s built-in VM one day, if in the end Microsoft's VM won the battle.

## ...to other softwares

This is just one of many problems I experienced with third-party softwares since I started working. Usually they are just small problems, but these problems always remind me of Ken’s article, and make me feel the urge to learn more and more, to understand “how much should I trust”. To be able to trust, we ought to understand things clearly first. The problem can become greater if that’s a tool which can change your code – Tortoise Git for example. There were more than one time when I was resolving conflicts while applying stash, and even after I chose the chunks of code I wanted to keep, they still appeared as conflicted again. When I went into the code to resolve the conflicts manually, I realized it did apply the change to the code, but somehow the UI display was not right – so when I repeated the process, I applied it three times. It’s not that hard to understand how things work – I never heard about Process Monitor before until the day our reverse proxy server broke, and using it was an amazing experience. It’s not Microsoft’s fault to broke our server, it’s out fault for not understand it well enough.

And that made me understand why software’s changelogs are important. Usually when trying a new version, I only care about its new features, all the others “technical logs” were put aside. But in working environment, where reading logs is one of the most important things to do (debug logs, error logs), reading third-party software’s changelogs is also no less critical. You can’t just update immediately without thinking – don’t trust it immediately. Usually they should be fine, but may be on one of the most important days of your career life, it’ll screw you up. Shinichi Akiyama in Liar Game once said, you need to doubt everything. No doubt is just giving up on trying to understand clearly, it’s plain apathy. Question them. Suspect them. When you got your answer on how much you should trust something, you’ll do everything better, and resolve it better when  problems happen.

## Programming languages are no different either

And this goes the same for Programming Language. It won’t be enough to just “know” a language – to understand how a language works is the real meaning of “learning”. Or else, when your code doesn’t work as expected, the only thing you can do is lamenting "why the f** %$@&!". I’ll come back one day with another article about this problem, when I have interesting ideas to write about, or only with the problem in Ken’s article “Write a self-reproducing program”. I really envy people who have wise knowledge on the language they’re using. This one is an example about PHP that our supervisor gave us on our training: https://eev.ee/blog/2012/04/09/php-a-fractal-of-bad-design/ that belonged to an awesome blog that you really should check it out! When I worked with PHP, there were many times I was annoyed by it, but I never noticed these details. Because I didn’t doubt it enough. I didn’t know which language PHP was written by, which compiler PHP is using, and I didn’t notice “how” PHP works carefully. That’s why my level of understanding is not improved. To reach a high level of understanding, it will require serious effort to be put into studying and working. And with PHP 7 came out, knowledge will need to be updated frequently, too.

## Conclusion

To end this article, I’ll talk about CSS. Many people say HTML is not a programming language, and look down on CSS. In my opinion, CSS is really convenient: it’ll save you loading space, and can do many things that you thought only JS or an image can do. And it’s not easy – if we didn’t know exactly what a CSS line actually do. From simple properties like padding, to tricky one like z-index, CSS doesn’t tell us exactly what it does. Nowadays it’s really easy to have a modern-looking website with awesome CSS libraries, so you may think it’s not necessary to put so much time in CSS. But real life is not a paradise, if you end up working with front-end someday, a simple div may become the root of your hard time. Many time I believed that I did something, but CSS actually did something different that resulted in wrong positioning. The lesson I learned was “Don’t let yourself be deceived by language”. In order to trust things right, you need to trust yourself on what you do, too, and to be able to trust yourself right, it’s all up to you.

<p style="text-align:right">Article written by *Fuuka Adachi*</p>