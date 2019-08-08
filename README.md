### cat-signature

+ cat-signature 是一款基于uni-app开发的canvas手绘签名组件

### 参数说明
| 参数名 | 类型 | 默认值| 说明 |
| ---- | ---- |---- |---|
| visible | Boolean | false |显示手绘板 |
| canvasId | String | firstCanvas | canvas-id 一个页面如有多个建议写成不同的 |
| @close | Function |  | 点击遮罩事件 |
| @clear | Function |  | 点击清除事件 |
| @save(img) | Function |  | 点击保存事件 img参数为生成的图片（h5 返回base64,其他返回路径） |

+ 如有问题欢迎提问