---
order: 2
title:
  zh-CN: 动态添加和删除
  en-US: Add and Remove Dynamically
---

## zh-CN

用数组生成一组标签，可以动态添加和删除。

删除动画结束时会触发 `afterClose` 事件。

## en-US

Generating a set of tags from array, and you can add and remove them dynamically.

`afterClose` event will be triggered while the closing animation is completed.

````jsx
import { Tag, Button } from 'antd';

let index = 3;
const EditableTagGroup = React.createClass({
  getInitialState() {
    return {
      tags: [
        { key: 1, name: 'Unremovable' },
        { key: 2, name: 'Tag 2' },
        { key: 3, name: 'Tag 3' },
      ],
    };
  },
  handleDelete(key) {
    const tags = [...this.state.tags].filter(tag => (tag.key !== key) && tag);
    console.log(tags);
    this.setState({ tags });
  },
  handleAddtag() {
    const tags = [...this.state.tags];
    index += 1;
    tags.push({ key: index, name: `New tag ${index}` });
    this.setState({ tags });
  },
  render() {
    const { tags } = this.state;
    return (
      <div>
        {tags.map(tag =>
          <Tag key={tag.key} closable={tag.key !== 1} afterClose={() => this.handleDelete(tag.key)}>
            {tag.name}
          </Tag>
        )}
        <Button size="small" type="dashed" onClick={this.handleAddtag}>+ New tag</Button>
      </div>
    );
  },
});

ReactDOM.render(<EditableTagGroup />, mountNode);
````
