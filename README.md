# EaselJS-ScrollContainer

![2016-05-07 18 38 56](https://cloud.githubusercontent.com/assets/5355966/15091406/45bd814c-1483-11e6-8ca8-24e80be7efeb.png)

EaselJS extension adds ScrollContainer to CreateJS.

ScrollContainer provides scroll bars and you can use as normal Container.

## Usage

1. instantiate ScrollContainer with canvas element
2. set contentSize and bounds to calculate bar size
3. add to stage
4. add object to ScrollContainer by calling `addChild`

```js
const scroll = new createjs.ScrollContainer(canvas)
scroll.x = 30
scroll.y = 90
scroll.setBounds(0, 0, 520, 300)
scroll.contentSize = {
  width: 1200,
  height: 960
}
stage.addChild(scroll)

const circle = new createjs.Shape()
circle.graphics.beginFill("DeepSkyBlue").drawCircle(0, 0, 50)
circle.x = 100
circle.y = 100
scroll.addChild(circle)
```

## Features

- Shows scroll bar like Windows 10
- Scroll by the mouse wheel
- Scroll by bar dragging

## Issues

- This does not clip children
