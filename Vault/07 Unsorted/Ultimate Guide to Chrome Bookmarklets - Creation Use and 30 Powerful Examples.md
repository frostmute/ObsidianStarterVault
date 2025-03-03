---
source: https://nzouat.com/ultimate-guide-chrome-bookmarklets/
feature: "![[../03 - MEDIA & FILES/d5bf1a519d488b4b9299fa92d8888f27_MD5.png]]"
---
## What Are Chrome Bookmarklets?

So, what are bookmarklets, you ask? Well, in simple terms, bookmarklets are little snippets of JavaScript code that you can save as bookmarks in your [Chrome browser](https://www.google.com/chrome/). They’re like magic wands that let you perform all sorts of nifty actions on web pages with just a single click. Want to instantly change the background color of a page? There’s a bookmarklet for that! How about quickly extracting all the links from a [website](https://nzouat.com/)? Yep, bookmarklets have got you covered!

But that’s just the tip of the iceberg. Bookmarklets can do so much more, and the best part is that they’re super easy to create and use. So, whether you’re a tech-savvy wizard or a curious newbie, bookmarklets are here to make your browsing experience more fun and efficient.

Ready to get started? Awesome! Let’s explore the incredible world of Chrome Bookmarklets together.

### Creating and Running Bookmarklets in Chrome

Fantastic! Now that we’ve got a taste of what bookmarklets are all about, let’s dive into how we can create and run our very own bookmarklets in Chrome. Don’t worry, it’s a piece of cake! Just follow along with me, and you’ll be a bookmarklet wizard in no time.

## **How To Create Your Own Bookmarklet In Chrome**

So, you’re ready to craft your first bookmarklet, huh? Awesome! Let’s do it together:

1. **Open Chrome’s bookmarks bar**: First things first, make sure your bookmarks bar is visible in Chrome. To do that, click on the three vertical dots in the top-right corner of Chrome, hover over “Bookmarks,” and select “Show bookmarks bar.” Ta-da! You should now see the bookmarks bar right under the address bar.

![](../03%20-%20MEDIA%20&%20FILES/d5bf1a519d488b4b9299fa92d8888f27_MD5.png) 

Show Bookmarks, Chrome

1. **Create a new bookmark**: Right-click on the bookmarks bar and select “Add page.” This will open a little window where we’ll work our magic.

![](../03%20-%20MEDIA%20&%20FILES/906d919c1e59ba42aa867591e5655b9f_MD5.png)

1. **Name your bookmarklet**: In the “Name” field, give your bookmarklet a cool and catchy name. This is how it will appear on the bookmarks bar, so choose something that makes you smile.
2. **Enter the JavaScript code**: Here’s where the fun begins! In the “URL” field, type `javascript:` followed by the JavaScript code you want your bookmarklet to run. Don’t worry if you’re not a coding expert—I’ll share some awesome examples in a bit!

![](../03%20-%20MEDIA%20&%20FILES/e69442ffaf9a7fa5c062d1d485e72395_MD5.png)

1. **Save and celebrate**: Click the “Save” button, and voilà! Your very own bookmarklet is now sitting pretty on the bookmarks bar, ready for action.

## **How To Use A Bookmarklet In Chrome**

Using or running a bookmarklet is the easiest thing ever! All you have to do is:

1. **Navigate to a web page**: Open a web page where you want to use the bookmarklet. It could be any page you like — bookmarklets are super versatile!
2. **Click on the bookmarklet**: Find your bookmarklet on the bookmarks bar and give it a click. Just like that, the JavaScript code will run, and you’ll see the magic happen right before your eyes!

![](../03%20-%20MEDIA%20&%20FILES/eebcf0aed4f99de8bbe82319cf321bdf_MD5.png)

And that’s it! You’re now a bookmarklet pro 😂😂😂. But we’re not done yet — let’s take a look at some super cool bookmarklet examples that you can start using right away. Ready? Let’s go!

## **Exploring Amazing Examples Of Chrome Bookmarklets**

Alright, we’re making great progress! Now that we know how to create and run bookmarklets in Chrome, it’s time to explore some super cool and practical examples. I’ll walk you through each one, so you can start using them to enhance your browsing experience. Let’s get started!

##### **Highlight All Links on a Web Page**

Ever found yourself on a content-rich web page and wished you could easily spot all the links? Well, this bookmarklet has got your back! With a single click, it’ll highlight all the links on the page in bright yellow. Here’s how to create it:

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``() {` `var` `links = document.querySelectorAll(``'a'``);` `for` `(``var` `i = 0; i < links.length; i++) { links[i].style.backgroundColor =` `'yellow'``; }})();`<br><br>`<p>`|

![](../03%20-%20MEDIA%20&%20FILES/d072806fa8275bdff6e6ba47be2d6ca9_MD5.png)

Just paste this code into the “URL” field when creating a new bookmark, and you’re good to go!  
This bookmarklet creates a custom modal styled with [Tailwind CSS](https://tailwindcss.com/). It prompts the user to enter a color or a Tailwind background color class (e.g., red, #ff0000, bg-red-500). When the user clicks the “**Submit**” button, the bookmarklet highlights the links with the specified color or class. 

To activate the bookmarklet on a specific webpage, visit the webpage and click on the bookmarklet. You will be prompted to enter the color to use to highlight the link. Once you click ok, all links will be highlighted.

![](../03%20-%20MEDIA%20&%20FILES/3a1d68f0217130973f65d1ee450973ea_MD5.png)

![](../03%20-%20MEDIA%20&%20FILES/b53e45d4d833e926db607e1e9e40fc78_MD5.png)

To deactivate the highlighting, the user can click the bookmarklet again.

##### **Quick Word Count**

Curious to know how many words are on a web page? Whether you’re doing research or checking an article’s length, this nifty bookmarklet will count all the words for you and display the total in an alert box. Here’s the code:

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``function` `createModal(wordCount){``var` `modal=document.createElement(``'div'``);modal.id=``'tw-wordcount-modal'``;modal.classList.add(``'fixed'``,``'inset-0'``,``'bg-black'``,``'bg-opacity-50'``,``'flex'``,``'items-center'``,``'justify-center'``,``'z-50'``);``var` `modalContent=document.createElement(``'div'``);modalContent.classList.add(``'bg-white'``,``'p-6'``,``'rounded-lg'``,``'shadow-xl'``);``var` `modalTitle=document.createElement(``'h3'``);modalTitle.classList.add(``'text-xl'``,``'mb-4'``);modalTitle.textContent=``'Word Count'``;``var` `modalBody=document.createElement(``'p'``);modalBody.classList.add(``'text-lg'``,``'mb-4'``);modalBody.textContent=``'Total words on this page: '``+wordCount;``var` `closeButton=document.createElement(``'button'``);closeButton.textContent=``'Close'``;closeButton.classList.add(``'mt-4'``,``'bg-blue-500'``,``'text-white'``,``'px-4'``,``'py-2'``,``'rounded'``,``'hover:bg-blue-600'``,``'cursor-pointer'``);closeButton.addEventListener(``'click'``,``function``(){document.getElementById(``'tw-wordcount-modal'``).remove();});modalContent.appendChild(modalTitle);modalContent.appendChild(modalBody);modalContent.appendChild(closeButton);modal.appendChild(modalContent);document.body.appendChild(modal);}``if``(!document.getElementById(``'tw-bookmarklet-styles'``)){``var` `link=document.createElement(``'link'``);link.rel=``'stylesheet'``;link.id=``'tw-bookmarklet-styles'``;link.href=``'[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)'``;document.head.appendChild(link);}``var` `text=document.body.innerText;``var` `wordCount=text.trim().split(``' '``).length;createModal(wordCount);})();`<br><br>`<p>`|

![Chrome Bookmqrklet - Word Count - Blog | Nzouat](../03%20-%20MEDIA%20&%20FILES/21902bf7079feff09150db5658bfa1fe_MD5.png "Chrome Bookmqrklet - Word Count - Blog | Nzouat")

##### **Extract Header Tags**

