# vscode自定义Markdown样式

## 下载插件
 在`Activity Bar（左边栏）`的`Extension`中搜索`Markdown Preview Enhanced`插件，下载并应用；
## 修改style.less
键盘键入`Ctrl+Shift+P`，调出`命令面板`，在搜索框中输入`markdown-preview-enhanced.customizeCss`,进入`style.less`文件并修改css代码以改变markdown样式
## 样式代码
``` css 
.markdown-preview.markdown-preview {
  line-height: 1.8;
  color: #2b2b2b;
  font-family: "Roboto Mono","Arial";
  letter-spacing: 2px;   
  background-image: linear-gradient(90deg, rgba(50, 0, 0, 0.04) 3%, rgba(0, 0, 0, 0) 3%), linear-gradient(360deg, rgba(50, 0, 0, 0.04) 3%, rgba(0, 0, 0, 0) 3%);
  background-size: 20px 20px;
  background-position: center center;
  
  p{
    font-size:15px !important;
  }
  /* 一级标题 */
  
  h1 {
    display: table;
    margin: 30px auto 20px auto !important;
    padding: 10px !important;
    background-image: linear-gradient(to left,     rgb(253, 213, 231), rgb(194, 226, 249));
    border-width: 1px;
    border-radius: 10px;
    box-shadow: 3px 3px 3px #ccc;
    font-size: 20px !important;
    text-align:center;
  }
  
  h2 {
    display: table;
    margin: 30px auto 20px auto !important;
    padding: 0px 10px !important;
    border-bottom: 5px solid #205792;
    text-align: center;
    font-size: 18px !important;
  }
  
  
  /* 三级标题 */
  
  h3 {
    border-bottom: #2b2b2b;
  }
  
  h3:before {
    content: "✒️ ";
  }
  
  h4 {}
  
  h4:before {
    content: "✏️";
  }
  
  h5 {
    background-color: #f1f1f1;
    border-left: 5px solid #fff;
    padding-left: 5px !important;
    box-shadow: -3px 0px #205792;
  }
  
  h6 {
    border-left: 5px solid rgba(0, 0, 0, 0);
    box-shadow: 0px 2px #205792;
  }
  img{
    width:95%;
    margin: 5px auto 8px auto !important;
    border-radius: 5px;
    box-shadow:3px 2px 3px #ccc ;
  }
  strong{
    color:#ff4c00 !important;
  }
  em{ 
    font-weight:800;
    font-style:normal !important;
  }
}
```