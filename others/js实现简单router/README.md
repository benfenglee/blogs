# 简单的 JavaScript 路由器

这是一个简单的 JavaScript 路由器的实现，它允许你管理前端页面的路由和导航。

## 如何使用

1. 在 HTML 文件中引入 `router.js` 脚本。

```html
<script src="path-to-router.js"></script>

```

### 初始化路由和设置钩子。
添加路由
使用 addRoute 方法来定义路由和对应的回调函数。
```
Router.addRoute("/", () => {
  // 这是主页的回调函数
  // 在这里更新用户界面或执行其他操作
});

Router.addRoute("/about", () => {
  // 这是关于页面的回调函数
});
```

### 设置 beforeEach 钩子
使用 beforeEach 方法来添加导航前的钩子函数，用于执行一些前置操作。
```
Router.beforeEach((to, from, next) => {
  // 在每次路由导航前执行的操作
  // 使用 'next()' 来继续导航或者阻止它
});
```
### 导航
使用 navigate 方法来执行路由导航。


希望这个 README 文件能够帮助你更好地理解这个简单的 JavaScript 路由器的实现方式。