This bookmarklet extracts and lists all header tags (`<h1>` to `<h6>`) present on a web page. It provides an organized view of the headings and their hierarchy in a nice table.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``function` `createModal(){``var` `modal=document.createElement(``"div"``);modal.id=``"tw-heading-modal"``;modal.classList.add(``"fixed"``,``"inset-0"``,``"bg-black"``,``"bg-opacity-50"``,``"flex"``,``"items-center"``,``"justify-center"``,``"z-50"``);``var` `modalContent=document.createElement(``"div"``);modalContent.classList.add(``"bg-white"``,``"p-6"``,``"rounded-lg"``,``"shadow-xl"``,``"w-full"``,``"max-w-3xl"``,``"overflow-auto"``,``"max-h-screen"``);``var` `modalTitle=document.createElement(``"h3"``);modalTitle.classList.add(``"text-xl"``,``"mb-4"``);modalTitle.textContent=``"Heading Tags on the Page"``;``var` `table=document.createElement(``"table"``);table.classList.add(``"table-auto"``,``"w-full"``,``"text-left"``,``"whitespace-no-wrap"``);``var` `thead=document.createElement(``"thead"``);``var` `tr=document.createElement(``"tr"``);``var` `th=document.createElement(``"th"``);th.classList.add(``"px-4"``,``"py-2"``),th.textContent=``"Heading Level"``;``var` `th2=document.createElement(``"th"``);th2.classList.add(``"px-4"``,``"py-2"``),th2.textContent=``"Content"``;tr.appendChild(th),tr.appendChild(th2),thead.appendChild(tr),table.appendChild(thead);``var` `tbody=document.createElement(``"tbody"``);``for``(``var` `i=1;i<=6;i++){``var` `elements=document.getElementsByTagName(``"h"``+i);``for``(``var` `j=0;j<elements.length;j++){``var` `tr2=document.createElement(``"tr"``);tr2.classList.add(``"border-t"``,``"border-gray-200"``);``var` `td1=document.createElement(``"td"``);td1.classList.add(``"px-4"``,``"py-2"``),td1.textContent=``"H"``+i;``var` `td2=document.createElement(``"td"``);td2.classList.add(``"px-4"``,``"py-2"``),td2.textContent=elements[j].innerText;tr2.appendChild(td1),tr2.appendChild(td2),tbody.appendChild(tr2)}}table.appendChild(tbody),modalContent.appendChild(modalTitle),modalContent.appendChild(table);``var` `closeButton=document.createElement(``"button"``);closeButton.textContent=``"Close"``,closeButton.classList.add(``"mt-4"``,``"bg-blue-500"``,``"text-white"``,``"px-4"``,``"py-2"``,``"rounded"``,``"hover:bg-blue-600"``,``"cursor-pointer"``),closeButton.addEventListener(``"click"``,(``function``(){document.getElementById(``"tw-heading-modal"``).remove()})),modalContent.appendChild(closeButton),modal.appendChild(modalContent),document.body.appendChild(modal)}``if``(!document.getElementById(``"tw-bookmarklet-styles"``)){``var` `link=document.createElement(``"link"``);link.rel=``"stylesheet"``,link.id=``"tw-bookmarklet-styles"``,link.href=``"[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)"``,document.head.appendChild(link)}createModal();})();`<br><br>`<p>`|

![](../03%20-%20MEDIA%20&%20FILES/01c4f1e36cf46c42dc2d1ac76a96da60_MD5.png)

This bookmarklet calculates the word count of the page and displays it inside a custom modal styled with Tailwind CSS. The modal includes a title indicating “Word Count,” a body displaying the calculated word count (e.g., “Total words on this page: 500”), and a “Close” button that allows you to close the modal.

##### **Generate a QR Code for the Current Page**

Want to share a web page with a friend or quickly open it on your phone? This bookmarklet generates a QR code for the current URL, making it super easy to share or access the page on other devices. Here’s how to create it:

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``() {` `let` `qrUrl =` `'[https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=)'` `+ encodeURIComponent(location.href);` `let` `modal = document.createElement(``'div'``); modal.className =` `'fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50'``;` `let` `qrImage = document.createElement(``'img'``); qrImage.src = qrUrl;` `let` `closeButton = document.createElement(``'button'``); closeButton.textContent =` `'Close'``; closeButton.className =` `'bg-blue-500 text-white px-4 py-2 rounded-md'``; closeButton.addEventListener(``'click'``,` `function``() { modal.remove(); }); modal.appendChild(qrImage); modal.appendChild(closeButton); document.body.appendChild(modal); })();`<br><br>`<p>`|

Just click the bookmarklet, and a new tab will open with the QR code. Simple, right?

![](../03%20-%20MEDIA%20&%20FILES/ec8ada98998e6ea4534f30d97b4195ae_MD5.png)

##### **Identify Redirects**

Easily identify and analyze redirects on your web page with this bookmarklet. It fetches the current URL and provides information about the HTTP status code and any redirect locations.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``function` `createModal(t,e){``var` `n=document.createElement(``"div"``);n.id=``"tw-redirect-modal"``,n.classList.add(``"fixed"``,``"inset-0"``,``"bg-black"``,``"bg-opacity-50"``,``"flex"``,``"items-center"``,``"justify-center"``,``"z-50"``),n.addEventListener(``"click"``,(``function``(t){t.target.id===``"tw-redirect-modal"``&&n.remove()}));``var` `a=document.createElement(``"div"``);a.classList.add(``"bg-white"``,``"p-6"``,``"rounded-lg"``,``"shadow-xl"``,``"w-full"``,``"max-w-3xl"``,``"overflow-auto"``,``"max-h-screen"``);``var` `o=document.createElement(``"h3"``);o.classList.add(``"text-xl"``,``"mb-4"``),o.textContent=``"HTTP Redirect Checker"``;``var` `r=document.createElement(``"p"``);r.classList.add(``"text-lg"``,``"mb-4"``),r.textContent=t,r.style.color=e;``var` `i=document.createElement(``"button"``);i.textContent=``"Close"``,i.classList.add(``"mt-4"``,``"bg-blue-500"``,``"text-white"``,``"px-4"``,``"py-2"``,``"rounded"``,``"hover:bg-blue-600"``,``"cursor-pointer"``),i.addEventListener(``"click"``,(``function``(){n.remove()})),a.appendChild(o),a.appendChild(r),a.appendChild(i),n.appendChild(a),document.body.appendChild(n)}``if``(!document.getElementById(``"tw-bookmarklet-styles"``)){``var` `t=document.createElement(``"link"``);t.rel=``"stylesheet"``,t.id=``"tw-bookmarklet-styles"``,t.href=``"[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)"``,document.head.appendChild(t)}fetch(location.href,{redirect:``"manual"``}).then(t=>{``var` `e=t.status;e>=300&&e<400?(createModal(``"HTTP Status Code: "``+e,``"black"``),createModal(``"Redirect Location: "``+t.headers.get(``"Location"``),``"blue"``)):createModal(``"No redirect detected."``,``"green"``)}).``catch``(t=>createModal(``"Request failed: "``+t,``"red"``))})();`<br><br>`<p>`|

##### **Highlight NoFollow Links**

Quickly highlight all “nofollow” links on a web page with this bookmarklet. It visually distinguishes these links, making it easy to identify them during an SEO audit. You will be prompted with a modal to enter the color of the background and the border for the links to be highlighted on the page.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``function` `createModal(t,e){``var` `n=document.createElement(``"div"``);n.id=``"tw-redirect-modal"``,n.classList.add(``"fixed"``,``"inset-0"``,``"bg-black"``,``"bg-opacity-50"``,``"flex"``,``"items-center"``,``"justify-center"``,``"z-50"``),n.addEventListener(``"click"``,(``function``(t){t.target.id===``"tw-redirect-modal"``&&n.remove()}));``var` `a=document.createElement(``"div"``);a.classList.add(``"bg-white"``,``"p-6"``,``"rounded-lg"``,``"shadow-xl"``,``"w-full"``,``"max-w-3xl"``,``"overflow-auto"``,``"max-h-screen"``);``var` `o=document.createElement(``"h3"``);o.classList.add(``"text-xl"``,``"mb-4"``),o.textContent=``"HTTP Redirect Checker"``;``var` `r=document.createElement(``"p"``);r.classList.add(``"text-lg"``,``"mb-4"``),r.textContent=t,r.style.color=e;``var` `i=document.createElement(``"button"``);i.textContent=``"Close"``,i.classList.add(``"mt-4"``,``"bg-blue-500"``,``"text-white"``,``"px-4"``,``"py-2"``,``"rounded"``,``"hover:bg-blue-600"``,``"cursor-pointer"``),i.addEventListener(``"click"``,(``function``(){n.remove()})),a.appendChild(o),a.appendChild(r),a.appendChild(i),n.appendChild(a),document.body.appendChild(n)}``if``(!document.getElementById(``"tw-bookmarklet-styles"``)){``var` `t=document.createElement(``"link"``);t.rel=``"stylesheet"``,t.id=``"tw-bookmarklet-styles"``,t.href=``"[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)"``,document.head.appendChild(t)}fetch(location.href,{redirect:``"manual"``}).then(t=>{``var` `e=t.status;e>=300&&e<400?(createModal(``"HTTP Status Code: "``+e,``"black"``),createModal(``"Redirect Location: "``+t.headers.get(``"Location"``),``"blue"``)):createModal(``"No redirect detected."``,``"green"``)}).``catch``(t=>createModal(``"Request failed: "``+t,``"red"``))})();`<br><br>`<p>`|

