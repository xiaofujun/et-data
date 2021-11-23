# 表单顶部(或底部)的按钮

当页面渲染的是表单，且此时需要保存等操作按钮时。按钮信息可通过获取表单数据的接口一起返回。具体如下：

## 返回按钮信息

  ```json
  {
    "code": 200,
    "msg": "",
    "status": true,
    "data": {
      // 按钮信息放在 button 属性中
      "button": [ 
        {
          "icon": "Icon-OR",
          "id": "save",
          "type": "primary",
          "content": "保存"
        }
      ],
      // formSetting 可存放弹窗内 form 表单的一些信息
      "formSetting": {
        "layout": [],
        "items": {},
        "data": {},
        "groupId": []
      }
    }
  }
  ```