# imglazyload 懒加载
当页面存在很多图片的时候，使用lazyload第一次进入可以只加载首屏的图片，页面往上拉的时候才加载需要显示的图片，避免图片一次加载太多造成卡顿。

kylin项目中用到两个LazyLoad组件，一个是从npm安装的[react-lazyload](lazy.md),一个是在utils文件夹下的imglazyload

#### 标签
```html
<img class="swiper-lazy" />
```

#### 示例
```html
 <img
   data-src={item.AdFile ? window.H5Api.urlThumbPath(item.AdFile.split(',')[0], 720, 320) : ""}
   className="swiper-lazy"
   style={{height: '100%'}}
   data-item={JSON.stringify(item)}
 />
```