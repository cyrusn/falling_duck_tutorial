# Flappy Duck Tutorial

### ~button https://arcade.makecode.com/#tutorial:https://github.com/skhlpss/flappy_duck_tutorial

Try this tutorial!

### ~`

## 簡介 @unplugged

![school logo](https://liping.edu.hk/download/Resource/BGImage/201710261432147745579.png)

歡迎來到聖公會李炳中學的電腦教室

今日會學懂如何編寫一個 Flappy Duck 遊戲，希望當中能讓你學懂簡單的編程概念。

![duck](https://arcade.makecode.com/static/blocks-games.gif)

## 步驟 1 @fullscreen

首先，在左方選單中，點擊 `||Sprites: Sprites||` ，將方塊
`||variables: set mySprite to sprite of kind Player||`
拖拉到 `||loops:on start||` 方塊之內。點擊 `||sprites:sprite||` 旁的灰色圖像，在 `Gallery` 選單中選擇小鴨圖案。

```blocks
// @highlight
mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . .
    . . . . . . . . . b 5 b . . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . . . . b b 5 d 1 f 5 5 d f . .
    . . . . b 5 5 1 f f 5 d 4 c . .
    . . . . b 5 5 d f b d d 4 4 . .
    . b b b d 5 5 5 5 5 4 4 4 4 4 b
    b d d d b b d 5 5 4 4 4 4 4 b .
    b b d 5 5 5 b 5 5 5 5 5 5 b . .
    c d c 5 5 5 5 d 5 5 5 5 5 5 b .
    c b d c d 5 5 b 5 5 5 5 5 5 b .
    . c d d c c b d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
    . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
```

## 步驟 2 @fullscreen

在 `||scene: Scene||` 選單中，將 `||scene:set background color ||` 拖到 `||loops: on start||` 之內。在 `||scene: set background color ||` 方塊中，將顏色設定為淺藍色。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
// @highlight
scene.setBackgroundColor(9)
```

## 步驟 3 @fullscreen

在 `||scene: Scene||` 選單中，將 `||scene: start screen confetti effect ||` 拖到 `||loops: on start||` 之內。然後在 `||scene: start screen confetti effect ||` 方塊中，將效果設定為 `blizzard`。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
// @highlight
effects.blizzard.startScreenEffect()
```

## 步驟 4 @fullscreen

在 `||sprites:Sprites||` 選單中拖拉 `||sprites: set mySprite x to 0||` 到 `||loops: on start||` 內的最下方。然後在 `||math: Math||` 中拖拉 `||math: 0 ÷ 0||` 到 `||sprites: set mySprite x to 0||` 的 `||sprites: 0||` 上。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
// @highlight
mySprite.x = 0 /0
```

## 步驟 5 @fullscreen

在 `||scene: Scene||` 選單中拖拉 `||scene: screen width||` 到 `||math: 0 ÷ 0||` 的第一個 `||math:0||` 上，使之變成 `||math: screen width ÷ 3||`。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
// @highlight
mySprite.x = scene.screenWidth() / 3
```

## 步驟 6 @fullscreen

在 `||sprites:Sprites||` 選單中拖拉 `||sprites: set mySprite x to 0||` 到 `||loops:on start||` 內的最下方。點擊該方塊中的 `||sprites:x ▼||` ，揀選 `||sprites:ay (acceleration y)||`，並將數值改為 `300`。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
// @highlight
mySprite.ay = 300
```

## 步驟 7 @fullscreen

打開 `|Advanced|` 選單，在 `||arrays:Arrays||` 選單中拖拉 `||set list ▼ to array of 1 2 (-) (+)||` 到 `||loops: on start||` 內的最下方。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
// @highlight
let list = [1, 2]
```

## 步驟 8 @fullscreen

點擊 `||variables: list||` ，揀選 `Rename varaible ...` 將 `||varaible:list||` 改名為 `topLogImages` ，並按 `(+)` 兩次，使得 `||arrays:list||` 中有 4 個 `element` 。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
// @highlight
let topLogImages = [1, 2, 0, 0]
```

## 步驟 9 @fullscreen

在 `||images:Images||` 選單中，拖拉**有下拉選單的** image 4 次到 `||variable:topImages||` 中的四個 `element` 內。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
// @highlight
let topLogImages = [
    sprites.food.smallBurger,
    sprites.food.smallBurger,
    sprites.food.smallBurger,
    sprites.food.smallBurger
]
```

## 步驟 10 @fullscreen

將 4 個圖形依次改為第 5、6、7 及 8 顆樹。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
// @highlight
let topLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
```

## 步驟 11 @fullscreen

在 `||varaiables:set topLogImages to array of ...||` 方塊上點擊右鍵按 `Duplicate` 複製方塊，並將方塊放到 `||loops: on start||` 內的最下方。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
let topLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
// @highlight
let topLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
```

## 步驟 12 @fullscreen

在剛複製出來的方塊上，點擊方塊上的 `||variables:topLogImages ▼||`，揀選 `New variable ...` ，命名為 `||variables:bottomLogImages||`

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
let topLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
// @highlight
let bottomLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
```

## 步驟 13 @fullscreen

將 `||variables:bottomLogImages||` 中的 4 個圖形依次改為第 4、3、2 及 1 顆樹。

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . .
    . . . . . . . . . . . . . . . .
    . . . . . . . . . b 5 5 b . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . b b b b b 5 5 5 5 5 5 5 b . .
    . b d 5 b 5 5 5 5 5 5 5 5 b . .
    . . b 5 5 b 5 d 1 f 5 d 4 f . .
    . . b d 5 5 b 1 f f 5 4 4 c . .
    b b d b 5 5 5 d f b 4 4 4 4 b .
    b d d c d 5 5 b 5 4 4 4 4 4 4 b
    c d d d c c b 5 5 5 5 5 5 5 b .
    c b d d d d d 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
scene.setBackgroundColor(9)
effects.blizzard.startScreenEffect()
mySprite.x = scene.screenWidth() / 3
mySprite.ay = 300
let topLogImages = [
    sprites.duck.log5,
    sprites.duck.log6,
    sprites.duck.log7,
    sprites.duck.log8
]
// @highlight
let bottomLogImages = [
    sprites.duck.log4,
    sprites.duck.log3,
    sprites.duck.log2,
    sprites.duck.log1
]
```

## 步驟 14 @fullscreen

在 `||Controller:Controller||` 選單中拖拉 `||controller: on A ▼ button pressed||` 到主版面的空白位置上，點擊 `||controller:A ▼||` ，並揀選 `||controller:any||`。然後在 `||sprites:Sprites||` 中拖拉 `||sprites: set mySprite x to 0||` 到 `||controller: on any button pressed||` 內

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
        // @highlight
    mySprite.x = 0
})
```

## 步驟 15 @fullscreen

在 `||sprites: Sprites||` 選單中拖拉 `||sprites: mySprite ▼ start spray ▼ effect ||` 到 `||controller: on any button pressed||` 內的最下方。點擊 `||sprites: spray ▼||`
揀選 `||sprites: halo||`。

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x = 0
    // @highlight
     mySprite.startEffect(effects.halo)
})
```

