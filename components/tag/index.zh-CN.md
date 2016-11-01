---
category: Components
subtitle: 标签
type: Views
title: Tag
---

进行标记和分类的小标签。

## 何时使用

- 用于标记事物的属性和维度。
- 进行分类。

## API

| 参数           | 说明                           | 类型  | 默认值 |
|----------------|-------------------------------|------|--------|
| type           | 设置 Tag 的风格               | `'default' | 'simple'` | 'default' |
| checkable      | 让 Tag 具有类似 Checkbox 的行为| boolean    | false  |
| checked        | 指定当前是否选中               | boolean    | - |
| defaultChecked | 初始是否选中                  | boolean    | - |
| onChange       | 变化时回调函数                 | function(checked) | - |
| closable       | 标签是否可以关闭               | boolean    | false  |
| onClose        | 关闭时的回调                   | function(event) | - |
| afterClose     | 关闭动画完成后的回调             | function(event) | - |