##### **Display Image Alt Attributes**

Efficiently review the alt attributes of images on your web page with this bookmarklet. It generates an overlay displaying the alt text for each image, making it simple to assess image accessibility.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``if``(!document.getElementById(``"tw-bookmarklet-styles"``)){``var` `e=document.createElement(``"link"``);e.rel=``"stylesheet"``,e.id=``"tw-bookmarklet-styles"``,e.href=``"[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)"``,document.head.appendChild(e)}``var` `t=document.createElement(``"div"``);t.id=``"tw-img-stats-modal"``,t.classList.add(``"fixed"``,``"inset-0"``,``"bg-black"``,``"bg-opacity-50"``,``"flex"``,``"items-center"``,``"justify-center"``,``"z-50"``),t.addEventListener(``"click"``,(``function``(e){e.target.id===``"tw-img-stats-modal"``&&t.remove()}));``var` `n=document.createElement(``"div"``);n.classList.add(``"bg-white"``,``"p-6"``,``"rounded-lg"``,``"shadow-xl"``,``"w-full"``,``"max-w-3xl"``,``"overflow-auto"``,``"max-h-screen"``);``var` `a=document.createElement(``"h3"``);a.classList.add(``"text-xl"``,``"mb-4"``),a.textContent=``"Image Stats"``;``var` `c=document.createElement(``"table"``);c.classList.add(``"w-full"``,``"text-left"``,``"border-collapse"``,``"border"``,``"border-gray-300"``,``"rounded-md"``),c.innerHTML=``"<thead><tr><th class='border border-gray-300 px-4 py-2 bg-gray-100'>Image Src</th><th class='border border-gray-300 px-4 py-2 bg-gray-100'>Alt Text</th><th class='border border-gray-300 px-4 py-2 bg-gray-100'>Preview</th><th class='border border-gray-300 px-4 py-2 bg-gray-100'>Actions</th></tr></thead><tbody></tbody>"``;``var` `r=c.querySelector(``"tbody"``),o=document.querySelectorAll(``"img"``);``for``(``let` `e of o){``var` `s=e.src\|``"N/A"``,i=e.alt\|``"No alt text"``,d=document.createElement(``"tr"``);d.innerHTML=``'<td class="border border-gray-300 px-4 py-2 break-all">'``+s+``'</td><td class="border border-gray-300 px-4 py-2 break-all">'``+i+``'</td><td class="border border-gray-300 px-4 py-2"><img src="'``+s+``'" alt="'``+i+``'" class="w-16 h-auto inline-block object-cover"></td><td class="border border-gray-300 px-4 py-2"><a href="'``+s+``'" target="_blank" class="text-blue-500 hover:underline">View Image</a></td>'``,r.appendChild(d)}``var` `l=document.createElement(``"button"``);l.textContent=``"Close"``,l.classList.add(``"mt-4"``,``"bg-blue-500"``,``"text-white"``,``"px-4"``,``"py-2"``,``"rounded"``,``"hover:bg-blue-600"``,``"cursor-pointer"``),l.addEventListener(``"click"``,(``function``(){t.remove()})),n.appendChild(a),n.appendChild(c),n.appendChild(l),t.appendChild(n),document.body.appendChild(t)})();`<br><br>`<p>`|

##### **Utilizing Schema Markup for Enhanced SERP Presence**

Another important aspect of SEO is the use of schema markup. Schema markup is a form of structured data that helps search engines better understand the content of your web page. By implementing schema markup, you can enhance the way your website appears in search engine results pages (SERPs) and improve click-through rates.

Consider using the following bookmarklet to assess whether your web page contains schema markup:

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``let` `modal=document.createElement(``'div'``);modal.className=``'fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50'``;modal.addEventListener(``'click'``,``function``(event){event.target===modal&&modal.remove()});``let` `container=document.createElement(``'div'``);container.className=``'relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto'``;container.style.maxHeight=``'80vh'``;container.style.overflow=``'auto'``;``let` `title=document.createElement(``'h2'``);title.className=``'text-xl font-semibold mb-4'``;title.textContent=``'Schema Markup (JSON-LD) Detected:'``;container.appendChild(title);``let` `jsonLdScripts=document.querySelectorAll(``'script[type="application/ld+json"]'``);``if``(jsonLdScripts.length>0){jsonLdScripts.forEach(script=>{``let` `data=document.createElement(``'pre'``);data.className=``'bg-gray-100 p-4 my-4'``;data.textContent=JSON.stringify(JSON.parse(script.textContent),``null``,2);container.appendChild(data);});}``else``{``let` `message=document.createElement(``'p'``);message.textContent=``'No schema markup (JSON-LD) detected.'``;container.appendChild(message);}``let` `closeButton=document.createElement(``'button'``);closeButton.className=``'absolute top-4 right-4 px-3 py-1 bg-blue-500 text-white rounded-md'``;closeButton.textContent=``'Close'``;closeButton.addEventListener(``'click'``,``function``(){modal.remove()});container.appendChild(closeButton);modal.appendChild(container);document.body.appendChild(modal);})();`<br><br>`<p>`|

##### **Highlight External Links**

This bookmarklet identifies and highlights all external links on a web page, making it easier to distinguish between internal and outbound links. All external links will be highlighted with a light blue background and blue border.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`<p>`|

##### **Find Broken Images**

Identify broken images on a web page with this bookmarklet. It checks the loading status of each image and highlights any that fail to load.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=``function``(){``var` `e=document.createElement(``"div"``);e.className=``"fixed top-0 left-0 w-screen h-screen bg-black bg-opacity-50 flex items-center justify-center z-50"``;``var` `t=document.createElement(``"div"``);t.className=``"relative bg-white p-6 max-w-md mx-auto rounded-md shadow-xl overflow-auto"``;e.appendChild(t);``var` `n=document.createElement(``"button"``);n.textContent=``"Close"``,n.className=``"absolute top-2 right-2 bg-gray-300 p-1 rounded-md cursor-pointer"``,e.appendChild(n),n.addEventListener(``"click"``,``function``(){e.remove()}),e.addEventListener(``"click"``,``function``(t){t.target===e&&e.remove()}),document.body.appendChild(e);``return` `t}(),n=document.createElement(``"ul"``),o=document.querySelectorAll(``"img"``);``for``(``let` `e of o)e.addEventListener(``"error"``,``function``(){e.style.border=``"2px solid red"``;``var` `o=document.createElement(``"li"``);o.textContent=``"Broken Image: "``+e.src,n.appendChild(o)});``var` `l=t;l.innerHTML=``'<div class="overflow-auto"><h2 class="text-xl font-semibold mb-4">Broken Images Detected</h2><p class="text-gray-700">The following images failed to load:</p></div>'``,l.appendChild(n)})();`<br><br>`<p>`|

##### **Show Hidden Form Fields**

Reveal all hidden form fields on a web page with this bookmarklet. It makes hidden fields visible, allowing you to inspect their values.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;``var` `style=document.createElement(``"style"``);style.innerHTML=css;document.head.appendChild(style);``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4 overflow-auto"``;modalBg.appendChild(modal);modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&modalBg.remove()});document.body.appendChild(modalBg);``var` `table=document.createElement(``"table"``);table.className=``"table-auto w-full text-left"``;``var` `thead=document.createElement(``"thead"``);thead.innerHTML=``"<tr><th class='border px-4 py-2'>Name</th><th class='border px-4 py-2'>Value</th><th class='border px-4 py-2'>HTML Code</th></tr>"``;table.appendChild(thead);``var` `tbody=document.createElement(``"tbody"``);table.appendChild(tbody);``var` `hiddenFields=document.querySelectorAll(``'input[type="hidden"]'``);``if``(hiddenFields.length==0){modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">No Hidden Input Fields</h2><p class="text-gray-700 mb-4">There are no hidden input fields on this page.</p>'``;}``else```{modal.innerHTML=`<h2`` `class``=``"text-xl font-semibold mb-4"``>Hidden Input Fields Made Visible</h2><p` `class``=``"text-gray-700 mb-4"```>The following hidden input fields have been made visible on page: <strong>${location.href}</strong></p>`;```for``(``var` `field of hiddenFields){field.setAttribute(``"type"``,``"text"``);field.style.backgroundColor=``"lightyellow"``;``var` `tr=document.createElement(``"tr"```);tr.innerHTML=`<td`` `class``=``'border px-4 py-2'``>${field.name}</td><td` `class``=``'border px-4 py-2'``>${field.value}</td><td` `class``=``'border px-4 py-2'```>${field.outerHTML}</td>`;tbody.appendChild(tr);}modal.appendChild(table);}```var` `btnClose=document.createElement(``"button"``);btnClose.textContent=``"Close"``;btnClose.className=``"bg-gray-300 p-1 rounded-md mt-4 self-end"``;btnClose.addEventListener(``"click"``,``function``(){modalBg.remove()});modal.appendChild(btnClose);})();`<br><br>`<p>`|