## 步驟 16 @fullscreen

在 `||music: Music||` 選單中拖拉 `||music: play sound ba ding ||` 到 `||controller: on any button pressed||` 內的最下方。點擊 `||music: ba ding ▼||`
揀選 `||music: magic wand||`。

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.x = 0
    mySprite.startEffect(effects.halo)
    // @highlight
    music.magicWand.play()
})
```

## 步驟 17 @fullscreen

點擊 `||sprites: set mySprite x to 0||` 中的 `||sprites:x ▼||` ，揀選 `||sprites:vy (velocity y)||` ，並將數值改為 `-100`。 `velocity` 解作速度，負值代表向上，意思將小鴨的速度改成向上 100。

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    mySprite.vy = -100
})
```

## 步驟 18

完成後，請到左方版面進行測試。雙擊左方模擬器，開始遊戲後，試試按空白鍵，看看小鴨會否飛。

## 步驟 19 @fullscreen

`||game:Game||` 選單中，拖拉 `||game:on game update every 500 ms||` 到主版面，將數值改為 `1500`。

```blocks
game.onUpdateInterval(1500, function () {
})
```

## 步驟 20 @fullscreen

在 `||info:Info||` 選單中拖拉 `||info:change score by 1 ||` 到 `||game:on game update every 1500 ms||` 方塊之內。

```blocks
game.onUpdateInterval(1500, function () {
    // @highlight
    info.changeScoreBy(1)
})
```

## 步驟 21 @fullscreen

在 `||variables:Variables||` 選單中，點擊 `Make a variable`，建立 `||variables:logType||` `variable`。在 `||variables:Variables||` 拖拉 `||variables: set logtype to 0 ||` 到 `||game:on game update every 1500 ms||` 內的最下方。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    // @highlight
    logType = 0
})
```

## 步驟 22 @fullscreen

在 `||math:Math||` 選單中，拖拉 `||math:pick random 0 to 10||` 到 `||variables: set logType to 0 ||` 的 `||variables:0 ||` 上。並將數值由 `||math:0 to 10||` 改為 `||math:0 to 3||`。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    // @highlight
    logType = Math.randomRange(0, 3)
})
```

## 步驟 23 @fullscreen

在 `||sprites:Sprites||` 選單中，拖拉 `||variables:set projectile to ...  from side with ...||` 到 `||game:on game update every 1500 ms||` 內。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    // @highlight
        let projectile = sprites.createProjectileFromSide(img`
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `, 50, 100)
})
```

## 步驟 24 @fullscreen

在 `||arrays:Arrays||` 選單中，拖拉 `||arrays: list ▼ get value at 0 ||` 到 `projectile` 及 `from side with vx ..` 之間的灰色圖案上。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    // @highlight
    let list: Sprite[] = []
    let projectile = sprites.createProjectileFromSide(list[0], 50, 100)
})
```

## 步驟 25 @fullscreen

