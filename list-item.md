# js 描述模板

#### 标签

```html
<ItemList/>
```

#### 示例

```html
<ItemList
   item={item}
   handleRadioChange={this.handleRadioChange.bind(this,item)}
   handleItemClick={this.handleItemClick.bind(this,item)}
   key={i}
   checkedValue={this.state.currentPaymentCheck}
/>
``` 

##### 参数

* `options` `类型：Object` - 轮播属性设置
* `height` `类型：Number` - 设置轮播高度
* `onAdClick` `类型：Function` - 轮播点击事件

#### 其他

* `adObj['U01002_home001']` 广告数据以及广告id
* `window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""}` 服务器压缩图片至指定

#### `options` 例子

```js
df
```