##### **View Cookies for Current Site**

Display all cookies associated with the current website with this bookmarklet. It provides an overview of cookie names and values in the browser console.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;``var` `style=document.createElement(``"style"``);style.innerHTML=css;document.head.appendChild(style);``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4 overflow-auto"``;modalBg.appendChild(modal);modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&modalBg.remove()});document.body.appendChild(modalBg);``var` `ul=document.createElement(``"ul"``);ul.className=``"list-disc list-inside"``;``var` `cookies=document.cookie.split(``'; '``);``if``(cookies.length==0\|cookies[0]==``""``){modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">No Cookies Found</h2><p class="text-gray-700 mb-4">There are no cookies for this site.</p>'``;}``else``{modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Cookies for Current Site</h2><p class="text-gray-700 mb-4">The following cookies were found for this site:</p>'``;``for``(``var` `cookie of cookies){``var` `li=document.createElement(``"li"``);li.textContent=cookie;ul.appendChild(li);}modal.appendChild(ul);}``var` `btnClose=document.createElement(``"button"``);btnClose.textContent=``"Close"``;btnClose.className=``"bg-gray-300 p-1 rounded-md mt-4 self-end"``;btnClose.addEventListener(``"click"``,``function``(){modalBg.remove()});modal.appendChild(btnClose);})();`<br><br>`<p>`|

##### **Preview Meta Tags and Open Graph Tags**

Examine the meta tags and Open Graph tags of a web page with this bookmarklet. It displays the meta description, meta keywords, and Open Graph properties in the browser console, allowing you to evaluate their content.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;``var` `style=document.createElement(``"style"``);style.innerHTML=css;document.head.appendChild(style);``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4 overflow-auto"``;modalBg.appendChild(modal);modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&modalBg.remove()});document.body.appendChild(modalBg);``var` `ul=document.createElement(``"ul"``);ul.className=``"list-disc list-inside"``;``var` `metaDescription=document.querySelector(``'meta[name="description"]'``);``var` `metaKeywords=document.querySelector(``'meta[name="keywords"]'``);``var` `ogTitle=document.querySelector(``'meta[property="og:title"]'``);``var` `ogDescription=document.querySelector(``'meta[property="og:description"]'``);``var` `ogImage=document.querySelector(``'meta[property="og:image"]'``);``var` `liMetaDesc=document.createElement(``"li"``);liMetaDesc.innerHTML=``'<strong>Meta Description:</strong> '``+(metaDescription?metaDescription.content:``'Not found'``);ul.appendChild(liMetaDesc);``var` `liMetaKeywords=document.createElement(``"li"``);liMetaKeywords.innerHTML=``'<strong>Meta Keywords:</strong> '``+(metaKeywords?metaKeywords.content:``'Not found'``);ul.appendChild(liMetaKeywords);``var` `liOgTitle=document.createElement(``"li"``);liOgTitle.innerHTML=``'<strong>Open Graph Title:</strong> '``+(ogTitle?ogTitle.content:``'Not found'``);ul.appendChild(liOgTitle);``var` `liOgDesc=document.createElement(``"li"``);liOgDesc.innerHTML=``'<strong>Open Graph Description:</strong> '``+(ogDescription?ogDescription.content:``'Not found'``);ul.appendChild(liOgDesc);``var` `liOgImage=document.createElement(``"li"``);liOgImage.innerHTML=``'<strong>Open Graph Image:</strong> '``+(ogImage?ogImage.content:``'Not found'``);ul.appendChild(liOgImage);modal.appendChild(ul);``var` `btnClose=document.createElement(``"button"``);btnClose.textContent=``"Close"``;btnClose.className=``"bg-gray-300 p-1 rounded-md mt-4 self-end"``;btnClose.addEventListener(``"click"``,``function``(){modalBg.remove()});modal.appendChild(btnClose);})();`<br><br>`<p>`|

##### **Check Robots.txt File**

Quickly access the robots.txt file of the current website with this bookmarklet. It provides you with a link to navigate directly to the robots.txt file, enabling you to assess the directives for web crawlers.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(t);``var` `e=``function``(){``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `e=document.createElement(``"div"``);e.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(e);``var` `n=document.createElement(``"div"``);n.className=``"overflow-auto max-h-96"``,e.appendChild(n);``var` `o=document.createElement(``"button"``);o.textContent=``"Close"``,o.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,e.appendChild(o),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),o.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t);``return` `n}(),n=document.createElement(``"pre"``),o=location.protocol+``"//"``+location.hostname+``"/robots.txt"``;fetch(o).then(``function``(t){``return` `t.text()}).then(``function``(t){n.textContent=t,e.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Robots.txt Content</h2><p class="text-gray-700 mb-4">The content of the robots.txt file is shown below:</p><a href="'``+o+``'" target="_blank" class="text-blue-500 mb-4">Open robots.txt in a new tab</a>'``,e.appendChild(n)}).``catch``(``function``(t){console.warn(``"Error fetching robots.txt:"``,t)})})();`<br><br>`<p>`|

##### **Test Responsiveness of Web Page**

Verify the responsiveness of a web page by viewing it in different device sizes with this bookmarklet. It simulates opening the page in a new window (in the background) and offers multiple screen resolutions status.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``,document.head.appendChild(t);``var` `e=document.createElement(``"div"``);e.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col"``,e.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-y-auto flex-1 mb-4"``,n.appendChild(o);``var` `c=document.createElement(``"ul"``);c.className=``"list-disc list-inside"``;``var` `i=[320,480,768,1024,1440];i.forEach((``function``(t){``var` `e=document.createElement(``"li"``);e.textContent=``"Screen width: "``+t+``"px - "``;``var` `i=document.createElement(``"span"``);document.documentElement.clientWidth>=t?(i.textContent=``"Responsive"``,i.className=``"text-green-500 font-bold"``):(i.textContent=``"Not Responsive"``,i.className=``"text-red-500 font-bold"``),e.appendChild(i),c.appendChild(e)})),o.appendChild(c);``var` `r=document.createElement(``"button"``);r.textContent=``"Close"``,r.className=``"bg-blue-500 text-white p-1 rounded-md self-end"``,r.addEventListener(``"click"``,(``function``(){e.remove()})),n.appendChild(r),e.addEventListener(``"click"``,(``function``(t){t.target===e&&e.remove()})),document.body.appendChild(e)})();`<br><br>`<p>`|

##### **Find Duplicate Content on Page**

Identify any duplicate content on a web page with this bookmarklet. It checks for repeated text and provides a summary of the duplicates in a nice table sorted by word counts in descending order.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(t);``var` `e=document.createElement(``"div"``);e.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;e.appendChild(n);``var` `a=document.createElement(``"div"``);a.className=``"overflow-auto max-h-96"``,n.appendChild(a);``var` `o=document.createElement(``"table"``);o.className=``"w-full text-left table-auto"``,a.appendChild(o);``var` `r=document.createElement(``"thead"``),c=document.createElement(``"tr"``);r.appendChild(c);``var` `l=document.createElement(``"th"``);l.textContent=``"Word"``,l.className=``"px-4 py-2"``,c.appendChild(l);``var` `d=document.createElement(``"th"``);d.textContent=``"Count"``,d.className=``"px-4 py-2"``,c.appendChild(d),o.appendChild(r);``var` `s=document.createElement(``"tbody"``),i=document.body.innerText.split(/\s+/),u={};i.forEach(``function``(t){u[t]=(u[t]\|0)+1});``var` `m=Object.entries(u).filter(``function``(t){``return` `t[1]>1});m.sort(``function``(a,b){``return` `b[1]-a[1]});m.forEach(``function``(t){``var` `e=document.createElement(``"tr"``),n=document.createElement(``"td"``);n.textContent=t[0],n.className=``"border px-4 py-2"``,e.appendChild(n);``var` `a=document.createElement(``"td"``);a.textContent=t[1],a.className=``"border px-4 py-2"``,e.appendChild(a),s.appendChild(e)}),o.appendChild(s);``var` `f=document.createElement(``"button"``);f.textContent=``"Close"``,f.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,n.appendChild(f),f.addEventListener(``"click"``,``function``(){e.remove()}),e.addEventListener(``"click"``,``function``(t){t.target===e&&e.remove()}),document.body.appendChild(e)})();`<br><br>`<p>`|

