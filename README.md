# lists
repository contains a large lists that i have generated and its source


# [source #1](https://en.wikipedia.org/wiki/List_of_U.S._state_and_territory_nicknames)
```javascript
var rows = $('.wikitable')[0].rows;
var states = []

for(var i=1;i<=rows.length;i++){

  var tr = $(rows[i]);
	var tdState = $(tr.find('td')[0]);
	var tdNicknames = $(tr.find('td')[1]);
	var stateName = tdState.find('a')[0]?tdState.find('a')[0].text: tdState.find('a').text();
  states.push({name:stateName,'nicknames':tdNicknames.html()});
}
console.log(states)
```
