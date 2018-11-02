


[md书写规范](https://www.jianshu.com/p/436caf91dd06)

## 小程序

***1. 抛出事件中属性***
```
> this.triggerEvent('action',oAccount)

```

***2. 跳转页面清除定时器***
````
onUnload: function () {
clearInterval(this.interval)
},
````