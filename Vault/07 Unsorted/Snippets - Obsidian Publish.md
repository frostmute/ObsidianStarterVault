irst, there are non-user-defined attributes that every file must have: [file attribute query](https://blacksmithgu.github.io/obsidian-dataview/data-annotation/#implicit-fields) .

### Sorting of file attributes such as file name

```js
.sort(p => p.file.name)
```

### Reverse

```js
.sort(p => p.file.name, 'desc')  # 默认升序是'asc'
```

### Chinese sorting

```js
.sort(p => p.file.name, 'asc', (a, b) => a.localeCompare(b, 'zh-CN'))
```

### filter

```js
.filter(p => p.file.name == "xxxx")
```

Only files that are true according to the expression in the parentheses will be selected.  
Filters can be processed all at once using Boolean operators, or multiple filters can be connected in succession.

```js
.filter(p => p.file.name != "xxxx")
.filter(p => p.file.tags.includes('#yyyy'))
```

### Display time in format

Dataview uses [Luxon](https://moment.github.io/luxon/#/tour) for internal time recording .

```js
var time = dv.current().file.ctime;
dv.paragraph(time.toFormat("yy-MM-dd H:mm:ss a"));
```

Query [time format code](https://github.com/moment/luxon/blob/master/docs/formatting.md#table-of-tokens)

### Create the current time point

```js
luxon.DateTime.now()
```

### Create a specified time point

```js
luxon.DateTime.fromISO("2017-09-24")
```

### Time sequence

```js
var now = luxon.DateTime.now();
var past = luxon.DateTime.fromISO("2017-09-24");
dv.paragraph(past < now);
```

### Determine the same day/simultaneity

```js
time1.equals(time2)
```

Note that Luxon time objects cannot be compared with `a == b`or because they are not basic types `a === b`; do not use them when comparing dates `ctime/mtime`, use `cday/mday`.

### Time difference

```js
var end = DateTime.fromISO('2017-03-13'); 
var start = DateTime.fromISO('2017-02-13'); 
var i = Interval.fromDateTimes(start, end);

i.length('days'); //=> 28
i.length('months') //=> 1
```

See [Luxon Math](https://moment.github.io/luxon/#/math) to learn more about time comparison problems.