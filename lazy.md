# lazyload 懒加载
当页面存在很多图片的时候，使用lazyload第一次进入可以只加载首屏的图片，页面往上拉的时候才加载需要显示的图片，避免图片一次加载太多造成卡顿。

kylin项目中用到两个LazyLoad组件，一个是从npm安装的react-lazyload,一个是在utils文件夹下的imglazyload

#### 标签

```html
<Lazyload></Lazyload>
<img class="swiper-lazy" />
```
#### 示例
```html
 <!--Lazyload-->
 <Lazyload throttle={200} overflow>
	<img src={item.AdFile?window.H5Api.urlThumbPath(item.AdFile.split(',')[0],360,180):""} alt="" />
 </Lazyload>

 <!--imgLazyload-->
 <img
	data-src={item.AdFile ? window.H5Api.urlThumbPath(item.AdFile.split(',')[0], 720, 320) : ""}
	className="swiper-lazy"
	style={{height: '100%'}}
	data-item={JSON.stringify(item)}
 />
```
##### Lazyload参数
* `options` - 轮播属性设置
* `height` - 设置轮播高度
* `onAdClick` - 轮播点击事件

　　[详见 react-LazyLoad Git](https://github.com/jasonslyvia/react-lazyload)

#### 其他
* `adObj['U01002_home001']` 广告数据以及广告id
* `window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""}` 服务器压缩图片至指定

#### `options` 例子
```js
df
```

