---
order: 0
title: 简单的图片选择组件
-----------


````jsx
import { ImagePicker } from 'antd-mobile';

const ImagePickerExample = React.createClass({
  getInitialState() {
    return {
      files: [{
        url: 'https://zos.alipayobjects.com/rmsportal/PZUUCKTRIHWiZSY.jpeg',
        id: '2121',
      }, {
        url: 'https://zos.alipayobjects.com/rmsportal/hqQWgTXdrlmVVYi.jpeg',
        id: '2122',
      }],
    };
  },
  render() {
    return (
      <div>
        <ImagePicker
          onChange={(files, type, index) => {
            console.log(files);
            console.log(type);
            console.log(index);
            this.setState({
              files,
            });
          }}
          onImageClick={(index, files) => {
            console.log(index);
            console.log(files);
          }}
          files={this.state.files}
        />
      </div>
    );
  },
});

ReactDOM.render(<ImagePickerExample />, mountNode);
````
