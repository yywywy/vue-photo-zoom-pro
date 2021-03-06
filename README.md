# vue-photo-zoom-pro

> Vue(2.x) 图片放大器(Photoloupe)

![example](example.png)

[demo](https://codepen.io/xbup/project/editor/AjnEgE)

## Usage example

```js

npm install vue-photo-zoom-pro

```

main.js

```js
import VuePhotoZoomPro from 'vue-photo-zoom-pro'

Vue.use(VuePhotoZoomPro)
```

*.vue

```html
<vue-photo-zoom-pro url="https://bpic.588ku.com/illus_water_img/18/07/30/f3c7060bc28216271dc8c4630b288331.jpg!/watermark/url/L3dhdGVyL3dhdGVyX2JhY2tfNDAwXzIwMC5wbmc=/repeat/true"
></vue-photo-zoom-pro>
```

### Settings

| Prop          | Type              | Default | Note                                                                                                                                             |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| url           | String            |         | 图片地址(photo url)                                                                                                                              |
| high-url      | String            |         | 更清晰的图片,若不提供会采用 url(more detailed photo url)                                                                                         |
| scale         | Number            | 3       | 放大倍数(scale)                                                                                                                                  |
| width         | Number            | 166     | 放大镜宽度(width of magnifying glass)                                                                                                            |
| selectorStyle | Object            | {}      | 放大镜样式(style of magnifying glass)                                                                                                            |
| type          | String            | square  | 放大镜类型(circle,square)(magnifying glass type (circle,square))                                                                                 |
| hide-zoom     | Boolean           | false   | 隐藏放大镜，图像加载时不会显示放大镜(hide magnifying)                                                                                            |
| out-show      | Boolean           | true    | 图片展示区域会在图片外部(image will be displayed on the outside)                                                                                 |
| pointer       | Boolean           | false   | 外部区域的中心点 (The center of an external area)                                                                                                |
| baseline      | Boolean           | false   | 外部区域的基线 (The baseline of the external area)                                                                                               |
| move-event    | Object/mouseEvent | null    | 当需要在外部监听移动事件时,请通过该字段传入事件（必须包含 pageX,pageY,clientY）(When you need to listen for moving events outside the component) |
| leave-event   | Object/mouseEvent | null    | 当需要在外部监听离开事件时，请通过该字段传入事件(When you need to listen for leaving events outside the component)                               |

---

| Slot | Note                                                               |
| ---- | ------------------------------------------------------------------ |
|      | 内容将会在放大镜内部显示(content will display in magnifying glass) |

---

| Method | Note                                |
| ------ | ----------------------------------- |
| reset  | 重置放大镜位置(reset zoom position) |

---

| Event   | Note                               | event                                       |
| ------- | ---------------------------------- | ------------------------------------------- |
| created | 图片放大镜创建(photo-zoom created) | 图片属性(photo prop)(top,left,width,height) |

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

## License

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2018-present, xbup
