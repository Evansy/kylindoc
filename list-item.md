# list-item 支付方式列表项
用于显示支付方式列表中
#### 标签

```html
<ItemList/>
```

#### 示例

```html
{payments&&payments.length>0?
 payments.map((item,i)=>{
  return (
   <ItemList
    item={item}
    handleRadioChange={this.handleRadioChange.bind(this,item)}
    handleItemClick={this.handleItemClick.bind(this,item)}
    key={i}
    checkedValue={this.state.currentPaymentCheck}
   />
  )
 }):""}
``` 

##### 参数

* `item` `类型：Object` - 商品列表项数据
* `checkedValue` `类型：Function` - 校验支付状态

#### 其他

* `handleRadioChange` radio更换默认样式事件
* `handleItemClick` 选中事件
* `key` map时候的key
* `payments` 支付方式数据

