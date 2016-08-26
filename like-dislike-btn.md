# like-dislike-btn

#### 标签

```html

<LikeDislikeBtn></LikeDislikeBtn>

```

#### 示例

```html
<LikeDislikeBtn topic={post} tagname="LikePost"
	className="action xc-btn xc-btn-default" clickCallback={this.props.actions.likeTopic}>
	<i className="xc-icons xc-icon-like-grey"></i>{firstComment.Support?firstComment.Support:0}
</LikeDislikeBtn>
```

##### 参数

* `topic` `类型：Object` - 轮播属性设置

* `tagname` `类型：String` - 值可选`LikePost / DislikePost` 显示不同类型的样式

* `clickCallback` `类型：Function` - 点击回调事件 点击之后触发


