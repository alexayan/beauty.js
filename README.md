# beauty.js

![Build Status](https://img.shields.io/travis/alexayan/beauty.js.svg)
![Coverage](https://img.shields.io/coveralls/alexayan/beauty.js.svg)
![Downloads](https://img.shields.io/npm/dm/beauty.js.svg)
![Downloads](https://img.shields.io/npm/dt/beauty.js.svg)
![npm version](https://img.shields.io/npm/v/beauty.js.svg)
![dependencies](https://img.shields.io/david/alexayan/beauty.js.svg)
![dev dependencies](https://img.shields.io/david/dev/alexayan/beauty.js.svg)
![License](https://img.shields.io/npm/l/beauty.js.svg)

make web beautiful

## Use it with NPM

Install it via npm:

```shell
npm install beauty.js
```

And include in your project:

```javascript
import beautyJS from 'beauty.js';

// default usage
beautyJS.beauty('text')
beautyJS.beauty(Element)

// custom usage of TextFormat
const format = new beautyJS.TextFormat({
  nouns: ['Apple', 'IOS']
});
format.updateNouns(['Apple', 'IOS', 'Android'])
format.formatText('text')
// all tags must closed like: <tag /> or <tag></tag>
format.formatHTMLText('<p><image src="url"/>text</p>')
// all tags must closed like: <tag></tag> and no nest
format.formatHTML('<span>text</span><span>another text</span>')

// custom usage of ParagraphFormat
const p = new beautyJS.ParagraphFormat(Element, {
    disableHanging: false, // 取消标点悬挂
    format: new beautyJS.TestFormat(), // 文本格式化
    disableFormat: false, // 禁用文本格式化
    clamp: 3 // 最多显示行数
})
// clamp
p.clamp(10) //设置展开行数

// remember destroy to avoid memory leaks
p.clear()
```

## Use it with Script Link

```javascript
<head>
  // Files are located on /node_modules/beauty.js/build/
  <script src="beauty.min.js"></script>
</head>
<script>
  beautyJS.beauty('text')
  ...
</script>
```

## License

MIT