##### **List All CSS Stylesheets**

Generate a list of all CSS stylesheets linked to the current web page with this bookmarklet. It displays the URLs of the stylesheets, providing an overview of the styles being applied to the page. Each stylesheet is displayed as a clickable link that opens in a new tab when clicked.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(t);``var` `e=document.createElement(``"div"``);e.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;e.appendChild(n);``var` `a=document.createElement(``"div"``);a.className=``"overflow-auto max-h-96"``,n.appendChild(a);``var` `o=document.createElement(``"ul"``),r=document.querySelectorAll(``'link[rel="stylesheet"]'``);r.forEach(``function``(t){``var` `e=document.createElement(``"li"``),n=document.createElement(``"a"``);n.href=t.href,n.textContent=t.href,n.target=``"_blank"``,e.appendChild(n),o.appendChild(e)}),a.appendChild(o);``var` `c=document.createElement(``"button"``);c.textContent=``"Close"``,c.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,n.appendChild(c),c.addEventListener(``"click"``,``function``(){e.remove()}),e.addEventListener(``"click"``,``function``(t){t.target===e&&e.remove()}),document.body.appendChild(e)})();`<br><br>`<p>`|

##### **View JavaScript Errors on Page**

Detect JavaScript errors on a web page with this bookmarklet. It opens the browser’s console and filters to display only error messages, helping you identify and troubleshoot JavaScript issues. 

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});document.body.appendChild(modalBg);``return``{modal:modal,close:closeModal}};``var` `errorModal=createModal();errorModal.modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">JavaScript Errors:</h2><table class="w-full text-left"><thead><tr><th class="border px-2 py-1">Message</th><th class="border px-2 py-1">Source</th><th class="border px-2 py-1">Line</th><th class="border px-2 py-1">Column</th></tr></thead><tbody></tbody></table><button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4" onclick="this.parentElement.parentElement.remove()">Close</button><button class="bg-red-500 text-white px-4 py-2 rounded-md mt-4 ml-4" onclick="triggerTestError()">Test Error</button>'``;``var` `tbody=errorModal.modal.querySelector(``"tbody"``);window.onerror=``function``(message,source,lineno,colno,error){``var` `tr=document.createElement(``"tr"``);tr.innerHTML=``'<td class="border px-2 py-1">'``+message+``'</td><td class="border px-2 py-1"><a href="'``+source+``'" target="_blank">'``+source+``'</a></td><td class="border px-2 py-1">'``+lineno+``'</td><td class="border px-2 py-1">'``+colno+``'</td>'``;tbody.appendChild(tr)};window.triggerTestError=``function``(){``throw` `new` `Error(``"This is a test error."``)}})();`<br><br>`<p>`|

##### **Highlight All Images Without Alt Attributes**

Identify images without alt attributes on a web page with this bookmarklet. It highlights such images and provides a visual indication of images that may impact accessibility.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});document.body.appendChild(modalBg);``return``{modal:modal,close:closeModal}};``var` `colorModal=createModal();``var` `colorForm=document.createElement(``"form"``);colorForm.innerHTML=``'<label class="block mb-2">Highlight Color: <input type="color" name="highlightColor" class="border"></label><button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded-md">Submit</button>'``;colorModal.modal.appendChild(colorForm);colorForm.addEventListener(``"submit"``,``function``(e){e.preventDefault();``var` `color=e.target.elements.highlightColor.value;colorModal.close();``var` `images=document.querySelectorAll(``'img:not([alt])'``);``var` `infoModal=createModal();infoModal.modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Images without Alt Attributes</h2><table class="w-full text-left"><thead><tr><th class="border px-2 py-1">Image</th><th class="border px-2 py-1">URL</th></tr></thead><tbody></tbody></table><button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4" onclick="this.parentElement.parentElement.remove()">Close</button>'``;``var` `tbody=infoModal.modal.querySelector(``"tbody"``);images.forEach(``function``(img){img.style.border=``"3px solid "``+color;``var` `tr=document.createElement(``"tr"``);tr.innerHTML=``'<td class="border px-2 py-1"><img src="'``+img.src+``'" style="max-width:100px;max-height:100px;"></td><td class="border px-2 py-1"><a href="'``+img.src+``'" target="_blank">'``+img.src+``'</a></td>'``;tbody.appendChild(tr)})});})();`<br><br>`<p>`|

##### **Display Server Response Headers**

Examine the server response headers for the current URL with this bookmarklet. It fetches the URL and provides a summary of the response headers.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});document.body.appendChild(modalBg);``return``{modal:modal,close:closeModal}};``var` `headerModal=createModal();headerModal.modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Server Response Headers:</h2><pre class="border p-4 rounded overflow-auto max-h-96"></pre><button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4" onclick="this.parentElement.parentElement.remove()">Close</button>'``;``var` `pre=headerModal.modal.querySelector(``"pre"``);fetch(location.href,{method:``"HEAD"``}).then(``function``(response){``for``(``let``[header,value]of response.headers.entries()){pre.textContent+=header+``": "``+value+``"\\n"``}}).``catch``(``function``(error){pre.textContent=``"Request failed: "``+error})})();`<br><br>`<p>`|

##### **Generate Sitemap of Internal Links**

Create a simple sitemap of all internal links on a web page with this bookmarklet. It extracts the links and organizes them in a list format, providing an overview of the site’s structure.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});document.body.appendChild(modalBg);``return``{modal:modal,close:closeModal}};``var` `sitemapModal=createModal();sitemapModal.modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Sitemap of Internal Links:</h2><div class="border p-4 rounded overflow-auto max-h-96"></div><button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4" onclick="this.parentElement.parentElement.remove()">Close</button>'``;``var` `linksDiv=sitemapModal.modal.querySelector(``"div"``);``var` `currentDomain=window.location.hostname;``var` `links=Array.from(document.querySelectorAll(``"a"``)).filter(link=>``new` `URL(link.href).hostname===currentDomain);``var` `uniqueLinks=[...``new` `Set(links.map(link=>link.href))];uniqueLinks.forEach(``function``(link){``var` `linkElem=document.createElement(``"a"``);linkElem.href=link;linkElem.textContent=link;linkElem.className=``"block mb-2 text-blue-500"``;linksDiv.appendChild(linkElem)})})();`<br><br>`<p>`|

##### **Measure Page Load Time**

Evaluate the loading performance of a web page with this bookmarklet. It calculates the time taken for the page to load and displays the result in milliseconds.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});document.body.appendChild(modalBg);``return``{modal:modal,close:closeModal}};``var` `loadTimeModal=createModal();loadTimeModal.modal.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Page Load Time:</h2><div></div><button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4" onclick="this.parentElement.parentElement.remove()">Close</button>'``;``var` `loadTimeDiv=loadTimeModal.modal.querySelector(``"div"``);``var` `loadTime=window.performance.timing.domContentLoadedEventEnd-window.performance.timing.navigationStart;loadTimeDiv.textContent=loadTime+``" milliseconds"``;})();`<br><br>`<p>`|

##### **Analyze Anchor Text Distribution**

