# Time down 
#### 标签 
```html 
<TimeDown></TimeDown> 
``` 
#### 示例 
```html 
<TimeDown Time={current}
 GameTime={order.JoinTime}
 cancelOrder={this.cancelOrder}
 OrderID={order.OrderID}
/> 
``` 
##### 参数 
* `Time` `类型：String` - 时间 
* `GameTime` `类型：Number` - 加入时间
* `cancelOrder` `类型：Function` - 关闭订单事件
* `OrderID` `类型：String` - 订单ID

#### `cancelOrder` 例子 
```js 
cancelOrder:function(){
    window.requestHybrid({
      tagname:"cancelOrder",
      param:this.props.LegWorkOrder.JoinTime, 
    });
},
```
#### `current` 例子 
```js 
var current=store2.get('Current'+order.OrderID);
```