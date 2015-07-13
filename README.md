# ogp-meta

[![version](https://img.shields.io/npm/v/ogp-meta.svg) ![download](https://img.shields.io/npm/dm/ogp-meta.svg)](https://www.npmjs.com/package/ogp-meta)

Generate open graph meta tags.

## Usage

```javascript
var OpenGraph = require('../');

var ogp = new OpenGraph();

ogp.title('title');
ogp.type('website');
ogp.site_name('site_name');
ogp.description('description');
ogp.url('http://ogp-meta.npm');
// ogp.image('http://image url');
ogp.image({
    url: 'http://image url',
    width: 400,
    height: 400
});
ogp.app({
    url: 'example://app',
    app_store_id: 'app_store_id',
    app_name: 'app_name'
}, 'ios');
ogp.app({
    url: 'example://app',
    package: 'com.ogp-meta.app',
    app_name: 'app_name'
}, 'android');

console.log(ogp.toHTML());
```


## LICENSE

ogp-meta is licensed under the MIT license.