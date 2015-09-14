# bible-search [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]
> A client Bible Search Api wrapper for NodeJs https://pt-br.bibles.org/pages/api


## Install

```sh
$ npm install --save bible-search
```


## Usage

Before you run tests, you must create a file named: config.auth.json, example:

```
{
  "bibleApiKey": ""
}
```


```js
var BibleSearch = require('bible-search');
var bibleSearch = new BibleSearch('<<API KEY HERE>>');

//
//ES6 Style
//
import BibleSearch from 'blble-search';
var bibleSearch = new BibleSearch('<<API KEY HERE>>');

//
// Get books
//
bibleApi.book.getBooks().then((data) => {
  //JSON Structure see: https://pt-br.bibles.org/pages/api/documentation/books 
}).catch(function (err) {
  console.log('Ops! Sorry :|');
});

//
// Get passage
//
bibleApi.passage.getPassage({
  book: 'rev',
  chapter: 21,
  start: 4
}).then(function (data) {
  //JSON Structure see: https://pt-br.bibles.org/pages/api/documentation/passages
}).catch(function (err) {
  console.log('Ops! Sorry :|');
});

//
// Get book chapters
//
bibleApi.book.getChapters({
  book: 'rev'
}).then(function (data) {
  //JSON Structure see: https://pt-br.bibles.org/pages/api/documentation/chapters
}).catch(function (err) {
  console.log('Ops! Sorry :|');
});

//
// Get book verses
//
bibleApi.book.getVerses({
  book: 'rev',
  chapter: 21
}).then(function (data) {
  //JSON Structure see: https://pt-br.bibles.org/pages/api/documentation/verses
}).catch(function (err) {
  console.log('Ops! Sorry :|');
});

//
// Search in the bible
//
bibleApi.search.find({
  query: 'Pai nosso'
}).then(function (data) {
  //JSON Structure see: https://pt-br.bibles.org/pages/api/documentation/search
}).catch(function (err) {
  console.log('Ops! Sorry :|');
});
```

## License

Apache-2.0 © [William Sena](www.coisadeprogramador.com.br)

[npm-image]: https://badge.fury.io/js/bible-search.svg
[npm-url]: https://npmjs.org/package/bible-search
[travis-image]: https://travis-ci.org/willsenabr/bible-search.svg?branch=master
[travis-url]: https://travis-ci.org/willsenabr/bible-search
[daviddm-image]: https://david-dm.org/willsenabr/bible-search.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/willsenabr/bible-search

## TODO

- Correct English Wrongs! :)
- Improve Documentation (ESDocs)
- Support Browserify
- Refactoring