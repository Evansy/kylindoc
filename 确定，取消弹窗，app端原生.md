##### 每一个方法对应一个接口

* 现在介绍其中一个列子

```html
DeleteLegworkOrder: function(order) { //删除订单

 var order = this.props.LegWorkOrderDetails;
 if (process.env.NODE_ENV !== 'production') {
 // if(confirm("你确定要删除订单吗？")){this.props.actions.DeleteLegworkOrder(order);}
 }

 var self = this;
 var btn_CallBack = [
{
 buttonName: '取消',
 buttonCallBack: function() {
 return;
 }
}, 
{
 buttonName: '确定',
 buttonCallBack: function() {
     window.JsBridge.DisOrderDelOrder(order.OrderID, function(data) {
 // console.log('data',data);
 if (data == "true") {
 var btn_CallBack1 = [{
 buttonName: '确定',
 buttonCallBack: function() {
 // self.props.actions.DeleteLegworkOrder(order);
 window.JsBridge.DisH5PageBack();
 }
 }];

 window.JsBridge.CallAppAlert('', '操作成功', btn_CallBack1);
 } else {
 var btn_CallBack2 = [{
 buttonName: '确定',
 buttonCallBack: function() {
 return
 }
 }];
 window.JsBridge.CallAppAlert('', '操作失败', btn_CallBack2);
 }
 });
 }
 }];
 window.JsBridge.CallAppAlert('', '确定删除吗', btn_CallBack);
},


```


    btn\_CallBack 按钮的数组，包括确定和取消，也可以只有一个确定按钮
    buttonName：按钮名字
    buttonCallBack：点击按钮执行的回调方法
    window.JsBridge.CallAppAlert 弹窗方法及提示


这个列子是删除订单的操作
    取消确定对应的提示是确定确定删除吗？点击取消不做任何操作，点击确定，调用相应的删除订单的方法 window.JsBridge.DisOrderDelOrder,如果接口操作成功，提示操作成功，操作失败提示操作失败，成功之后执行相应的方法刷新页面状态，但有一点要注意，有些对订单的状态我们H5的方法只是改变了他的状态刷新了相应的状态，但是有些数据并没有刷新，比如确认送达之后，我们改变了订单的状态，订单状态的显示和之后对应该有的操作改变了，但是页面数据并没有完全刷新，我们的确认送达时间还是为null,所有有的时候有必要操作成功时重新请求一次数据，刷新页面



