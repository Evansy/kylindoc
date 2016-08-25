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

* `lvSpec` `类型：Object / String` - 等级
* `lv`  `类型：Object`- 用户经验值
* `sex` `类型：String` - 用户性别

#### 其他

* `this.props.LvSpec` 用来判断父元素是否传入LvSpec数据或者组件内是否初始化LvSpec数据