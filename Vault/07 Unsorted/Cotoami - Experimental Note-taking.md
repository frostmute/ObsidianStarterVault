---
banner: https://c10.patreonusercontent.com/4/patreon-media/p/campaign/1954224/f6476c5e3c974a0f9fc3bde8cfcce139/eyJ3IjoxOTIwLCJ3ZSI6MX0%3D/1.png?token-time=1717459200&token-hash=GX7hYYt81F9jJpjisJSEUCWieS194cUYMgUxuVMpEso%3D
category:
  - "[[../00 - CATEGORIES/Clippings]]"
feature: "![[../03 - MEDIA & FILES/1d85930d9bd0c705a54632778498aead_MD5.jpg]]"
---
# Experimental Note-taking App Focusing on Connecting


![Cotoami Project](../03%20-%20MEDIA%20&%20FILES/1d85930d9bd0c705a54632778498aead_MD5.jpg)

Hello. My name is Daisuke Morita([@marubinotto](https://twitter.com/marubinotto)), I’m a software engineer based in Tokyo.

For about two years now, I’ve been developing an experimental web app for knowledge workers, especially who need to produce new ideas and concepts on a regular basis. It’s called “Cotoami” and designed for both personal and collaborative use.

Cotoami has unique concepts that are largely based on the recent shifting of knowledge structures from trees into networks.

In fact, it’s not just a matter of structure, but also involving a drastic change of the process to make structures.

In many cases of note-taking, writing and connecting things are happening at the same time. You write things into categories, which are represented as, for example, sections in a notebook, folders/directories on an operating system or nodes in an outliner. You almost connect things unconsciously just following inclusive or deductive relationships to make a tree structure.

Cotoami also supports this way of organizing things, but its main aim is to separate writing and connecting to make the latter a more conscious step.

Here’s how it works. In Cotoami, you post your thoughts and ideas like chatting (the timeline actually has a chatting feature where you can chat with other users sharing the same space):

![[../03 - MEDIA & FILES/1_jQLm7gNw2wkO88X_e8RsVw.gif]]

You would feel free to write anything that comes in your mind. Your posts just flow into the past unless they are pinned:

![[../03 - MEDIA & FILES/1_CN261mz-E7Uk8IxMN2WlUA.gif]]

And then afterward, you make connections between the posts to enrich your stock (there are two panes side by side representing [flow and stock](http://snarkmarket.com/2010/4890) respectively).

![[../03 - MEDIA & FILES/1_UPMKo-pAYoofhJ5rEN4F_Q.gif]]

I personally call it an Input/Observe/Connect cycle. In iterations of this cycle, the outlines of structures are not mere containers designed in advance or reflecting known categories, but discoveries emerged from the observation of a variety of inputs.

Cotoami has various features to support this cycle, for example, a random/shuffle feature helps you observe many combinations of posts to discover unknown connections.

![[../03 - MEDIA & FILES/1_QCGRm2eULjyDNWF3gdHIoQ.gif]]

The screenshot below is an example of connected knowledge I created with Cotoami. I was collecting fragments of information about Brexit from various websites, which was not a familiar topic for me before this experiment, and at the same time, making connections between them and extracting concepts to gradually build up this network structure.

![[../03 - MEDIA & FILES/Pasted image 20240518182006.png]]

Clicking on one of the nodes in the summarized network diagram shows the original posts behind it, indicating the network of the abstract concepts has emerged from the concrete information of the posts.

![[../03 - MEDIA & FILES/1_wjCU0bEfT5SXlFxeThmxzQ.gif]]

From this experiment, I found that the network model is more suitable for learning complex topics like Brexit that involves many concepts and entities interconnected to each other. A network can be more complex to grasp than a tree, but it can have multiple contexts and viewpoints, helping you grasp complex things as they are and keeping you from jumping to premature conclusions from a single viewpoint.

Cotoami’s challenge is to mitigate the difficulty of dealing with networks. One of the features to tackle it is “Cotonomas”. Here I should explain the terms of the basic building blocks in Cotoami.

In Cotoami, individual posts are called “Cotos”, which is a Japanese word meaning “thing”, and there’s a special type of Coto called “Cotonoma” (Coto-no-ma means “a space of Cotos”). These two concepts are the basic building blocks of a knowledge base in Cotoami.

Here you might notice something about why this software is called “Cotoami”. “Coto” means “thing” and “ami” means “weave” in Japanese.

Cotonomas let you divide a large network of Cotos into sub-networks to deal with each sub-network separately. Here is a video to demonstrate splitting the Brexit network into sub-networks by converting some of the seemingly important Cotos into Cotonomas.

Each Cotonoma has a dedicated chat timeline associated with it so that you can iterate another Input/Observe/Connect cycle solely on a topic represented by a Cotonoma and produce further deriving Cotonomas. So the cycle is recursive and generative, and yet it’s not simply drilling down into specifics because there are two types of connections in Cotoami while trees generally have only one type of connections.

Cotoami divides connections into two categories by letting you optionally annotate them: annotated connections and plain connections. Annotations on connections are called “linking phrases”. The term “linking phrases” is borrowed from [Concept Maps](http://cmap.ihmc.us/docs/conceptmap.php). Actually, you can create concept maps with this feature as demonstrated in the following video:

The concept map created in the demo explains why we have seasons (originally presented in the article at Concept Maps official website: [http://cmap.ihmc.us/docs/theory-of-concept-maps](http://cmap.ihmc.us/docs/theory-of-concept-maps)).

Concept mapping is a good way to demonstrate this annotating feature, but an important difference is that Cotoami’s linking phrases are optional. That means you should annotate only connections whose relationships are not clear to you. Those obscure relationships are possibly valuable knowledge for you (since you didn’t know them well before), and should be highlighted in your knowledge base. I personally call them “horizontal relationships”.

On the other hand, “vertical relationships” generally means inclusive or deductive relationships like “includes”, “results in”, or “is determined by”. Simple arrow lines would be enough to express these relationships and you wouldn’t feel the need for annotations in most cases. So whether a connection is vertical or horizontal is essentially subjective. It depends on your context in the same way as Cotonomas are concepts emerged from your iterations of the cycle.

If you are only following vertical relationships, your network of knowledge will form a mere hierarchy and your knowledge journey is just drilling down into specifics as making a tree. But, by introducing horizontal relationships, you can reach out to neighboring categories just like cross-links in Mind Maps or Concept Maps.

In terms of dealing with complex networks, linking phrases help you focus on important connections in a network.

![[../03 - MEDIA & FILES/Pasted image 20240518182021.jpg]]

When you look at a network like the above, you just need to focus on blue connections in it to grasp what you’ve learned so far.

In the experience of playing with these concepts for a year or so, I found that the varieties of inputs are crucial to discover unknown interesting connections later on. Only posting your thoughts and ideas popped up in your head will probably lead you to merely make known connections in a roundabout way. But, how do we collect many varieties of Cotos?

As a solution to this problem, I’ve been developing a Chrome Extension called “Cotoami Scraper”. It lets you scrape web content to generate inputs for Cotoami.

By not only writing your thoughts and ideas but also collecting random information from various sources, you could even discover new themes to delve into, in addition to setting a theme like “Brexit” in advance.

So, that is what Cotoami is all about. What do you think? It is still in an experimental phase, so the concepts are subject to change or evolve. If you are interested in the development of this project, follow the twitter account ([@cotoami](https://twitter.com/cotoami)) and keep an eye on this blog. I’ll write about new discoveries in development.

Cotoami is [an open source project](https://github.com/cotoami/cotoami) and looking for people who support this project in any way, especially if you become a patron at [https://www.patreon.com/cotoami](https://www.patreon.com/cotoami), that would be very grateful and in return, I’ll give you a login account to [the official Cotoami server](https://cotoa.me/).