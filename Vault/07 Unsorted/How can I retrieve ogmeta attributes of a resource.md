# [How can I retrieve og/meta attributes of a resource?](https://stackoverflow.com/questions/19312942/how-can-i-retrieve-og-meta-attributes-of-a-resource)

I'm making an application that retrieve tweets on Twitter of a user.

Those feeds contains links to external resources, such as Articles, Webpage or YouTube video.

I get trought the Twitter API the JSON of these feeds, but there arent included the `og:` attributes of the content. And I'd like to catch them and show to my website.

Such as [**this**](https://stackoverflow.com/questions/19001883/how-can-i-check-classes-that-ends-with) question of StackOverflow:

I'd like to catch those informations for each shared resource on each tweet. So I think I'll, for each tweet (which for me is a box) do an ajax request client side, download the html and parse it, retrieving `og:title`, `og:description`, `og:type` and `og:image`.

Is this the best approch? What's about parse this data in Javascript/Jquery?

## 4 Answers

These `og:` attributes are [**Open Graph Protocol**](http://ogp.me/) attributes, there are many way to get these datas : you should check the codes of [**Open Graph Protocol parser**](https://github.com/fiann/jquery.ogp) which may be very usefull for you, and this [**PHP and jQuery Facebook link parser**](http://redsunsoft.com/2011/01/parse-link-like-facebook-with-jquery-and-php/).

You can also check this [**StackOverflow Question**](https://stackoverflow.com/questions/7454644/how-to-get-open-graph-protocol-of-a-webpage-by-php) about PHP parsing and this [**Opengraph PHP parser**](https://github.com/scottmac/opengraph) and dynamically use them with ajax calls.

Finally, this [**StackOverflow question**](https://stackoverflow.com/questions/1034881/what-is-the-best-practice-for-parsing-remote-content-with-jquery) about JQuery and pure JavaScript parsing is very interesting and could really help you.

Hope you'll find what you need ! ;)

DISCLAIMER: OpenGraph.io is a commercial product I work on and support.

As you mentioned, often times there are no OG tags to work with. There are all sorts of scenarios you can come across (e.g. encoding, misusing HTML tags, etc). If you want to handle the edge cases I'd recommend [**http://www.opengraph.io/**](http://www.opengraph.io/)

One of its major benefits is that it will infer information like the title or description (if you end up needing it) from the content on the page if OpenGraph tags don't exist.

To get information about a site use (link should be URL encoded):

Which will return something like:

You can use [`**open-graph-scraper**`](https://github.com/jshemas/openGraphScraper) for this:

_**Note: on the client side you'll hit into CORS issues, so this is best done on the server side if possible.**_

In my instance I'm using Next.js, and I added a file in `/pages/api/metadata/[...url].ts` which I could then query, that would do the `ogs` lookup and then return the result, which I can then use in my front-end.

Anyone finding this question who is looking for a way to grab OG (open graph) metadata values using the browser console (Chrome or other) can do it using ES6 JavaScript.

Example:

To grab the "description" tag, (which will also return the site byline for WordPress website) use this one-liner code snippet I wrote to do just that:

`document.querySelectorAll('meta[property="og:description"]')[0]`

This does not address grabbing stuff remotely off a server with Ajax, this is simply a browser-based solution.

Here is another quick example. Let's say you want to grab all the metadata properties and store them in an object that can be passed. This is most easily tested on a good WordPress website, but should work wherever there are open graph meta tags.
