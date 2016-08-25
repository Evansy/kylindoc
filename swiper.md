# swiper 轮播图

#### 标签
```html
<ImgSwiper></ImgSwiper>
```
#### 示例
```html
  <ImgSwiper options={swiperInit} height={(430/72)+"rem"} onAdClick={this.handleAdClick}>
    {
              adObj['U01002_home001'].map(function(item,index){
                return (
                  <div className="swiper-slide ad-swiper-slide"
                      key={index}
                      data-item={JSON.stringify(item)}
                  >
                    <a href="javascript:;"
                        key={"b-"+index}
                        style={{width:'100%',height:'100%'}}
                        data-item={JSON.stringify(item)}
                    >
                      <img 
                      data-src={item.AdFile?window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""} 
                      className="swiper-lazy" 
                      style={{width:'100%',height:'100%'}}
                      data-item={JSON.stringify(item)}
                      alt={item.Title}
                      />
                      <div className="swiper-lazy-preloader"></div>
                  </a>
                  </div>
                );
              }.bind(this))
            }
   </ImgSwiper>
```

##### 参数

* `options` `类型：Object` - 轮播属性设置
* `height` `类型：number` - 设置轮播高度
* `onAdClick` `类型：function` - 轮播点击事件

#### 其他
* `adObj['U01002_home001']` 广告数据以及广告id
* `window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""}` 服务器压缩图片至指定 

#### `options` 例子

```js
 var swiperInit = {
  // 循环播放
  loop: true,
  lazyLoading:true,
  // 自动播放间隔
  autoplay: 2500,
  // 如果需要分页器
  pagination: '.swiper-pagination',
  autoplayDisableOnInteraction:false,
  observer:true,
  onInit: function(swiper){
    // fix swiper loop swiper with same reactid bug
    [].forEach.call(swiper.slides,function (item,i) {
      if (item.classList.contains("swiper-slide-duplicate")) {
        item.setAttribute('data-reactid',item.getAttribute('data-reactid')+"."+i)
        let link = item.querySelector('a');
        if (link) {
          link.setAttribute('data-reactid',item.getAttribute('data-reactid')+"."+i);
        }
        let img = item.querySelector('img');
        if (img) {
          img.setAttribute('data-reactid',item.getAttribute('data-reactid')+"."+i);
        }

      }
    });
  }
 };
```

#### `options` 例子

这是一个给客户端发送的点击事件 后面详解

```js
   handleAdClick:function (ad) {
    window.requestHybrid({
      tagname:'adClick',
      param:ad
    })
  },
```

