## 这是什么

这是一个快速配置 valine 表情的仓库，表情仓库为 https://github.com/blogimg/emotion

## 如何使用

首选需要引入 js

```html
<script src="https://cdn.jsdelivr.net/gh/monologuechi/valine-emoji@0.0.3/index.min.js"></script>
```

然后在 valine 配置表情

```js
//省略其他配置

  emojiCDN = " ";    //注意这里是空格
  emojiMaps = Emotion.Emoji(["热词系列","冷兔","那兔"]);  //选择需要的表情包，表情包名称可以参考 index.js 和 http://www.antmoe.ml
```

如果需要同时使用其他的表情仓库呢？

很简单，只需要合并表情配置就可以了

```js
new valine(
  //省略其他配置
  emojiCDN = " ";    //注意这里是空格
  emojiMaps = {
    "表情1" : "地址",
    "表情2" : "地址",
    "表情3" : "地址",
    ...Emotion.Emoji(["热词系列","冷兔","那兔"])
  }
)
```