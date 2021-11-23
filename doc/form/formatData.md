# 表单 itemType 详解


| 组件 | 描述 | 使用 demo | 前端调用保存接口时传值 | 后端返回表单渲染数据 | 集成中心示例
| :---  | :--- | :--- | :--- | :--- | :---
| switch | 开关组件 | [http://cloudstore.e-cology.cn:81/ui/switch](http://cloudstore.e-cology.cn:81/ui/switch) | `开启传值 1`, `关闭传值 0` | 开启值为 '1' 或者 1，关闭值为 '0' 或者 0 （推荐统一返回字符串的 '1' 和 '0'） | `日程会议集成`页面
| checkbox | 多选框组件 | [http://cloudstore.e-cology.cn:81/ui/checkbox](http://cloudstore.e-cology.cn:81/ui/checkbox) | `勾选传值 1`, `未勾选传值 0` | 勾选值为 '1' 或者 1，未勾选值为 '0' 或者 0 （推荐统一返回字符串的 '1' 和 '0'） | 
| upload | 上传组件 | [http://cloudstore.e-cology.cn:81/ui/upload](http://cloudstore.e-cology.cn:81/ui/upload) | `上传文件的 fileId` | 根据上传文件 fileId 获取的所有信息 | `集成登录新建`页面（上传图标）
| typesbrowser | 人员权限范围组件 | [http://cloudstore.e-cology.cn:81/ui/typesbrowser](http://cloudstore.e-cology.cn:81/ui/typesbrowser) |  |  | `集成登录新建`页面（适用对象）