點擊 `||variables:list ▼||`，揀選 `||variables:topLogImages||`。在 `||variables:Variables||` 選單中，拖拉 `||variables: logType||` 到 `||arrays: list ▼ get value at 0 ||` 的 `||arrays:0||` 之上。然後分別將 `||sprites:vx||` 及 `||sprites:vy||` 的值改為 `-45` 及 `0`

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    // @highlight
    let projectile = sprites.createProjectileFromSide(topLogImages[logType], -45, 0)
})
```

## 步驟 26 @fullscreen

在 `||sprites: Sprites||` 選單中拖拉 `||sprites: set mySprite x to 0||` 到 `||game:on game update every 1500 ms||` 內的最下方。點擊 `||variables:mySprite ▼||` ，揀選 `||variables:projectile||`。點擊 `||sprites:x ▼||` ，揀選 `||sprites: top||` ，數值不變，維持 `0`

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    let projectile = sprites.createProjectileFromSide(topLogImages[logType], -40, 0)
    // @highlight
    projectile.top = 0
})
```

## 步驟 27 @fullscreen

複製 `||variables:set projectile to projectile topLogImages get ...||` 方塊並將之加到 `||game:on game update every 1500 ms||` 內的最下方。點擊 `||variables:topLogImages ▼||` ，揀選 `||variables:bottomLogImages||`

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    let projectile = sprites.createProjectileFromSide(topLogImages[logType], -40, 0)
    projectile.top = 0
    // @highlight
    let projectile = sprites.createProjectileFromSide(bottomLogImages[logType], -40, 0)
})
```

## 步驟 28 @fullscreen

複製 `||sprites:set projectile top to 0||` 方塊，並將之加到 `||game:on game update every 1500 ms||` 內的最下方。點擊 `||sprites:top ▼||`，揀選 `||sprites:bottom||` 。在 `||scene:Scene||` 中拖拉 `||scene:screen height||` 到 `||sprites:set projectile bottom to 0||` 中的 `||sprites:0||` 上。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    logType = Math.randomRange(0, 3)
    let projectile = sprites.createProjectileFromSide(topLogImages[logType], -40, 0)
    projectile.top = 0
    let projectile = sprites.createProjectileFromSide(bottomLogImages[logType], -40, 0)
    // @highlight
    projectile.bottom = scene.screenHeight()
})
```

## 進行測試

完成後，請到左方模擬器測試結果。小鴨應該除了能飛以外，上下兩方應該有樹由右之左飛出來。

## 步驟 29 @fullscreen

在 `||game: Game||` 選單中，拖拉 `||game: on game update||` 到主版上。

```blocks
// @highlight
game.onUpdate(function () {
})
```

## 步驟 30 @fullscreen

在 `||logic: Logic||` 選單中，拖拉 `||logic:if true then||` 到 `||game: on game update||` 中，並在 `||game:Game||` 中拖拉 `||game:game over LOSE||` 方塊到 `||logic:if true then||` 內。

```blocks
game.onUpdate(function () {
    // @highlight
    if (true) {
        game.over(false)
    }
})
```

## 步驟 31 @fullscreen

在 `||logic: Logic||` 選單中，拖拉 `||logic: <> or <> ||` 到 `||logic:if true then||` 的 `||logic:true||` 上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if (false || false) {
        game.over(false)
    }
})
```

## 步驟 32 @fullscreen

在 `||logic: Logic||` 選單中，拖拉 `||logic: 0 < 0 ||` 到 `||logic: <> or <> ||` 中的前後兩個**條件**上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( 0 < 0) || ( 0 < 0)) {
        game.over(false)
    }
})
```

## 步驟 33 @fullscreen

在第二個條件中，點擊將在方塊 `||logic: 0 < 0 ||` 中的 `||logic:< ▼||` ，揀選 `||logic:> ||`

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( 0 < 0) || ( 0 > 0)) {
        game.over(false)
    }
})
```

## 步驟 34 @fullscreen

在 `||sprites: Sprites||` 選單中，拖拉 `||sprites: mySprite x ||` 到第一個條件上的第一個 `||logic:0||`。點擊 `||sprites: x ▼||` ，並揀選 `||sprites: top ||`。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( mySprite.top < 0) || ( 0 > 0)) {
        game.over(false)
    }
})
```

## 步驟 35 @fullscreen

在 `||sprites: Sprites||` 選單中，拖拉 `||sprites: mySprite x ||` 到第二個條件上的第一個 `||logic:0||`。點擊 `||sprites: x ▼||` ，並揀選 `||sprites: bottom ||`。在 `||scene: Scene||` 中拖拉 `||scene: screen height ||` 到第二個條件上的第二個 `||logic:0||` 上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( mySprite.top < 0) || ( mySprite.bottom > scene.screenHeight())) {
        game.over(false)
    }
})
```

## 步驟 36 @fullscreen

在 `||sprites:Sprite||` 選單中，拖拉 `||sprites:on sprite of kind player overlaps ...||` 到主版中。點擊方塊中**最後**的一個 `||sprites: Player ▼||`，揀選 `||sprites: Projectile||`。最後將 `||game: game over LOSE||` 拖到這個方塊之內。

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Player, SpriteKind.Projectile, function (sprite, otherSprite) {
    game.over(false)
})
```
