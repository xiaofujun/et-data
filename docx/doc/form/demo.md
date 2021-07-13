# 示例 demo

以集成登录设置的新建为例：
```json
{
  "code": 200,
  "msg": null,
  "status": true,
  "data": {
    // 按钮信息
    "button": [],
    // form 表单的信息
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
        ],
        [
          {
            "id": "outerUrl",
            "label": "单点登录地址",
            "items": [
              "outerUrl"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ],
        [
          {
            "id": "requestMethod",
            "label": "请求方式",
            "items": [
              "requestMethod"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ],
        [
          {
            "id": "urlEncode",
            "label": "启用编码",
            "items": [
              "urlEncode"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ],
        [
          {
            "id": "authObj",
            "label": "适用对象",
            "items": [
              "authObj"
            ],
            "groupId": "IntLoginBaseInfo",
            "labelSpan": 8,
            "hide": false
          }
        ]
      ],
      "data": {
        "appName": null,
        "requestMethod": "get",
        "outerUrl": null,
        "thirdName": null,
        "authObj": null,
        "urlEncode": 0,
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
        "outerUrl": {
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
        "requestMethod": {
          "itemType": "SELECT",
          "data": [
            {
              "id": "post",
              "content": "POST请求"
            },
            {
              "id": "get",
              "content": "GET请求"
            }
          ],
          "value": "get"
        },
        "authObj": {
          "itemType": "TYPESBROWSER",
          "visible": true,
          "disable": false,
          "required": false,
          "readOnly": false,
          "multiple": false,
          "common": false,
          "typesBrowserBean": {
            "module": "hrm",
            "type": "hrmcombination",
            "options": [
              {
                "id": "user",
                "content": "人员",
                "messageId": 0,
                "disabled": false,
                "addData": null,
                "prevBrowser": null
              },
              {
                "id": "dept",
                "content": "部门",
                "messageId": 0,
                "disabled": false,
                "addData": null,
                "prevBrowser": null
              },
              {
                "id": "all",
                "content": "所有人",
                "messageId": 0,
                "disabled": false,
                "addData": null,
                "prevBrowser": null
              }
            ],
            "browsers": {
              "all": {
                "hasAdvanceSearch": false,
                "hasLeftData": false,
                "disabledTabCache": false,
                "showCheckStrictly": true,
                "canSelectAllUser": false,
                "module": "hrm",
                "type": "all",
                "multiple": false,
                "defaultOpen": false,
                "multCheckbox": false,
                "multType": false
              },
              "dept": {
                "hasAdvanceSearch": false,
                "hasLeftData": false,
                "disabledTabCache": false,
                "showCheckStrictly": true,
                "canSelectAllUser": false,
                "module": "hrm",
                "type": "department",
                "multiple": false,
                "defaultOpen": false,
                "multCheckbox": false,
                "multType": false
              },
              "user": {
                "hasAdvanceSearch": false,
                "hasLeftData": false,
                "disabledTabCache": false,
                "showCheckStrictly": true,
                "canSelectAllUser": false,
                "module": "hrm",
                "type": "resource",
                "multiple": false,
                "defaultOpen": false,
                "multCheckbox": false,
                "multType": false
              }
            },
            "multiple": true
          },
          "otherParams": {}
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
        },
        "urlEncode": {
          "itemType": "SWITCH",
          "defaultValue": true,
          "otherParams": {
            "showWhere": [
              {
                "id": "requestMethod",
                "value": [
                  "get"
                ]
              }
            ]
          }
        }
      }
    }
  }
}
```