# openGraphScraper

A simple node module(with TypeScript declarations) for scraping Open Graph and Twitter Card and other metadata off a site.

Note: `open-graph-scraper` doesn't support browser usage at this time but you can use `open-graph-scraper-lite` if you already have the `HTML` and can't use Node's [Fetch API](https://nodejs.org/dist/latest-v18.x/docs/api/globals.html#fetch).

## Installation

[](https://github.com/jshemas/openGraphScraper#installation)

```shell
npm install open-graph-scraper --save
```

## Usage

[](https://github.com/jshemas/openGraphScraper#usage)

```js
const ogs = require('open-graph-scraper');
const options = { url: 'http://ogp.me/' };
ogs(options)
  .then((data) => {
    const { error, html, result, response } = data;
    console.log('error:', error);  // This returns true or false. True if there was an error. The error itself is inside the result object.
    console.log('html:', html); // This contains the HTML of page
    console.log('result:', result); // This contains all of the Open Graph results
    console.log('response:', response); // This contains response from the Fetch API
  })
```

## Results JSON

[](https://github.com/jshemas/openGraphScraper#results-json)

Check the return for a `success` flag. If success is set to true, then the url input was valid. Otherwise it will be set to false. The above example will return something like...

```js
{
  ogTitle: 'Open Graph protocol',
  ogType: 'website',
  ogUrl: 'https://ogp.me/',
  ogDescription: 'The Open Graph protocol enables any web page to become a rich object in a social graph.',
  ogImage: [
    {
      height: '300',
      type: 'image/png',
      url: 'https://ogp.me/logo.png',
      width: '300'
    }
  ],
  charset: 'utf-8',
  requestUrl: 'http://ogp.me/',
  success: true
}
```

## Options

[](https://github.com/jshemas/openGraphScraper#options)

|Name|Info|Default Value|Required|
|---|---|---|---|
|url|URL of the site.||x|
|html|You can pass in an HTML string to run ogs on it. (use without options.url)|||
|fetchOptions|Options that are used by the Fetch API|{}||
|timeout|Request timeout for Fetch (Default is 10 seconds)|10||
|blacklist|Pass in an array of sites you don't want ogs to run on.|[]||
|onlyGetOpenGraphInfo|Only fetch open graph info and don't fall back on anything else.|false||
|customMetaTags|Here you can define custom meta tags you want to scrape.|[]||
|urlValidatorSettings|Sets the options used by validator.js for testing the URL|[Here](https://github.com/jshemas/openGraphScraper/blob/master/lib/utils.ts#L4-L17)||

Note: `open-graph-scraper` uses the [Fetch API](https://nodejs.org/dist/latest-v18.x/docs/api/globals.html#fetch) for requests and most of [Fetch's options](https://developer.mozilla.org/en-US/docs/Web/API/fetch#options) should work as `open-graph-scraper`'s `fetchOptions` options.

## Custom Meta Tag Example

[](https://github.com/jshemas/openGraphScraper#custom-meta-tag-example)

```js
const ogs = require('open-graph-scraper');
const options = {
  url: 'https://github.com/jshemas/openGraphScraper',
  customMetaTags: [{
    multiple: false, // is there more than one of these tags on a page (normally this is false)
    property: 'hostname', // meta tag name/property attribute
    fieldName: 'hostnameMetaTag', // name of the result variable
  }],
};
ogs(options)
  .then((data) => {
    const { result } = data;
    console.log('hostnameMetaTag:', result.customMetaTags.hostnameMetaTag); // hostnameMetaTag: github.com
  })
```

## HTML Example

[](https://github.com/jshemas/openGraphScraper#html-example)

```js
const ogs = require('open-graph-scraper');
const options = {
  html: `<html><head>
  <link rel="icon" type="image/png" href="https://bar.com/foo.png" />
  <meta charset="utf-8" />
  <meta property="og:description" name="og:description" content="html description example" />
  <meta property="og:image" name="og:image" content="https://www.foo.com/bar.jpg" />
  <meta property="og:title" name="og:title" content="foobar" />
  <meta property="og:type" name="og:type" content="website" />
  </head></html>`
};
ogs(options)
  .then((data) => {
    const { result } = data;
    console.log('result:', result);
    // result: {
    //   ogDescription: 'html description example',
    //   ogTitle: 'foobar',
    //   ogType: 'website',
    //   ogImage: [ { url: 'https://www.foo.com/bar.jpg', type: 'jpg' } ],
    //   favicon: 'https://bar.com/foo.png',
    //   charset: 'utf-8',
    //   success: true
    // }
  })
```

## User Agent Example

[](https://github.com/jshemas/openGraphScraper#user-agent-example)

The request header is set to [undici](https://github.com/nodejs/undici) by default. Some sites might block this, and changing the `userAgent` might work. If not you can try [using a proxy](https://www.scrapingbee.com/blog/proxy-node-fetch/) for the request and then pass the `html` into `open-graph-scraper`.

```js
const ogs = require("open-graph-scraper");
const userAgent = 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36';
ogs({ url: 'https://www.wikipedia.org/', fetchOptions: { headers: { 'user-agent': userAgent } } })
  .then((data) => {
    const { error, html, result, response } = data;
    console.log('error:', error);  // This returns true or false. True if there was an error. The error itself is inside the result object.
    console.log('html:', html); // This contains the HTML of page
    console.log('result:', result); // This contains all of the Open Graph results
    console.log('response:', response); // This contains response from the Fetch API
  })
```

## Running the example app

[](https://github.com/jshemas/openGraphScraper#running-the-example-app)

Inside the `example` folder contains a simple express app where you can run `npm ci && npm run start` to spin up. Once the app is running, open a web browser and go to `http://localhost:3000/scraper?url=http://ogp.me/` to test it out. There is also a `Dockerfile` if you want to run this example app in a docker container.