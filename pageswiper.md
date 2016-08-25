# pageswiper 页面下拉刷新以及上拉加载更多
通常包裹在页面最外层
#### 标签
```html
<!-- 下拉刷新 有动画 引用自组件OverflowPage -->
<PageSwiper> </PageSwiper > 

<!--上拉加载更多 异步加载 无下拉动画 引用自组件swiperScroll -->
<PageSwiper type={myscroll}> </PageSwiper > 
```
#### 示例
```js
 <PageSwiper notRefreshNeedLoadMore={true} loadMore={this.loadMore}>
	······
 </PageSwiper> 
```

#### 参数
* `notRefreshNeedLoadMore`  `类型：Boolean` 不刷新只需要加载更多
* `loadMore`  		     `类型：function` 加载更多回调函数

#### `loadMore` 示例
 `requestDatas`是另外一个用来请求数据的组件
```js
 var self = this;
		var data = this.props.SortContainer;
		if (data && data.Data && 
		    data.Data.allproductlist && 
		    data.Data.allproductlist.length && 
		    data.Data.allproductlist.length > 0 && 
		    data.total <= data.Data.allproductlist.length) {
			this.setState({IsNoData: true})
			return
		}
		requestDatas({
			tagname: 'MoreProducts',
			param: {PageIndex: this.state.PageIndex + 1, CategoryID: this.state.sortTabIndex},
			callback: function (data) {
				if (data) {
					var result = JSON.parse(data);
					self.props.actions.moreWholeHeart(result);
					self.setState({PageIndex: self.state.PageIndex + 1});
					if (callback) {
						callback()
					}
				}
			}
		});
```