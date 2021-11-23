# 表单数据格式

以集成登录设置的新建为例：
```json
{
  "code": 200,
  "msg": null,
  "status": true,
  "data": {
    "formSetting": {
      "layout": [
        [
          {
            "id": "appName",
            "label": "应用名称",
            "items": [
              "appName"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ],
        [
          {
            "id": "thirdName",
            "label": "第三方系统名称",
            "items": [
              "thirdName"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ]
      ],
      "data": {
        "appName": null,
        "thirdName": null,
      },
      "groups": [
        {
          "id": "IntLoginBaseInfo",
          "title": "基本信息",
          "visible": true,
          "custom": false
        }
      ],
      "items": {
        "appName": {
          "itemType": "INPUT",
          "rules": "required|stringLength:200",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": false,
            "stringLength": 200
          }
        },
        "thirdName": {
          "itemType": "INPUT",
          "rules": "required|stringLength:200",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": false,
            "stringLength": 200
          }
        }
      }
    }
  }
}
```