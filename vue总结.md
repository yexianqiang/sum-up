***1. input返回页面cacheData缓存***
```


```
***2. beforeRouteEnter中vm执行***
````
https://blog.csdn.net/u012414590/article/details/79144722
beforeRouteEnter (to, from, next) {
    console.log(this);  //undefined，不能用this来获取vue实例
    console.log('组件路由钩子：beforeRouteEnter');
    next(vm => {
        console.log(vm);  //vm为vue的实例
        console.log('组件路由钩子beforeRouteEnter的next');
    });
}
next(vm=>{console.log(‘next’) }) 
这个里面的代码很晚执行，执行时机在组件mounted周期之后
但是beforeRouteEnter 是先于生命周期钩子函数执行的
````
***3. vue虚拟dom***
````
    1、vue2 引入了虚拟dom，即如果使用.vue的模板方式书写，会首先编译为render函数，生成vnode，每次数据变更后，会在nexttick中进行新老vnode对比进行patch操作
    https://www.cnblogs.com/teamblog/p/9565233.html
    
    2、Vue2.0 render:h => h(App)
    https://blog.csdn.net/qq78827534/article/details/80792514

    在Vue的mount过程中，template会被编译成AST语法树
    window.vApp = new Vue({
      el: '#app',
      router,
      store,
      mounted() {},
      render(h) {
        return h(app)
      },
    });
    其实以上代码总结起来就4步：

    获取el元素。判断el是否为body或者html。为$options编译render函数。
    执行之前的mount函数。关键在于第三步，编译 render 函数上。先获取 template，即获取HTML内容，然后执行 compileToFunctions 来编译，最后将 render 和 staticRenderFns 传给 vm.$options 对象。

````
***4. 登陆公共方法引入***
````
    1、引入js文件 http://10.13.5.152:8088/js/common.js（此处暂用我本机ip）
    2、做跨域处理
    3、var Request = new $request(); 
    4、调用方法（判断是否登陆为例）
        Request.isLogin().then(function(res){
                console.log(res)
        })

````
***5. 实例Vue中data数据渲染***
````
    https://www.jishux.com/p/0bebeb52c6eb0e03
    
    当你把一个普通的 JavaScript 对象传给 Vue 实例的 data 选项，Vue 将遍历此对象所有的属性，并使用 Object.defineProperty 把这些属性全部转为 getter/setter。
    用户是看不到 getter/setter，但是在内部它们让 Vue 追踪依赖，在属性被访问和修改时通知变化。
    每个组件里都有一个watcher 实例对象，它会在组件渲染时把属性依赖记录下来，当setter被调用时会通知 watcher 重新计算重新渲染页面。
````
***6. nuxt打包vender***
````
    https://www.jianshu.com/p/6300e482315e
    那么a.vue和b.vue打包后的文件大小将比不加上build.vendor小，如果很多文件都需要引入axios的话，那么对于文件大小的优化效果是比较明显的
````
我是hello
