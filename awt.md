


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

***4. 绘制小程序分享****
`````
https://www.cnblogs.com/gavinjay/p/8582137.html
`````
***5. 跳转页面***
`````
https://www.cnblogs.com/liuqingxia/p/7844937.html
`````
***6. animation***
````
transformOrigin
transtion和animation区别(https://blog.csdn.net/liaozhongping/article/details/79511820)
````

***7. charles***
```
简介https://blog.csdn.net/JerryWu145/article/details/52013128?utm_source=blogxgwz4
```

***8. promise***
```
异步调用 https://blog.csdn.net/u011500781/article/details/73883903?locationNum=7&fps=1
var $ajax = (url, data, method) => {
//     return new Promise((resolve, reject) => {
//         defaultRequest = {
//             data: data || {},
//             url,
//             type: method || 'POST',
//             // dataType: 'json',
            
//             success:function(res){
//                 resolve(res)
//             },
//             fail: (res) => {
//                 reject(res)
//             }
//         }
//         Object.assign(defaultRequest, data);
        
//         $.ajax(defaultRequest)
//     })
// };

// var b1 = $ajax('/SPREADAPI/porsche/ad/v2/getAd',{adSlotId: 'APP-A10051'},'GET')
// var a1 =  $ajax('/SPREADAPI/porsche/koiapi/v1/getkiounixtime')

// a1.then(function(res){
//     console.log(res)
//     return b1
// })
// .then(function(res){
//     console.log(res)
// })
// Promise.all([b1, a1]).then((result)=>{
//     console.log(result)
//     console.log(1111)
// })
```
***9.file和http协议***
```
![avatar](/images/fileAnd_ht.png)
```
