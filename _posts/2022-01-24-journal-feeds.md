---
layout: post
title: "Efficient pipelines and tools for scientific journal reading"
date: 2022-01-24
---

If you're a graduate student or researcher, journal reading will be an important part of your life. Trying to catch up with the scientific literature can be daunting, if not impossible.

In this post, I will share my method of reading and keeping track of scientific articles. It is extremely simple, and you might find that it's not so hard to follow the scientific literature, after all. Hopefully you will find the answers to some commonly asked questions about scientific journal reading.

## 1. How much should I read?

Do I read the abstract, just the figures, just the methods, discussion, or introduction?

I suspect that reading style varies *a lot* from person to person. Some people prefer skimming through papers to get a sense of the research and interesting studies out there. Some people prefer digging deep into one paper to find inspiration for their current work. Others might prefer reading just the figures. Or just the introduction/discussion. I don't think you should fret about finding the 'right' way to read scientific paper: there probably isn't one style that works for everyone.

That said, I think it is important to develop the *habit* of journal reading: reading consistently and thinking critically about the papers that you read. I will go more in depth in the next sections.

## 2. How do I build a consistent habit of reading?

For me, the key is to develop a system that helps you to be more efficient at reading. I learned this from several nice blog posts. Personally, I find that the most effective way to build a habit is to (1) operate in a single mode at a time and (2) use a system that helps you switch between modes seamlessly, i.e. with functions for creating bookmarks for 'read later', tagging etc.

I normally operate in two primary modes. In the 'skim' mode, my goal is to cover as many articles as possible. I skim the artiles, marking the ones that seem important to read later. I find this method more efficient and prevents me from 'floating', which means wandering around the scientific literature with no clear goal in mind. That's dangerous. When I operate in this mode, the only things I care about are the title, key words in the abstract and authors of the articles. 

Some of you might start to sense a crippling sense of FOMO (fear of missing out). What if I miss out on some really cool research articles because I failed to read the abstracts? Well, I think that if there is an article that is *so* important and worth reading, you will surely encounter it again at some point, whether on Twitter or through a conversation with your lab-mate who is always on top of the literature.

My second mode is the `focus` mode. Here, I will go through the articles that I bookmarked with a clear goal in mind. I ask myself, why do I need to read this paper? What do I get out of it? Do I want to read the paper from beginning to end or focus on specific sections and figures? Having clear answers to these questions is an interesting exercise in mindfulness which will ultimately enhance your productivity and critical evaluation of research topics.

## 3. RSS feeds

**RSS feeds** are a convenient way of subscribing to contents and receiving automated notifications of a website's recent changes. A long time ago, before the age of Facebook, YouTube and 'subscribe' buttons, people used to keep updated with the news and websites by following an RSS feed thread that is associated with the site. Unlike clicking subscribe buttons on Youtube where your preferences and personal information might be tracked, you can subscribe to RSS feeds without privacy concerns. 

Fortunately for scientific journal readers, major journals often come with an RSS feed that you can follow. For example, a simple search for `Nature Neuroscience RSS feeds` will get you to [this site](http://feeds.nature.com/neuro/rss/current) - you can copy the link and enter it to an RSS reader such as [Feedly](https://feedly.com/). These are sites where you can specify a list of RSS feeds and the site will provide you with updates on the subscribed threads.

I started with Feedly in 2019 and it worked quite well for keeping track of journals. Feedly offers a convenient interface for separating the two journal reading modes. In `skim` mode you can go through the list of articles on the Feedly landing page, and flag the articles that are interesting to you (a few useful keyboard shortcuts helped me speed up this process: `j` for next article, `k` for previous article, `l` for flag, this can be set up with the Feedly site and are great so that you can scan the list of articles with just the keyboard).

## 4. Newsboat
While Feedly is a great starting point for journal readers, it was a bit inflexible for some advanced functions that I wanted. For example, I wanted to highlight authors whose papers I am particularly interested in checking out. I also wanted to have easy ways to open up articles while I'm browsing, and tag the articles with relevant flags (for instance, articles related to theoretical, computation, machine learning, articles about prefrontal cortex etc). I found **Newsboat** to be a valuable replacement and more flexible RSS aggregator. There is a great tutorial by Luke Smith [here](https://www.youtube.com/watch?v=dUFCRqs822w) if you are interested in setting up the environment. The Newsboat documentation can be found [here](https://newsboat.org/releases/2.26/docs/newsboat.html).

The nice thing about Newsboat is that you can write your own custom scripts and define keyboard shortcuts that automate a lot of the steps that I find repetitive while browsing through the literature. For example, I can define keys for skipping, tagging and untagging articles, etc. You can even define a keyboard shortcut that downloads any youtube links in the RSS file. Pretty neat.

I have uploaded my newsboat config file to [github](https://github.com/nhat-le/dotfiles) as a helpful template. If you checkout the `newsboat` folder, there is a separate file called `author_highlight.sh` which is called to highlight specific authors of interest. In addition, the urls of the RSS feeds I subscribe to are given in the `urls` file, and you can see they are conveniently grouped into distinct groups (journals, news, youtube, twitter etc).


## 5. Notion
Finally, a tool that I have used increasingly often is [Notion](https://www.notion.so). Notion is a platform for advanced note-keeping with amazing functionalities for:

- Note-taking at *multiple levels*, i.e. having notebooks inside notebooks and infinitely-nested notes.

- Convenient organization into tables with tags and custom field information. This makes it easy to filter out papers by topic or authors - a huge plus for avid readers who need to remember important papers for their research.

- Easy search and filter your notes.

- Web-clipping - this is a huge plus and why I decided to use Notion in conjunction with Newsboat. After I skim the articles in my `skim` mode, I decide very quickly which articles I want to read later and clip them to my `Papers` database with appropriate tags. 

[Here](https://efficacious-artichoke-8c1.notion.site/43ab7a86f9924f4bb987e3d3c0e11058?v=a644afdd329f4712b805ef3f6abe2b17) is a copy my Notion database for papers.

## 6. Conclusion
Paper reading doesn't have to be scary and overwhelming if you have an efficient pipeline for reading, filtering and keeping track of the enormous online content of modern research. With the tools provided here, hopefully you have a good starting point for implementing your own methods and figuring out the workflow that works best for your purposes. I have found out for myself that there is no right way that works for everyone - it's all about self-reflection and the search for tools that help increase your efficiency and productivity each day.

Have a great time reading!







