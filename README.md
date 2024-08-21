# vuejs manual

1. Vue 大版本发布时的代号是 动漫名 vue 1.0 vue 2.0 vue 3.0 https://github.com/vuejs/core/releases/tag/v3.0.0
2. Vue 采用“组件化”模式
3. 使用“声明式”编码，而非jQuery的“命令式”编码
4. 容器里面的代码，被称为 “Vue模板”
5. 新版本根组件 data 只能是“函数式”，旧版本的 data，可以“对象式”，也可以“函数式”。警告信息：vue-3.4.37.js:1641 [Vue warn]: The data option must be a function. Plain object usage is no longer supported.  at \<App\>
6. 指定容器 可以 el，或 mount，可以提供 容器的CSS选择器或者元素对象
7. {{}} 这是 Vue 的插值语法，里面放的是 JS表达式
8. Vue.js devtools 浏览器扩展，可以方便调试 Vue 应用 https://devtools.vuejs.org/  Browser devtools extension for debugging Vue.js applications
9. Vue 的很多概念都非常抽象，例如挂载，其实就是把组件渲染出来的视图，放到某个容器里面；
10. 渐进式框架的理解，① 可以先页面一部分用 Vue，然后逐渐整个页面都用 Vue；②可以先页面使用 Vue 核心库，然后再一步一步使用各种插件，开发更复杂的应用
11. (Vue 2) 虽然没有完全遵循 MVVM 模型，但是 Vue 的设计也受到了它的启发。因此在文档中经常会使用 vm (ViewModel 的缩写) 这个变量名表示 Vue 实例。这说明 MVVM不是 Vue创造的，它也是借鉴别人的这个模型，https://v2.cn.vuejs.org/v2/guide/instance.html#%E5%88%9B%E5%BB%BA%E4%B8%80%E4%B8%AA-Vue-%E5%AE%9E%E4%BE%8B
12. MVVM（Model–view–viewmodel）是一种软件架构模式。MVVM表示的是三个东西，M V VM。Model表示业务逻辑和数据。https://zh.wikipedia.org/wiki/MVVM
13. Vue 2 文档 https://v2.cn.vuejs.org/
14. createApp({}) 传的对象，就是根组件或者叫根组件选项，推荐叫根组件，更形象
15. 模板语法 有 插值语法 和 命令语法 两种语法，插值语法是元素内容里面使用，命令语法一般在元素属性上使用。例如`<a v-bind:href="school_url">{{school_name}}</a>` https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/HTML_basics
16. v-model一般需要用在表单类元素上，否者会有警告，例如`<input v-model:value="school_name" />`，默认的属性是value属性
17. v-bind v-model等，双引号里面的，在Vue底层会当做 JS表达式 来使用，并不是普通的字符串
18. Vue2组件使用data,methods，Vue3组件也可以用data,methods，但更推荐 组合式 API 而不是 选项式 API， `<script setup></script>` 是语法糖
19. v-bind 是单向数据绑定，v-model 是双向数据绑定。举例`<input v-href:value="school_name" />` 修改school_name，value值会跟着修改，但修改input的value属性，school_name不会跟着更改，单向数据绑定；`<input v-model:value="school_name" />` 修改school_name，value值会跟着修改，修改input的value属性，school_name也会跟着更改，双向数据绑定
20. 尽量不要写缩写形式的指令，可读性比较差，例如 :href 改成 v-bind:href，v-model 改成 v-model:value，貌似Vue3只能写v-model
21. (Vue 2) 组件的数据，底层通过各种方式，最终会变成 组件实例 的属性，这些属性都做了数据代理，插值语法、指令语法中的 JS表达式 其实可以访问组件实例的所有属性 例如{{$emit}} {{_c}}
22. Vue2使用webpack前端构建工具 https://webpack.js.org/，Vue3使用Vite前端构建工具 https://vitejs.dev/
23. Vite（法语意为 "快速的"，发音 /vit/，发音同 "veet"）是一种新型前端构建工具，能够显著提升前端开发体验。
24. Vue3，通过组合式 API，我们可以使用导入的 API 函数来描述组件逻辑。在单文件组件中，组合式 API 通常会与 `<script setup>` 搭配使用。这个 setup attribute 是一个标识，告诉 Vue 需要在编译时进行一些处理，让我们可以更简洁地使用组合式 API。比如，`<script setup>` 中的导入和顶层变量/函数都能够在模板中直接使用 https://cn.vuejs.org/guide/introduction#composition-api
25. Vue3 在组合式 API 中，推荐使用 ref() 函数来声明响应式状态(数据)：还有另一种声明响应式状态的方式，即使用 reactive() API。与将内部值包装在特殊对象中的 ref 不同，reactive() 将使对象本身具有响应性： https://cn.vuejs.org/guide/essentials/reactivity-fundamentals.html
26. 声明响应式数据，基本数据类型用 ref()，对象或数组数据类型用 ref() 或 reactive()，要留意这两种方式的不同点，例如reactive()，不需要像ref()一样总是加.value，reactive()可以用Object.assign()覆盖数据
27. (Vite+Vue) npm run dev ，运行的是 vite 命令，这个命令在，`node_modules/.bin/vite.cmd`，如果linux，则是 `node_modules/.bin/vite`
28. `.vue` 文件是，Vue特有的文件，用来定义一个组件，组件里面可以写三个标签 `<script setup>` `<template></template>` `<style scoped></style>`
29. (Vite+Vue) npm run dev，是启动 Vite 开发服务器
