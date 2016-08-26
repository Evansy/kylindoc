# distance 距离组件
#### 标签
```html
<Distance></Distance>
```

#### 示例
```html
<Distance startPoint={{Latitude:post.Latitude,PassLevel:post.PassLevel}}
	      endPoint={this.props.currentPoint} />
```

##### 参数

* `startPoint` `类型：Object` - 开始点的坐标信息
* `endPoint` `类型：Object` - 结束点的坐标信息