Evaluate the distribution of anchor text on a web page with this bookmarklet. It extracts the anchor text of all links on the page and provides a summary of their frequency in the browser.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `css=document.createElement(``"style"``);css.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(css);``var` `createModal=``function``(){``var` `modalBg=document.createElement(``"div"``);modalBg.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `modal=document.createElement(``"div"``);modal.className=``"bg-white rounded-md shadow-lg max-w-2xl mx-auto h-3/5 overflow-auto flex flex-col"``;modalBg.appendChild(modal);``var` `closeModal=``function``(){modalBg.remove()};modalBg.addEventListener(``"click"``,``function``(e){e.target===modalBg&&closeModal()});``var` `modalHeader=document.createElement(``"div"``);modalHeader.className=``"bg-gray-100 p-4 flex justify-between items-center"``;modal.appendChild(modalHeader);``var` `modalTitle=document.createElement(``"h2"``);modalTitle.className=``"text-xl font-semibold"``;modalTitle.textContent=``"Anchor Text Distribution:"``;modalHeader.appendChild(modalTitle);``var` `closeButton=document.createElement(``"button"``);closeButton.textContent=``"Close"``;closeButton.className=``"bg-blue-500 text-white px-3 py-1 rounded-md"``;closeButton.addEventListener(``"click"``,closeModal);modalHeader.appendChild(closeButton);``var` `content=document.createElement(``"div"``);content.className=``"p-4"``;modal.appendChild(content);document.body.appendChild(modalBg);``return` `content};``var` `anchorModal=createModal();``var` `anchorList=document.createElement(``"ul"``);anchorList.className=``"list-disc list-inside"``;anchorModal.appendChild(anchorList);``var` `anchors=document.querySelectorAll(``"a"``);``var` `anchorTextCount={};anchors.forEach(``function``(anchor){``var` `text=anchor.textContent.trim();anchorTextCount[text]=(anchorTextCount[text]\|0)+1});Object.entries(anchorTextCount).forEach(``function``(entry){``var` `listItem=document.createElement(``"li"``);listItem.textContent=``'"'``+entry[0]+``'": '``+entry[1]+``" occurrences"``;anchorList.appendChild(listItem)});})();`<br><br>`<p>`|

##### **Check SSL/TLS Certificate Details**

Quickly access the SSL/TLS certificate details of the current website with this bookmarklet. It opens the browser’s security information panel, allowing you to review the certificate’s validity and issuer.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``),n=window.navigator.userAgent.toLowerCase(),a=``""``;-1!==n.indexOf(``"chrome"``)?a=``"<li>Click on the lock icon next to the URL in the address bar.</li><li>Click on 'Certificate' to view SSL/TLS certificate details.</li>"``:-1!==n.indexOf(``"firefox"``)?a=``"<li>Click on the lock icon next to the URL in the address bar.</li><li>Click on the right arrow next to 'Connection secure'.</li><li>Click on 'More Information' and go to the 'Security' tab.</li><li>Click on 'View Certificate' to view SSL/TLS certificate details.</li>"``:-1!==n.indexOf(``"safari"``)&&(a=``"<li>Click on the lock icon next to the URL in the address bar.</li><li>Click on 'Show Certificate' to view SSL/TLS certificate details.</li>"``);``var` `o=location.protocol===``"https:"``?``'<p>Open your browser\'s security information panel to view SSL/TLS certificate details. Follow these steps:</p><ul>'``+a+``"</ul>"``:``'This site is not using HTTPS. No SSL/TLS certificate details available.'``;t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``,t.innerHTML=``'<div class="bg-white rounded-md shadow-lg p-6 max-w-md mx-auto relative flex flex-col space-y-4"><div class="overflow-auto max-h-60vh">'``+o+``'</div><button class="bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto" onclick="this.parentNode.parentNode.remove()">Close</button></div>'``,document.body.appendChild(t)})();`<br><br>`<p>`|

##### **Extract All Email Addresses**

Extract all email addresses present on a web page with this bookmarklet. It scans the page’s content and displays a list of found email addresses in the browser.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``),n=document.body.innerText,o=/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/g,a=n.match(o)\|[],i=a.length?``'<ul>'``+a.map(``function``(e){``return``"<li>"``+e+``"</li>"``}).join(``""``)+``"</ul>"``:``"No email addresses found."``;t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``,t.innerHTML=``'<div class="bg-white rounded-md shadow-lg p-6 max-w-md mx-auto relative flex flex-col space-y-4"><div class="overflow-auto max-h-60vh"><h2 class="text-xl font-semibold mb-4">Email Addresses Found:</h2>'``+i+``'</div><button class="bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto" onclick="this.parentNode.parentNode.remove()">Close</button></div>'``,document.body.appendChild(t)})();`<br><br>`<p>`|

##### **Display Accessibility Warnings**

Identify potential accessibility issues on a web page with this bookmarklet. It checks for common accessibility pitfalls, such as missing alt attributes and improper header structure, and provides warnings in the browser .

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-auto max-h-60vh"``;n.appendChild(o);``var` `a=document.createElement(``"button"``);a.textContent=``"Close"``,a.className=``"bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto"``,n.appendChild(a),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),a.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t),o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Accessibility Warnings:</h2>'``,``function``(){``var` `e=document.querySelectorAll(``"img:not([alt])"``);e.length>0&&(o.innerHTML+=``'<p class="text-red-600">Images without alt attributes detected.</p>'``);``var` `t=[``"H1"``,``"H2"``,``"H3"``,``"H4"``,``"H5"``,``"H6"``],n=0;t.forEach((``function``(t,e){``if``(document.getElementsByTagName(t).length>0){e>n+1&&(o.innerHTML+=``'<p class="text-red-600">Improper header structure detected: '``+t+``" follows H"``+(e+1)+``".</p>"``),n=e}}))}()})();`<br><br>`<p>`|

##### **View Cache-Control Headers**

Determine the cache-control headers set for the current web page with this bookmarklet. It fetches the current webpage using an HTTP HEAD request and displays the value of the ‘cache-control’ header. If the ‘cache-control’ header is not found, it displays a message indicating that no ‘cache-control’ headers were found.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-auto max-h-60vh"``;n.appendChild(o);``var` `a=document.createElement(``"button"``);a.textContent=``"Close"``,a.className=``"bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto"``,n.appendChild(a),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),a.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t),fetch(location.href,{method:``"HEAD"``}).then(``function``(e){o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Cache-Control Headers:</h2>'``;``var` `t=e.headers.get(``"cache-control"``);t?o.innerHTML+=t:o.innerHTML+=``"No cache-control headers found."``}).``catch``(``function``(e){o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Request failed:</h2>'``+e})})();`<br><br>`<p>`|

##### **Check for Mixed Content**

Identify mixed content on a web page with this bookmarklet. It detects insecure HTTP resources on an HTTPS page and provides a list of such resources in the browser. If no mixed content is detected, the modal indicates that as well. If the page is not using HTTPS, the modal states that the mixed content check is not applicable.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-auto max-h-60vh"``;n.appendChild(o);``var` `a=document.createElement(``"button"``);a.textContent=``"Close"``,a.className=``"bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto"``,n.appendChild(a),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),a.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t),o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Mixed Content Check:</h2>'``,``function``(){``if``(location.protocol===``"https:"``){``var` `e=[];document.querySelectorAll(``'link[href^="http:"], script[src^="http:"], img[src^="http:"]'``).forEach((``function``(t){e.push(t.href\|t.src)})),e.length>0?(o.innerHTML+=``'<p class="text-red-600">Mixed Content Detected:</p>'``,e.forEach((``function``(e){o.innerHTML+=``'<p class="text-gray-700">'``+e+``"</p>"``}))):o.innerHTML+=``'<p class="text-green-600">No mixed content detected.</p>'``}``else` `o.innerHTML+=``'<p class="text-yellow-600">This page is not using HTTPS. Mixed content check is not applicable.</p>'``}()})();`<br><br>`<p>`|

##### **List All Iframes on Page**

Generate a list of all iframes present on a web page with this bookmarklet. It displays the source URLs of the iframes, providing an overview of the embedded content on the page.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-auto max-h-60vh"``;n.appendChild(o);``var` `a=document.createElement(``"button"``);a.textContent=``"Close"``,a.className=``"bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto"``,n.appendChild(a),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),a.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t),o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Iframes on Page:</h2>'``,``function``(){``var` `e=document.querySelectorAll(``"iframe"``);e.length>0?e.forEach((``function``(e){o.innerHTML+=``'<p class="text-gray-700">'``+e.src+``"</p>"``})):o.innerHTML+=``'<p class="text-yellow-600">No iframes found on the page.</p>'``}()})();`<br><br>`<p>`|

##### **Display Social Media Meta Tags**

Examine the social media meta tags of a web page with this bookmarklet. It retrieves and displays the Open Graph and Twitter Card meta tags in the browser console, allowing you to assess their content.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `e=document.createElement(``"style"``);e.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(e);``var` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``;``var` `n=document.createElement(``"div"``);n.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto flex flex-col space-y-4"``;t.appendChild(n);``var` `o=document.createElement(``"div"``);o.className=``"overflow-auto max-h-60vh"``;n.appendChild(o);``var` `a=document.createElement(``"button"``);a.textContent=``"Close"``,a.className=``"bg-blue-500 text-white px-4 py-2 rounded-md self-start mt-auto"``,n.appendChild(a),t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()}),a.addEventListener(``"click"``,``function``(){t.remove()}),document.body.appendChild(t),o.innerHTML=``'<h2 class="text-xl font-semibold mb-4">Social Media Meta Tags:</h2>'``,``function``(){``var` `e=document.querySelectorAll(``'meta[property^="og:"]'``),t=document.querySelectorAll(``'meta[name^="twitter:"]'``);(e.length>0\|t.length>0)?(e.forEach((``function``(e){o.innerHTML+=``'<p class="text-gray-700">'``+e.getAttribute(``"property"``)+``": "``+e.content+``"</p>"``})),t.forEach((``function``(e){o.innerHTML+=``'<p class="text-gray-700">'``+e.getAttribute(``"name"``)+``": "``+e.content+``"</p>"``}))):o.innerHTML+=``'<p class="text-yellow-600">No social media meta tags found on the page.</p>'``}()})();`<br><br>`<p>`|

##### **Display Mobile Viewport Meta Tag**

