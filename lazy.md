# lazyload 懒加载
当页面存在很多图片的时候，使用lazyload第一次进入可以只加载首屏的图片，页面往上拉的时候才加载需要显示的图片，避免图片一次加载太多造成卡顿。

#### 标签

```html
<ImgSwiper></ImgSwiper>
```
#### 示例
```html
<ImgSwiper></ImgSwiper>

```
##### 参数
* `options` - 轮播属性设置
* `height` - 设置轮播高度
* `onAdClick` - 轮播点击事件

#### 其他
* `adObj['U01002_home001']` 广告数据以及广告id
* `window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""}` 服务器压缩图片至指定

#### `options` 例子
```js
df
```

