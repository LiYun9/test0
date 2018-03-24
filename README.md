# Github 留言系统

[在线预览](http://liyun9.github.io/test0/)

让评论质量更高，让网站与 Github 关联
适合程序员的评论系统，基于 Github issues 留言

[![preview](http://p5k7mvi7l.bkt.clouddn.com/%E5%9B%BE%E7%89%871.png)](http://liyun9.github.io/test0/)

## 使用
### data-api
```html
<style>.gc-comments {font:12px/1.5 Lantinghei SC,Microsoft Yahei,Hiragino Sans GB,Microsoft Sans Serif,WenQuanYi Micro Hei,sans-serif}</style>
<script src="https://unpkg.com/github-comments/gc.js"></script>
<div class="gc-comments" data-repos="liyun9/test0" data-issues="1" >
    <div class="gc-comments-title">
        评论
    </div>
    <div class="gc-comments-info">
        想在此留下评论，请访问 <a target="_blank" href="issues_link">issues_link</a> 提交评论
    </div>
</div>
```

`issues_link` 会自动替换成 `https://github.com/liyun9/github-comments/issues/1`

### gc.load()


```js
gc.load(repos, issues, element, noCommentsTip)
// 或者
githubComments.load(repos, issues, element, noCommentsTip)
// 当 全局变量 gc 被占用时使用 githubComments
```

| 参数 | 说明 | 示例 |
| --- | --- | ---- |
| repos | 项目地址 |[liyun9/test0](http://github.com/liyun9/test0) |
| issues| issues id | [1](https://github.com/liyun9/test0/issues/1)
| element | 渲染容器 | `"#demo"` `document.getElementById('demo')` `$('#demo')` |

```
<div id="demo"></div>
<script src="https://unpkg.com/github-comments@0.4.0/gc.js"></script>
<script>
gc.load('liyun9/test0', 1, '#demo')
</script>
```

fork自：        https://github.com/nimojs/github-comments  
灵感来自：      http://fex.baidu.com/webuploader/demo.html  
全站使用示例：  http://fmsjs.org/


### 参与开发

```shell
git clone https://github.com/liyun9/test0.git
cd github-comments
npm i --registry=https://registry.npm.taobao.org
# server
npm run s
npm run dev
```
