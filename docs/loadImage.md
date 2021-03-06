# loadImage
:alien: 加载图片函数, 支持Promise方式调用, then对应onSuccess, catch对应onError

## 函数参数 
| 参数名 | 说明 | 默认值 | 数据类型 |
| --- | --- | --- | --- |
| url | 图片地址 | - |string|
| options | 配置 | - | object |

## options 
| 参数名 | 说明 | 默认值 | 数据类型 |
| --- | --- | --- | --- |
| isCrossOrigin | url是否跨域 | false |boolean|
| beforeLoad | 图片加载前触发的回调, data中返回图片尺寸信息等) | (data) => { } | function |
| onSuccess | 图片加载成功触发的回调 | (data) => { } | function |
| onError | 发生错误触发的回调 | (data) => { } | function |
| onAbort | 放弃加载触发的回调| (data) => { } | function |

## 实例 
``` javascript
loadImage('https://avatars1.githubusercontent.com/u/8264787?s=460&v=4').then(({
    img,
    width,
    height,
    costTime,
    nativeEvent})=>{
    console.log({
        img,
        width,
        height,
        costTime,
        nativeEvent
    });
}).catch(({
    img,
    width,
    height,
    costTime,
    nativeEvent})=>{
    console.log({
        img,
        width,
        height,
        costTime,
        nativeEvent
    });
});
```

## 源码
[查看](https://github.com/383514580/useful-utils/blob/master/src/loadImage.ts)
