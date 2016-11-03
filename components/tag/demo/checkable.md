---
order: 1
title:
  zh-CN: 可选择
  en-US: Checkable
---

## zh-CN

设置 `checkable` 属性后，标签将可以被选择。同时 `defaultChecked` `checked` `onChange` 属性也会生效。

## en-US

We can set `checkable` to make a Tag checkable, and `defaultChecked` `checked` `onChange` will be enable.

````jsx
import { Tag } from 'antd';

const ControlledTag = React.createClass({
  getInitialState() {
    return { checked: false };
  },
  handleChange(checked) {
    this.setState({ checked });
  },
  render() {
    return (
      <Tag
        bordered={false}
        checkable
        checked={this.state.checked}
        onChange={this.handleChange}
      >
        Controlled
      </Tag>
    );
  },
});

function log(checked) {
  console.log('Current checked: ', checked);
}

ReactDOM.render(
  <div>
    <Tag checkable onChange={log}>Default</Tag>
    <Tag bordered={false} checkable onChange={log}>Simple</Tag>
    <ControlledTag />
  </div>,
  mountNode
);
````