Review the mobile viewport meta tag of a web page with this bookmarklet. It retrieves the viewport meta tag and displays its content in the browser console, allowing you to assess the viewport settings for mobile devices.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``let` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``,document.head.appendChild(t);``let` `e=``function``(){``let` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``,t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()});``let` `e=document.createElement(``"div"``);e.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto"``;``let` `n=document.createElement(``"div"``);n.className=``"overflow-auto max-h-96"``;``let` `o=document.createElement(``"button"``);o.textContent=``"Close"``,o.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,o.addEventListener(``"click"``,``function``(){t.remove()});``let` `r=document.createElement(``"table"``);r.className=``"table-auto"``;``let` `c=document.createElement(``"thead"``),s=document.createElement(``"tr"``),a=document.createElement(``"th"``);a.textContent=``"Mobile Viewport Meta Tag"``,s.appendChild(a),c.appendChild(s),r.appendChild(c);``let` `i=document.createElement(``"tbody"``);``let` `d=document.querySelector(``'meta[name="viewport"]'```);d?i.innerHTML=`<tr><td>${d.content}</td></tr>`:i.innerHTML=```"<tr><td>No mobile viewport meta tag found.</td></tr>"``,r.appendChild(i),e.appendChild(r),e.appendChild(o),e.appendChild(n),t.appendChild(e),document.body.appendChild(t)};e()})();`<br><br>`<p>`|

##### **Detect Redirects**

Detect HTTP redirects for the current URL with this bookmarklet. It performs a fetch request and identifies any redirects, providing details in the browser.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``let` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(t);``let` `e=``function``(){``let` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``,t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()});``let` `e=document.createElement(``"div"``);e.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto"``;``let` `n=document.createElement(``"button"``);n.textContent=``"Close"``,n.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,n.addEventListener(``"click"``,``function``(){t.remove()});``let` `o=document.createElement(``"pre"``);fetch(location.href,{redirect:``"manual"``}).then(t=>{t.type===``"opaqueredirect"```?o.textContent=`Redirect detected. Redirect URL: ${t.url}`:o.textContent=```"No redirect detected."``}).``catch``(t=>{console.warn(``"Request failed:"``,t)}),e.appendChild(o),e.appendChild(n),t.appendChild(e),document.body.appendChild(t)};e()})();`<br><br>`<p>`|

##### **Extract Schema Markup Data**

Analyze the Schema markup data (structured data) present on a web page with this bookmarklet. It retrieves and displays the JSON-LD or Microdata structured data in the browser console, allowing you to assess the markup used for search engine optimization.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``let` `t=document.createElement(``"style"``);t.innerHTML=``"@import url('[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)')"``;document.head.appendChild(t);``let` `e=``function``(){``let` `t=document.createElement(``"div"``);t.className=``"fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"``,t.addEventListener(``"click"``,``function``(e){e.target===t&&t.remove()});``let` `e=document.createElement(``"div"``);e.className=``"relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto"``;``let` `n=document.createElement(``"button"``);n.textContent=``"Close"``,n.className=``"bg-blue-500 text-white px-3 py-1 rounded-md self-start mt-auto"``,n.addEventListener(``"click"``,``function``(){t.remove()});``let` `o=document.createElement(``"pre"``);console.log(``"Schema Markup Data:"``);``let` `i=document.querySelectorAll(``'script[type="application/ld+json"]'``),r=document.querySelectorAll(``'[itemscope]'``);i.length>0&&(console.log(``"JSON-LD Structured Data:"``),i.forEach(e=>{``let` `t=document.createElement(``"div"``);t.textContent=e.textContent,o.appendChild(t)})),r.length>0&&(console.log(``"Microdata Structured Data:"``),r.forEach(e=>{``let` `t=document.createElement(``"div"``);t.textContent=e.outerHTML,o.appendChild(t)})),0===i.length&&0===r.length&&console.log(``"No Schema markup data found."``),e.appendChild(o),e.appendChild(n),t.appendChild(e),document.body.appendChild(t)};e()})();`<br><br>`<p>`|

##### **Show Page Title and Description**

Display the title and meta description of a web page with this bookmarklet. It retrieves the title tag and meta description tag and provides their content in the browser console.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``let` `modal=document.createElement(``'div'``);modal.className=``'fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50'``;modal.addEventListener(``'click'``,``function``(event){event.target===modal&&modal.remove()});``let` `container=document.createElement(``'div'``);container.className=``'relative bg-white rounded-md shadow-lg p-6 max-w-md mx-auto'``;container.style.maxHeight=``'80vh'``;container.style.overflow=``'auto'``;``let` `title=document.createElement(``'h2'``);title.className=``'text-xl font-semibold mb-4'``;title.textContent=``'Page Title and Description'``;container.appendChild(title);``let` `table=document.createElement(``'table'``);table.className=``'border-collapse'``;``let` `row1=document.createElement(``'tr'``);``let` `row2=document.createElement(``'tr'``);``let` `col1=document.createElement(``'td'``);col1.className=``'border border-gray-300 px-4 py-2'``;col1.textContent=``'Title'``;row1.appendChild(col1);``let` `col2=document.createElement(``'td'``);col2.className=``'border border-gray-300 px-4 py-2'``;col2.textContent=document.title;row2.appendChild(col2);``let` `metaDescription=document.querySelector(``'meta[name="description"]'``);``if``(metaDescription){``let` `col3=document.createElement(``'td'``);col3.className=``'border border-gray-300 px-4 py-2'``;col3.textContent=``'Description'``;row1.appendChild(col3);``let` `col4=document.createElement(``'td'``);col4.className=``'border border-gray-300 px-4 py-2'``;col4.textContent=metaDescription.content;row2.appendChild(col4);}table.appendChild(row1);table.appendChild(row2);container.appendChild(table);modal.appendChild(container);document.body.appendChild(modal);})();`<br><br>`<p>`|

##### **List All Schema Types with Summary**

Discover and analyze all Schema types present on a web page with this bookmarklet. It extracts the JSON-LD and Microdata structured data, lists the Schema types used, and provides a summary of each Schema instance.

|   |   |
|---|---|
|1<br><br>2<br><br>3|`</p>`<br><br>`javascript:(``function``(){``var` `t=document.createElement(``"link"``);t.rel=``"stylesheet"``,t.href=``"[https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css](https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css)"``,document.head.appendChild(t);``var` `e=document.querySelectorAll(``'script[type="application/ld+json"]'``),n=document.querySelectorAll(``"[itemscope]"``),o=[];``if``(e.length>0&&e.forEach(``function``(e){``try``{``var` `n=JSON.parse(e.textContent);Array.isArray(n)?n.forEach(``function``(e){o.push(e)}):o.push(n)}``catch``(e){console.warn(``"Error parsing JSON-LD data:"``,e)}}),n.length>0&&n.forEach(``function``(e){``var` `t=e.getAttribute(``"itemtype"``),n={},r=e.querySelectorAll(``"[itemprop]"``);r.forEach(``function``(e){``var` `r=e.getAttribute(``"itemprop"``),t=e.content\|e.textContent.trim();n[r]=t}),o.push({``"@context"``:``"[https://schema.org](https://schema.org/)"``,``"@type"``:t,...n})}),o.length>0){``var` `r=document.createElement(``"div"``);r.innerHTML=``'<div class="fixed z-10 inset-0 overflow-y-auto" aria-labelledby="modal-title" role="dialog" aria-modal="true"><div class="flex items-end justify-center min-h-screen pt-4 px-4 pb-20 text-center sm:block sm:p-0"><div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" aria-hidden="true"></div><span class="hidden sm:inline-block sm:align-middle sm:h-screen" aria-hidden="true">&#8203;</span><div class="inline-block align-bottom bg-white rounded-lg text-left overflow-hidden shadow-xl transform transition-all sm:my-8 sm:align-middle sm:max-w-lg sm:w-full"><div class="bg-white px-4 pt-5 pb-4 sm:p-6 sm:pb-4"><div class="sm:flex sm:items-start"><div class="mt-3 text-center sm:mt-0 sm:text-left w-full"><h3 class="text-lg leading-6 font-medium text-gray-900" id="modal-title">Schema Types with Summary</h3><div class="mt-2">'``+o.map(``function``(e){``return``'<p class="text-sm text-gray-500"><strong>Schema Type:</strong> '``+e[``"@type"``]+``"<br><strong>Summary:</strong><br><pre>"``+JSON.stringify(e,``null``,2)+``"</pre></p>"``}).join(``""``)+``'</div></div></div><div class="bg-gray-50 px-4 py-3 sm:px-6 sm:flex sm:flex-row-reverse"><button type="button" class="mt-3 w-full inline-flex justify-center rounded-md border border-transparent shadow-sm px-4 py-2 bg-blue-600 text-base font-medium text-white hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm" onclick="this.closest(\'.fixed\').remove();">Close</button></div></div></div></div>'``,document.body.appendChild(r)}``else` `alert(``"No Schema markup data found."``)})();`<br><br>`<p>`|

