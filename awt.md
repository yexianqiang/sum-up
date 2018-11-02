


[md书写规范](https://www.jianshu.com/p/191d1e21f7ed)

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

***3. charCodeAt()***
````
返回字符的Unicode 编码（ASCII）, 汉字的charCodeAt在 大于255
````