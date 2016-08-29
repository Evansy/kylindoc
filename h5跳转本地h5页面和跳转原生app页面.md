##### 点击某个链接跳转另外一个页面的方法（包括app原生的还有h5的）
- 跳转H5：
  
         window.JsBridge.JumpH5Page(window.Legwork+'#/LegWorkAssetsManage',null,"资金管理","");
       window.Legwork全局变量在H5API文件夹下设置，本地开发是localhost，url不需要前缀，正式环境需要
       带上页面地址legwork.html,#/LegWorkAssetsManage 是路由，null可以填写相应的参数，没有参数写null,
       资金管理是跳转的页面名称，app需要用，
- 跳转app：
      window.JsBridge.DisUserCententSet();每一个调整对应一个方法


