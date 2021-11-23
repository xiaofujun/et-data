# 数据格式

以集成登录设置的新建为例：
```json
{
  "code": 200,
  "msg": null,
  "status": true,
  "data": {
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
          "width": "70%"
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
          "rules": "required|stringLength:50",
          "placeholder": "请输入",
          "readOnly": false,
          "required": false,
          "otherParams": {
            "autoFocus": false,
            "stringLength": 50
          }
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
      "data": []
    }
  }
}
```