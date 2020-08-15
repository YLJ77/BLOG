解析器内部包含开始标签钩子函数、结束标签钩子函数、文本钩子函数以及注释钩子函数。

伪代码：
```javascript
parseHTML(template, {
    start (tag, attrs, unary) {
        // 每当解析到标签的开始位置时，触发该函数
    },
    end () {
        // 每当解析到标签的结束位置时，触发该函数
    },
    chars (text) {
        // 每当解析到文本时，触发该函数
    },
    comment (text) {
        // 每当解析到注释时，触发该函数
    }
})
```

比如：
```html
<div><p>我是Berwin</p></div>
```

上面模板解析时依次触发的钩子函数是：
