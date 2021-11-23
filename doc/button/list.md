# 列表顶部的按钮

## 背景
e10 中人力模块提供了校验当前登录人是否拥有功能操作权限的接口。所以每个功能的首页如果需要按钮，则统一遵循以下方法返回全部按钮的信息。

## 返回按钮信息
1. 后端同事提供获取页面按钮的 api

    例如： ``` /api/bs/intcenter/intunifytodo/client/sendinfo/getButton ```

2. api 返回的数据格式如下：

    ```json
    {
      "code": 200,
      "msg": "",
      "status": true,
      "data": {
        "button": [
          {
            "id": "add",  // 新建注册 id 用 add 
            "content": "新建",
            "icon": "Icon-add-to03",
            "type": "primary"
          },
          {
            "id": "log",  // 日志 id 用 log 
            "content": "操作日志",
            "icon": "Icon-Operation-log02",
            "type": "primary"
          },
          {
            "id": "customColumns", // 显示列定制 id 用 customColumns
            "content": "显示列定制",
            "icon": "Icon-Custom-columns",
            "type": "primary"
          }
        ]
      }
    }
    ```
    **除了【操作日志】和【显示列定制】外，其他涉及权限的按钮 id 需要和权限进行对应，否则按钮渲染出错。举例说明：**

    |  权限项                 | 按钮 id   |
    |  :----:                | :----:   |
    | ic-ldap-baseSet-add    | add      |
    | ic-ldap-baseSet-batchDelete | batchDelete |


3. 在【资源申请】-> 【E10】-> 【权限设置】->【权限菜单】中制作添加菜单权限
4. 告知前端同事菜单权限的值