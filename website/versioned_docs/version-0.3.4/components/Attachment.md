---
id: version-0.3.4-attachment
title: Attachment
sidebar_label: Attachment
original_id: attachment
---

## Constructor
**Parameter**

| Name| Type| Required| Description |
| --- | --- | --- | --- |
|options|Object|No|An object contains params of constructor.|
|options.dropZoneText|String|No|Text will show when the file is dragged over the attachment field. (item 7)<br>Default value: 'Drop files here.'|
|options.browseButtonText|String|No|Text of the browse button. (item 4)<br>Default value: 'Browse'|
|options.fileLimitText|String|No|Text of the file limit warn part. (item 5)|
|options.errorMessage|String|No|Error message (item 6)|
|options.isErrorVisible|Boolean|No|Only when it is **true**, "errorMessage" will show.<br>Default value: false|
|options.files|Array&lt;Object&gt;|No|File objects (ref. [https://developer.mozilla.org/en-US/docs/Web/API/File](https://developer.mozilla.org/en-US/docs/Web/API/File))<br>Or objects contain "name" and "size"|
|options.files[].name|String|No|The file name|
|options.files[].size|String|No|The file size|
|options.isVisible|Boolean|No|The attachment component will be visible.<br>Default value: true|

<details class="tab-container" open>
<Summary>View source</Summary>

**Javascript**
```javascript
const attachment = new kintoneUIComponent.Attachment({files: [{name: 'test_1', size: 12345}]});
```

**React**
```jsx
import {Attachment} from '@kintone/kintone-ui-component';
import React from 'react';
 
export default class Plugin extends React.Component {
  state = {
    files: [],
  };
 
  handleFilesAdd = (files) => {
    this.setState({files});
  };
 
  handleFileRemove = (files) => {
    this.setState({files});
  };
 
  render() {
    return (<Attachment files={this.state.files} onFilesAdd={this.handleFilesAdd} onFileRemove={this.handleFileRemove} />);
  }
}
```
</details>