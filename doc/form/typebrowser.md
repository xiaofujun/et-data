# typeBrowser 数据格式

```json
{
      "layout": [
        [
          {
            "hide": false,
            "groupId": "g3",
            "labelSpan": 4,
            "id": "synDataObj",
            "label": "同步数据范围",
            "otherParams": {
              
            },
            "items": [
              "synDataObj"
            ],
            "order": 0
          }
        ]
      ],
      "data": {
        "synDataObj": "",
      },
      "items": {
        "synDataObj": {
          "itemType": "TYPESBROWSER",
          "visible": true,
          "common": false,
          "disable": false,
          "multiple": false,
          "readOnly": false,
          "typesBrowserBean": {
            "module": "hrm",
            "options": [
              {
                "messageId": 0,
                "disabled": false,
                "id": "user",
                "content": "人员"
              },
              {
                "messageId": 0,
                "disabled": false,
                "id": "dept",
                "content": "部门"
              },
              {
                "messageId": 0,
                "disabled": false,
                "id": "all",
                "content": "所有人"
              }
            ],
            "multiple": true,
            "type": "hrmcombination",
            "browsers": {
              "all": {
                "disabledTabCache": false,
                "multType": false,
                "module": "hrm",
                "multiple": false,
                "enableExtendButton": false,
                "defaultAccount": false,
                "type": "all",
                "hasAdvanceSearch": true,
                "defaultStopDept": false,
                "multCheckbox": false,
                "showCheckStrictly": true,
                "hasLeftData": false,
                "defaultCheckStrictly": true,
                "enableAddData": false,
                "canSelectAllUser": false,
                "defaultOpen": false
              },
              "dept": {
                "disabledTabCache": false,
                "multType": false,
                "module": "hrm",
                "multiple": false,
                "enableExtendButton": false,
                "defaultAccount": false,
                "type": "department",
                "hasAdvanceSearch": true,
                "defaultStopDept": false,
                "multCheckbox": false,
                "showCheckStrictly": true,
                "hasLeftData": false,
                "defaultCheckStrictly": true,
                "enableAddData": false,
                "canSelectAllUser": false,
                "defaultOpen": false
              },
              "user": {
                "disabledTabCache": false,
                "multType": false,
                "module": "hrm",
                "multiple": false,
                "enableExtendButton": false,
                "defaultAccount": false,
                "type": "resource",
                "hasAdvanceSearch": true,
                "defaultStopDept": false,
                "multCheckbox": false,
                "showCheckStrictly": true,
                "hasLeftData": false,
                "defaultCheckStrictly": true,
                "enableAddData": false,
                "canSelectAllUser": false,
                "defaultOpen": false
              }
            }
          },
          "otherParams": {
            "errorType": "popover"
          },
          "required": false
        }
      }
    }

```
