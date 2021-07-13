# 弹窗内的按钮

## 背景
1. 新建编辑等弹窗内部需要保存等按钮；
2. 弹窗内部展示的不是分页列表组件

满足以上两个条件即可参照下方的数据格式提供 api。

## 返回按钮信息

  ```json
  {
    "code": 200,
    "msg": "接口返回成功",
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
      }
    }
  }
  ```