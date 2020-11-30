# LWC Buffer

[lwc-buffer](https://github.com/exiahuang/lwc-buffer) The buffer module from [node.js](https://nodejs.org/), for the lwc developer.
Base on [buffer](https://github.com/feross/buffer).

## features

- Manipulate binary data like a boss, in all browsers!
- Super fast. Backed by Typed Arrays (`Uint8Array`/`ArrayBuffer`, not `Object`)
- Extremely small bundle size (**6.75KB minified + gzipped**, 51.9KB with comments)
- Excellent browser support (Chrome, Firefox, Edge, Safari 11+, iOS 11+, Android, etc.)
- Preserves Node API exactly, with one minor difference (see below)
- Square-bracket `buf[4]` notation works!
- Does not modify any browser prototypes or put anything on `window`
- Comprehensive test suite (including all buffer tests from node.js core)

## deploy lwc-buffer

<a href="https://githubsfdeploy.herokuapp.com?owner=exiahuang&repo=lwc-buffer">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png">
</a>

or 

```sh
git clone https://github.com/exiahuang/lwc-buffer.git
cd lwc-buffer
sfdx force:source:deploy --loglevel fatal -p force-app/main/default/lwc/buffer/buffer.js-meta.xml --targetusername=$username_or_alias_for_your_sfdc_org
```

## usage

```js
import buffer from 'c/buffer';
const Buffer = buffer.Buffer;

const buf = Buffer.from([1, 2, 3]);
console.log(buf);
```

## document

- https://nodejs.org/api/buffer.html