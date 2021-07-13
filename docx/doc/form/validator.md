# 校验规则

## 校验

form 表单会设计到必填等校验 [基础校验规则列表](https://learnku.com/docs/laravel/5.7/validation/2262#c58a91)。设置方式： 在 `rules` 中设置需要的校验规则，多个规则通过 | 隔开。后端接口返回校验规则如下：
```json
{
  "code": 200,
  "msg": "接口返回成功",
  "status": true,
  "data": {
    // 按钮相关的信息
    "button": [],
    // form 表单的相关信息
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
          ]
        ],
        "data": {},
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
            "rules": "required|stringLength:200", // rules 中设置校验规则，多个规则用 | 隔开
            "placeholder": "请输入",
            "readOnly": false,
            "required": false,     // required 为 true，表示必填。和 rules 中设置 "required" 等价
            "otherParams": {
              "stringLength": 200
            }
          }
        }
      }
    }
  }
```

## 联动隐现

form 表单涉及联动隐现时，在 `otherParams` 中设置 `showWhere` 属性，控制联动隐现的项。约定数据格式按下面方式返回：
```json
{
  "code": 200,
  "msg": "接口返回成功",
  "status": true,
  "data": {
    // 按钮相关的信息
    "button": [],
    // form 表单的相关信息
      "formSetting": {
        "layout": [
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
          ]
        ],
        "data": {},
        "groups": [
          {
            "id": "IntLoginBaseInfo",
            "title": "基本信息",
            "visible": true,
            "custom": false
          }
        ],
        "items": {
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
            "defaultValue": "get"
          },
          "urlEncode": {
            "itemType": "SWITCH",
            "value": true,
            "otherParams": {
              "showWhere": [ // 字段需要做联动隐现时，在 otherParams 中添加 showWhere 字段
                { "value": ["get"], "id": "requestMethod" }  // urlEncode 字段在 requestMethod 值不为 get 时隐藏
              ]
            }
          }
        }
      }
    }
  }
```