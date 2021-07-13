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
    // 参数设置可编辑列表信息
    "customParam": {
      "title": "自定义参数",
      "deleteConfirm": true,
      "sortableType": true,
      "columns": [
        {
          "title": "参数名",
          "dataIndex": "paramName",
          "comKey": "paramName",
          "showRequired": true,
          "width": "30%"
        },
        {
          "title": "备注",
          "dataIndex": "remark",
          "comKey": "remark",
          "showRequired": false,
          "width": "30%"
        },
        {
          "title": "参数值",
          "dataIndex": "paramTypeId",
          "comKey": [
            "paramTypeId",
            "paramValue"
          ],
          "showRequired": false,
          "width": "40%"
        }
      ],
      "comProps": {
        "remark": {
          "itemType": "INPUT",
          "rules": "stringLength:255",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": true,
            "stringLength": 255
          }
        },
        "paramName": {
          "itemType": "INPUT",
          "rules": "required|intUnique|stringLength:50",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": false,
            "stringLength": 50
          }
        },
        "paramTypeId": {
          "itemType": "SELECT",
          "data": [
            {
              "id": "1",
              "content": "固定值"
            },
            {
              "id": "2",
              "content": "用户录入"
            }
          ],
          "value": "1"
        },
        "paramValue": {
          "itemType": "INPUT",
          "rules": "stringLength:255",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": true,
            "stringLength": 255
          }
        }
      },
      "cascadeRules": {
        "paramTypeId": {
          "1": [
            "paramValue"
          ],
          "2": "[]"
        }
      },
      "topTools": [
        {
          "type": "add",
          "icon": "Icon-add-to03",
          "title": "新增"
        },
        {
          "type": "maximize",
          "icon": "Icon-Global-zoom-in",
          "title": "最大化"
        },
        {
          "type": "batchDelete",
          "icon": "Icon-Batch-delete",
          "title": "删除"
        }
      ],
      "rowTools": [
        {
          "type": "delete",
          "icon": "Icon-delete",
          "title": "删除"
        },
        {
          "type": "insertUp",
          "icon": "Icon-Insert-forward",
          "title": "向前插入一行"
        },
        {
          "type": "insertDown",
          "icon": "Icon-Insert-after-line",
          "title": "向后插入一行"
        },
        {
          "type": "copy",
          "icon": "Icon-copy",
          "title": "复制"
        }
      ],
      "data": [],
      "customValidator": {
        "customRegister": [
          {
            "name": "intUnique",
            "errorMessage": "参数名重复"
          }
        ]
      }
    }
  }
}
```