These are just a few examples of the incredible things bookmarklets can do. Feel free to experiment and create your own — bookmarklets are all about making the web work for you!

Stay tuned, because up next, we’re going to address some common questions and misconceptions about Chrome Bookmarklets. Let’s bust some myths together!

## **Common Questions And Myths About Bookmarklets**

We’ve come a long way on our Chrome Bookmarklets journey, and you’re already a bookmarklet aficionado! But hey, I get it — bookmarklets can raise some questions, and there are a few misconceptions floating around. So, in this section, let’s clear the air and answer some common questions about bookmarklets. Let’s get started!

## **What is the Difference Between a Chrome Bookmarklet and a Browser Extension?**

Great question! While bookmarklets and browser extensions can both enhance your browsing experience, there are some key differences:

- **Simplicity**: Bookmarklets are simple JavaScript snippets saved as bookmarks. Browser extensions, on the other hand, are more complex and often involve multiple files and programming languages.
- **Installation**: Bookmarklets can be created and used with just a few clicks, while browser extensions require installation from a web store or developer’s website.
- **Permissions**: Bookmarklets only run when you click them, and they don’t require special permissions. Extensions may require permission to access certain data or features in your browser.

In short, bookmarklets are lightweight and easy to use, making them perfect for quick tasks and customizations!

## **Are Chrome Bookmarklets Safe To Use?**

Safety first, right? Bookmarklets are generally safe, but there are a few things to keep in mind:

- **Source**: Only use bookmarklets from trusted sources or create your own. Be cautious of bookmarklets that ask for sensitive information or perform unexpected actions.
- **Code**: Take a moment to review the JavaScript code in a bookmarklet. If something looks fishy or you don’t understand it, it’s best to steer clear.

With a little vigilance, you can safely enjoy the benefits of bookmarklets!

## **Can Bookmarklets Access My Private Data?**

**Nope**! Bookmarklets can only interact with the web page you’re currently viewing, and they can’t access your browser history, stored passwords, or other sensitive data. Rest assured, your privacy is secure!

And there you have it! I hope that clears things up and gives you confidence as you explore the world of Chrome Bookmarklets. Don’t forget, bookmarklets are all about making the web a more enjoyable and personalized place for you!

Coming up, we’ll take a look at some potential issues you might encounter with bookmarklets and how to troubleshoot them. Don’t worry, I’ve got your back!

## **Troubleshooting Common Bookmarklet Issues In Chrome**

Hey, even the best of us run into hiccups sometimes! While using Chrome Bookmarklets is usually smooth sailing, there might be moments when things don’t go as planned. But don’t worry — I’m here to help you navigate any challenges and keep your bookmarklet game strong. Let’s look at some common issues you might encounter and how to troubleshoot them.

### **“My Bookmarklet Isn’t Working!”**

Oh no! If your bookmarklet isn’t doing its magic, here are some things to check:

- **Syntax**: Make sure the bookmarklet code is correct and doesn’t have any syntax errors. A missing parenthesis or quotation mark could be the culprit.
- **Website Compatibility**: Some websites use security features like Content Security Policy (CSP) that may prevent bookmarklets from running. If that’s the case, try using the bookmarklet on a different website to see if it works.
- **Browser Version**: Make sure you’re using the latest version of Chrome. An outdated browser might affect bookmarklet functionality.

### **“I Accidentally Deleted My Bookmarklet!”**

No worries, it happens to the best of us! If you accidentally deleted a bookmarklet from your bookmarks bar, you can recreate it using the same steps we covered earlier. If you don’t remember the code, check if you have a backup or reach out to the original source for the bookmarklet.

### “The Bookmarklet Code Looks Scrambled In The Bookmark Manager!”

Chrome’s bookmark manager sometimes shows bookmarklet code as a single, scrambled line. That’s okay! You don’t need to edit it directly in the bookmark manager. If you want to modify the code, copy it into a code editor, make your changes, and then create a new bookmarklet with the updated code.

### “Can I Use Bookmarklets On Mobile Devices?”

Yes, you can! Bookmarklets can also be used on mobile browsers like Chrome for Android or Safari for iOS. The process for adding and running bookmarklets might be slightly different on mobile devices, so be sure to check the instructions for your specific device.

And that’s a wrap on troubleshooting! I hope these tips help you overcome any bookmarklet hurdles and keep you cruising smoothly.

## **Frequently Asked Questions (FAQS)**: **Chrome Bookmarklets**

****1. What is the difference between a bookmark and a bookmarklet?****

A bookmark in Chrome is a saved link to a specific web page that allows you to quickly access it later. It is similar to saving a favorite website. On the other hand, a bookmarklet is a type of bookmark that contains a piece of JavaScript code. When clicked, a bookmarklet executes the code on the current page, enabling you to perform specific actions or enhancements within the browser.

****2. What do Bookmarklets do?****

Bookmarklets are small JavaScript programs embedded within bookmarks. They add functionality to your web browsing experience by allowing you to perform tasks or modify the content of a webpage. They can be used for various purposes, such as enhancing page styling, extracting data, manipulating elements, or performing custom actions. Bookmarklets provide a convenient way to extend the capabilities of your browser without the need for installing separate extensions or plugins.

****3. What is the difference between a Chrome extension and a bookmarklet?****

A Chrome extension is a standalone program that extends the functionality of the Chrome browser. It is typically installed from the Chrome Web Store and can provide a wide range of features, including modifying webpage content, adding new UI elements, integrating with external services, and more. On the other hand, a bookmarklet is a small piece of JavaScript code that runs directly within the context of the current webpage. While bookmarklets can perform certain actions and enhancements, their functionality is more limited compared to Chrome extensions.

****4. What is the difference between a browser extension and a bookmarklet?****

The main difference between a browser extension and a bookmarklet lies in their implementation and capabilities. A browser extension is a software module that adds new features and functionality to a web browser. It has broader access to the browser’s APIs and can interact with web content, modify page structure, and integrate with external services. On the other hand, a bookmarklet is a lightweight JavaScript code snippet that runs within the scope of the current webpage. Its capabilities are more constrained, usually focused on performing specific tasks or modifications on the page itself.

****5. Do bookmarklets work in Chrome?****

Yes, bookmarklets work in Chrome. Chrome supports the use of bookmarklets and provides a convenient way to create and use them. You can add bookmarklets to your bookmarks bar or bookmark manager in Chrome, allowing you to execute the embedded JavaScript code with a single click. However, it’s important to note that bookmarklets may be subject to security restrictions depending on the website you are using them on.

****6. What does a bookmarklet look like?****

A bookmarklet is essentially a bookmark that contains JavaScript code instead of a regular URL. When viewed in the Chrome bookmark manager or bookmarks bar, a bookmarklet appears like any other bookmark. It typically has a name or description that indicates its purpose. Clicking on the bookmarklet executes the embedded JavaScript code, triggering the desired action or modification on the current webpage.

It’s been a blast exploring the world of Chrome Bookmarklets with you. As we wrap up, let’s do a quick recap and share some final thoughts on this amazing tool that can transform your browsing experience. Let’s finish strong!

### Conclusion: Unlocking the Power of Chrome Bookmarklets

Well, my friend, we’ve reached the end of our incredible journey through the land of Chrome Bookmarklets! It’s been an absolute pleasure guiding you along the way, and I’m thrilled to see you become a bookmarklet pro.

Let’s take a moment to reflect on everything we’ve learned:

- **What are bookmarklets**? We discovered that bookmarklets are small, yet powerful JavaScript snippets that you can save as bookmarks in Chrome. They’re like magical shortcuts that enhance and customize your browsing experience.
- **Creating and running bookmarklets**: We learned how to craft our own bookmarklets and run them in Chrome with just a few clicks. We explored cool examples like highlighting links, counting words, and generating QR codes.
- **Understanding and troubleshooting**: We answered common questions, busted bookmarklet myths, and learned how to troubleshoot issues. We also learned about the differences between bookmarklets and browser extensions, as well as the importance of bookmarklet safety.

With all this knowledge, you’re now equipped to explore the limitless possibilities of bookmarklets. Whether you’re boosting productivity, improving accessibility, or simply having fun, bookmarklets are here to make the web a more personalized and enjoyable place for you.

As we part ways, remember that the spirit of bookmarklets is all about creativity and curiosity. So, go forth and experiment, discover, and create bookmarklets that reflect your unique style and needs. The web is your canvas, and bookmarklets are your brushes.