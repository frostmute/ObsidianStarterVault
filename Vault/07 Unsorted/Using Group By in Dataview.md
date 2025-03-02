# Using Group By in Dataview

I'm trying to build a simple tea database of teas I drink so I can rank them and refer to it later. Dataview felt like the perfect thing to consolidate it all. I got it into a table showing the tea name, brand, and type. I noticed in some videos or forums where they had their tables sectioned out into categories. Further reading led me to the GROUP BY command. I tried this out to group by Brand and it's not the result I was expecting. Further looking into it, I could not find any examples that show one that worked. I found a video of guy explaining it's complicated and you have to use a `rows.file.name` or something which he didn't go into detail about. Not sure if this has to be done with dataviewjs?

My simple query is this:

TABLE Brand, Type FROM "Tea Dataview Test"
GROUP BY Brand

And this is the result:

[![r/ObsidianMD - Using Group By in Dataview](https://preview.redd.it/using-group-by-in-dataview-v0-nm7ht9zcbe5a1.png?width=707&format=png&auto=webp&s=34afbd7bce21aba9e7c9c4e0914053e68f1de35a)](https://preview.redd.it/using-group-by-in-dataview-v0-nm7ht9zcbe5a1.png?width=707&format=png&auto=webp&s=34afbd7bce21aba9e7c9c4e0914053e68f1de35a "Image from r/ObsidianMD - Using Group By in Dataview")

Any help would be appreciated.

Edit:

Below is a picture of what I want. Now actually thinking about it, I suppose I should just write a query for each Brand and stack them on top of each other. The other example is like what is shown here made with dataviewjs: [https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/assets/books-by-genre.png](https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/assets/books-by-genre.png)

[![r/ObsidianMD - Using Group By in Dataview](https://preview.redd.it/using-group-by-in-dataview-v0-u1hhy9wz8l5a1.png?width=1282&format=png&auto=webp&s=efac970b12444a142eb445da1dee82d155a90db7)](https://preview.redd.it/using-group-by-in-dataview-v0-u1hhy9wz8l5a1.png?width=1282&format=png&auto=webp&s=efac970b12444a142eb445da1dee82d155a90db7 "Image from r/ObsidianMD - Using Group By in Dataview")

Edit 2:

Well, I tried modifying the linked dataviewjs query above and I got it to work! I have done SQL and other programming things before but never JavaScript so I have no idea what I'm doing. Here is the code and result if anyone is interested. Next I'd like to know how to set the column widths. The Name column is excessively wide.

```dataviewjs
for (let group of dv.pages('"Tea Ratings"').where(p => p.Brand != null).groupBy(p => p.Brand)) {
	dv.header(1, group.key);
	dv.table(["Name", "Type", "Rating"],
		group.rows
			.sort(k => k['Plain Rating'], 'desc')
			.map(k => [k.file.link, k.Type, k['Plain Rating']]))
}
```

[![r/ObsidianMD - Using Group By in Dataview](https://preview.redd.it/using-group-by-in-dataview-v0-e591y31hel5a1.png?width=1107&format=png&auto=webp&s=499b1a5e615179b985e73f1ab043c1ba00959920)](https://preview.redd.it/using-group-by-in-dataview-v0-e591y31hel5a1.png?width=1107&format=png&auto=webp&s=499b1a5e615179b985e73f1ab043c1ba00959920 "Image from r/ObsidianMD - Using Group By in Dataview")
