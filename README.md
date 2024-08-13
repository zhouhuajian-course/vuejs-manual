# vuejs manual

1. Vue 大版本以动漫名作为版本名 vue 1.0 vue 2.0 vue 3.0
2. Vue 采用“组件化”模式
3. 使用“声明式”编码，而非jQuery的“命令式”编码
4. 容器里面的代码，被称为 “Vue模板”
5. 新版本根组件 data 只能是“函数式”，旧版本的 data，可以“对象式”，也可以“函数式”。警告信息：vue-3.4.37.js:1641 [Vue warn]: The data option must be a function. Plain object usage is no longer supported.  at \<App\>
6. 指定容器 可以 el，或 mount，可以提供 容器的CSS选择器或者元素对象
7. {{}} 这是 Vue 的插值语法，里面放的是 JS表达式
8. Vue.js devtools 浏览器扩展，可以方便调试 Vue 应用 https://devtools.vuejs.org/  Browser devtools extension for debugging Vue.js applications
9. Vue 的很多概念都非常抽象，例如挂载，其实就是把组件渲染出来的视图，放到某个容器里面；
10. 渐进式框架的理解，① 可以先页面一部分用 Vue，然后逐渐整个页面都用 Vue；②可以先页面使用 Vue 核心库，然后再一步一步使用各种插件，开发更复杂的应用
