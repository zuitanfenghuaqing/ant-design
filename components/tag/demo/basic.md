---
order: 0
title:
  zh-CN: 基本
  en-US: Basic
---

## zh-CN

标签有 `default` 和 `simple` 两种风格，并可以通过设置 `closable` 把标签设为可关闭。

## en-US

Tag has two types of style, `default` and `simple`. And we can set `closable` to make tags closable.

````jsx
import { Tag } from 'antd';

function onClose(e) {
  console.log(e);
}

ReactDOM.render(
  <div>
    <Tag>Tag 1</Tag>
    <Tag closable onClose={onClose}>Tag 2</Tag>
    <Tag closable onClose={onClose}>
      <a href="https://github.com/ant-design/ant-design/issues/1862">Tag 3</a>
    </Tag>
    <br />
    <Tag type="simple">Tag 4</Tag>
    <Tag type="simple" closable onClose={onClose}>Tag 5</Tag>
    <Tag type="simple" closable onClose={onClose}>
      <a href="https://github.com/ant-design/ant-design/issues/1862">Tag 6</a>
    </Tag>
  </div>,
  mountNode
);
````
