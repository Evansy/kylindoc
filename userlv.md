# UserLv 用户等级
用来显示用户等级标识
#### 标签
```html
<UserLv></UserLv>
```
#### 示例

```html
 {this.props.LvSpec ? <UserLv lvSpec={this.props.LvSpec} lv={myExp} sex={post.Sex}/> : null}
```

##### 参数

* `lvSpec` - 轮播属性设置
* `height` - 设置轮播高度
* `onAdClick` - 轮播点击事件

#### 其他

* `adObj['U01002_home001']` 广告数据以及广告id
* `window.H5Api.urlThumbPath(item.AdFile.split(',')[0],720,430):""}` 服务器压缩图片至指定

#### `options` 例子
```js
df
```