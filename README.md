# Falling Duck Tutorial

### ~button https://arcade.makecode.com/#tutorial:https://github.com/cyrusn/flappy_duck_tutorial

Try this tutorial!

### ~

## 簡介 @unplugged

迎歡來到聖公會李炳中學的電腦教室

今日我們會教你編寫一個簡單的遊戲，希望當中能讓你學懂簡單的編程概念。

``||functions:letGetStart||``

![duck](https://arcade.makecode.com/static/blocks-games.gif)

## 步驟 1 @fullscreen

首先，在左方選單中，點擊 ``||Sprites: Sprites||`` ，將方塊
``||variables: set mySprite to sprite of kind Player||``
 拖拉到 ``||loops:on start||`` 方塊之內。點擊 ``||sprites:sprite||`` 旁的灰色圖像，在 `Gallery` 選單中選擇小鴨圖案。

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

在 ``||scene: Scene||`` 選單中，將 ``||scene:set background color ||`` 拖到 ``||loops: on start||`` 之內。在 ``||scene: set background color ||`` 方塊中，將顏色設定為淺藍色。

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

在 ``||scene: Scene||`` 選單中，將 ``||scene: start screen confetti effect ||`` 拖到 ``||loops: on start||`` 之內。然後在 ``||scene: start screen confetti effect ||`` 方塊中，將效果設定為 `blizzard`。

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

在 ``||sprites:Sprites||`` 選單中拖拉 ``||sprites: set mySprite x to 0||`` 到 ``||loops: on start||`` 內的最下方。然後在 ``||math: Math||`` 中拖拉 ``||math: 0 ÷ 0||`` 到 ``||sprites: set mySprite x to 0||`` 的 ``||sprites: 0||`` 上。

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

在 ``||scene: Scene||`` 選單中拖拉 ``||scene: screen width||`` 到 ``||math: 0 ÷ 0||`` 的第一個 ``||math:0||`` 上，使之變成 ``||math: screen width ÷ 3||``。

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

在 ``||sprites:Sprites||`` 選單中拖拉 ``||sprites: set mySprite x to 0||`` 到 ``||loops:on start||`` 內的最下方。點擊該方塊中的 ``||sprites:x||`` ，揀選 ``||sprites:ay (acceleration y)||``，並將數值改為 `300`。

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

在 ``||Controller:Controller||`` 選單中拖拉 ``||controller: on A button pressed||`` 到主版面的空白位置上，點擊 ``||controller:A||`` ，並揀選 ``||controller:any||``。然後在 ``||sprites:Sprites||`` 中拖拉 ``||sprites: set mySprite x to 0||`` 到 ``||controller: on any button pressed||`` 內

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
        // @highlight
    mySprite.x = 0
})
```

## 步驟 8 @fullscreen

點擊 ``||sprites: set mySprite x to 0||`` 中的 ``||sprites:x||`` ，揀選 ``||sprites:vy (velocity y)||`` ，並將數值改為 `-100`。 **velocity** 解作速度，負值代表向上，意思將小鴨的速度改成向上100。

```blocks
let mySprite: Sprite = null
controller.anyButton.onEvent(ControllerButtonEvent.Pressed, function () {
    // @highlight
    mySprite.vy = -100
})
```

## 步驟 7

完成後，請到左方版面進行測試。雙擊左方模擬器，開始遊戲後，試試按空白鍵，看看小鴨會否飛。

## 步驟 9 @fullscreen

打開 ``|Advanced|`` 選單，在 ``||functions:Functions||`` 選單中，按 `make a function` 將 `function` 的名稱改為 `createLogImage` 。這樣我們便可以建立 ``||functions:function||``

```blocks
// @highlight

function createLogImage () {
}
```

## 步驟 10 @fullscreen

在 ``||variables: Variables||`` 選單中按 `make a variable`，並將 `variable` 的名稱改為 `topLogImage`。在 ``||variables: Variables||`` 中，拖拉 ``||variables: set topLogImage to 0||`` 到 ``||functions:createLogImage||`` 內。

```blocks
function createLogImage () {
    // @highlight
    topLogImage = 0
}
```

## 步驟 11 @fullscreen

在 ``||images:Images||`` 選單中，拖拉**有下拉選單的** image 到 ``||variables: set topLogImage to 0||`` 中的 ``||variables:0||`` 上。然後將圖改為第5個樹幹圖，請確保如圖所示。

```blocks
function createLogImage () {
    // @highlight
    topLogImage = sprites.duck.log5
}
```

## 步驟 12 @fullscreen

在 ``||variables: set topLogImage ...||`` 方塊上按右鍵，揀選 `duplicate` 複製方塊。將複製出來的方塊加到 ``||functions:createLogImage||`` 內最下方。

```blocks
function createLogImage () {
    topLogImage = sprites.duck.log5
    // @highlight
    topLogImage = sprites.duck.log5
}
```

## 步驟 13 @fullscreen

點擊該方塊中的 ``||variables: topLogImage ||`` ，揀選 `New variable...`，將名稱改為 ``||variables:bottomLogImage||``。最後將圖為第4個樹幹圖，需如圖所示。

```blocks
function createLogImage () {
    topLogImage = sprites.duck.log5
    // @highlight
    bottomLogImage = sprites.duck.log4
}
```
## 步驟 14 @fullscreen

如之前建立 `function` 的步驟一樣，建立一個新的 `function` ``||functions:moveLogImage||`` 。然後到 ``||sprites:Sprites||`` 中，拖拉 ``||variables:set projectile ...  from side with ...||`` 到 ``||functions:moveLogImage||`` 內。

```blocks
function moveLogImage () {
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
}
```

## 步驟 15 @fullscreen

在 ``||variables:Variable||`` 選單中，拖拉 ``||variables: topLogImage ||`` 到 `projectile` 及 `from side with vx ..` 之間的灰色圖案上。 (將 `topLogImage` 轉成導彈)。分別將 ``||sprites:vx||`` 及 ``||sprites:vy||`` 的值改為 `-45` 及 `0` 

```blocks
function moveLogImage () {
    // @highlight
    projectile = sprites.createProjectileFromSide(topLogImage, -45, 0)
}
```

## 步驟 16 @fullscreen


在 ``||sprites: Sprites||`` 選單中拖拉 ``||sprites: set mySprite x to 0||`` 到 ``||functions:moveLogImage||`` 內的最下方。點擊 ``||variables:mySprite||`` ，揀選 ``||variables:projectile||``。點擊 ``||sprites:x||`` ，揀選 ``||sprites: top||`` ，數值不變，維持 `0`

```blocks
function moveLogImage () {
    let projectile: Sprite = null
    projectile = sprites.createProjectileFromSide(topLogImage, -45, 0)
    // @highlight
    projectile.top = 0
}
```

## 步驟 17 @fullscreen

複製 ``||variables:set projectile topLogImage from side with ...||`` 方塊並將之加到 ``||functions:moveLogImage||`` 內的最下方。點擊 ``||variables:topLogImage||`` ，揀選 ``||variables:bottomLogImage||``

```blocks
function moveLogImage () {
    let projectile: Sprite = null
    projectile = sprites.createProjectileFromSide(topLogImage, -45, 0)
    projectile.top = 0
    // @highlight
    projectile = sprites.createProjectileFromSide(bottomLogImage, -45, 0)
}

```

## 步驟 18 @fullscreen

複製 ``||sprites:set projectile top to 0||`` 方塊，並將之加到 ``||functions:moveLogImage||`` 內的最下方。點擊 ``||sprites:top||``，揀選 ``||sprites:bottom||`` 。在 ``||scene:Scene||`` 中拖拉 ``||scene:screen height||`` 到 ``||sprites:set projectile bottom to 0||`` 中的 ``||sprites:0||`` 上。

 
```blocks
function moveLogImage () {
    let projectile: Sprite = null
    projectile = sprites.createProjectileFromSide(topLogImage, -45, 0)
    projectile.top = 0
    projectile = sprites.createProjectileFromSide(bottomLogImage, -45, 0)
    // @highlight
    projectile.bottom = scene.screenHeight()
}

```

## 步驟 19 @fullscreen

``||game:Game||`` 選單中，拖拉  ``||game:on game update every 500 ms||`` 到主版面，將數值改為 `1500`。

```blocks
game.onUpdateInterval(1500, function () {
})
```

## 步驟 20 @fullscreen

在 ``||info:Info||`` 選單中拖拉 ``||info:change score by 1 ||`` 到 ``||game:on game update every 1500 ms||`` 方塊之內。

```blocks
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
})
```

## 步驟 21 @fullscreen

在 ``||functions:Functions||`` 選單中，將 ``||functions:call createLogImage||`` 及 ``||functions:call moveLogImage||`` 依次拖拉到 ``||game:on game update every 1500 ms||`` 內的最下方。


```blocks
// @highlight
game.onUpdateInterval(1500, function () {
    info.changeScoreBy(1)
    createLogImage()
    moveLogImage()
})
let projectile: Sprite = null
function createLogImage () {
    topLogImage = sprites.duck.log5
    bottomLogImage = sprites.duck.log4
}
function moveLogImage () {
    projectile = sprites.createProjectileFromSide(topLogImage, -45, 0)
    projectile.top = 0
    projectile = sprites.createProjectileFromSide(bottomLogImage, -45, 0)
    projectile.bottom = scene.screenHeight()
}
```

## 進行測試

完成後，請到左方模擬器測試結果

## 步驟 22 @fullscreen

先將 ``||functions: createLogImage||`` 拖到更大的空間，在 ``||variables:Variables||`` 建立 ``||variables:logType||`` `variable`。在 ``||variables:Variables||`` 拖拉 ``||variables: set logtype to 0 ||`` 到 ``||functions: createLogImage||`` 內的最上方。

```blocks
function createLogImage () {
    // @highlight
    logType = 0
    topLogImage = sprites.duck.log5
    bottomLogImage = sprites.duck.log4
}
```

## 步驟 23 @fullscreen

在 ``||math:Math||`` 選單中，拖拉 ``||math:pick random 0 to 10||`` 到 ``||variables: set logType to 0 ||`` 的 ``||variables:0 ||`` 上。並將數值由 ``||math:0 to 10||`` 改為 ``||math:0 to 3||``。 

```blocks
function createLogImage () {
    // @highlight
    logType = Math.randomRange(0, 3)
    topLogImage = sprites.duck.log5
    bottomLogImage = sprites.duck.log4
}
```

## 步驟 24 @fullscreen

在 ``||logic:Logic||`` 選單中，拖拉 ``||logic:if true then||``，到 ``||functions: createLogImage||`` 中，使得``||logic:if true then||`` 能包著 ``||variables: set topLogImage to ... ||`` 及 ``||variables: set bottomLogImage to ... ||`` 

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    // @highlight
    if (true) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
}
```

## 步驟 25 @fullscreen

在``||logic:Logic||`` 選單中拖拉 ``||logic:0 = 0||`` 到 ``||logic:if true then||`` 的 ``||logic:true||`` 上。在 ``||variables:Variables||`` 中，拖拉 ``||variables:logType||`` 到 ``||logic: 0 = 0 ||`` 的第一個 ``||logic: 0 ||`` 上，使之變成 ``||logic: logType = 0 ||``

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    // @highlight
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
}
```

## 步驟 26 @fullscreen

複製 ``||logic:if logType = 0 then||`` 整個大方塊，並放左 ``||functions:createLogImage||`` 內的最下方。

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
    // @highlight
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
}
```

## 步驟 27 @fullscreen

在最新複製的方塊中，將 ``||logic:logType = 0||`` 改成 ``||logic:logType = 1||``。分別將 ``||variables:topLogImage||`` 及 ``||variables:bottomLogImage||`` 的樹幹圖改成第6個及第3個幅圖，如圖所示。

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
    // @highlight
    if (logType == 1) {
        topLogImage = sprites.duck.log6
        bottomLogImage = sprites.duck.log3
    }
}
```
## 步驟 28 @fullscreen

重覆，複製 ``||logic:if logType = 1 then||``並放左 ``||functions:createLogImage||`` 內的最下方。將 ``||logic:logType = 1||`` 改成 ``||logic:logType = 2||``。分別將 ``||variables:topLogImage||`` 及 ``||variables:bottomLogImage||`` 改成第7個及第2個樹幹圖。

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
    if (logType == 1) {
        topLogImage = sprites.duck.log6
        bottomLogImage = sprites.duck.log3
    }
    // @highlight
    if (logType == 2) {
        topLogImage = sprites.duck.log7
        bottomLogImage = sprites.duck.log2
    }
}
```

## 步驟 29 @fullscreen

重覆，複製 ``||logic:if logType = 2 then||``並放左 ``||functions:createLogImage||`` 內的最下方。將 ``||logic:logType = 2||`` 改成 ``||logic:logType = 3||``。分別將 ``||variables:topLogImage||`` 及 ``||variables:bottomLogImage||`` 改成第8個及第1個樹幹圖。

```blocks
function createLogImage () {
    logType = Math.randomRange(0, 3)
    if (logType == 0) {
        topLogImage = sprites.duck.log5
        bottomLogImage = sprites.duck.log4
    }
    if (logType == 1) {
        topLogImage = sprites.duck.log6
        bottomLogImage = sprites.duck.log3
    }
    if (logType == 2) {
        topLogImage = sprites.duck.log7
        bottomLogImage = sprites.duck.log2
    }
    // @highlight
    if (logType == 3) {
        topLogImage = sprites.duck.log8
        bottomLogImage = sprites.duck.log1
    }
}
```

## 步驟 30 @fullscreen

在 ``||game: Game||`` 選單中，拖拉 ``||game: on game update||`` 到主版上。

```blocks
// @highlight
game.onUpdate(function () {
})
```

## 步驟 31 @fullscreen

在 ``||logic: Logic||`` 選單中，拖拉 ``||logic:if true then||`` 到 ``||game: on game update||`` 中，並在 ``||game:Game||`` 中拖拉 ``||game:game over LOSE||`` 方塊到 ``||logic:if true then||`` 內。 

```blocks
game.onUpdate(function () {
    // @highlight
    if (true) {
        game.over(false)
    }
})
```

## 步驟 32 @fullscreen

在 ``||logic: Logic||`` 選單中，拖拉 ``||logic: <> or <> ||`` 到 ``||logic:if true then||`` 的 ``||logic:true||`` 上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if (false || false) {
        game.over(false)
    }
})
```
## 步驟 33 @fullscreen

在 ``||logic: Logic||`` 選單中，拖拉 ``||logic: 0 < 0 ||`` 到 ``||logic: <> or <> ||`` 中的前後兩個**條件**上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( 0 < 0) || ( 0 < 0)) {
        game.over(false)
    }
})
```

## 步驟 34 @fullscreen

在第二個條件中，將在方塊 ``||logic: 0 < 0 ||`` 中的 ``||logic:< ||`` 改為 ``||logic:> ||``

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( 0 < 0) || ( 0 > 0)) {
        game.over(false)
    }
})
```

## 步驟 35 @fullscreen

在 ``||sprites: Sprites||`` 選單中，拖拉 ``||sprites: mySprite x ||`` 到第一個條件上的第一個 ``||logic:0||``。點擊 ``||sprites: x ||`` ，並揀選 ``||sprites: top ||``。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( mySprite.top < 0) || ( 0 > 0)) {
        game.over(false)
    }
})
```

## 步驟 36 @fullscreen

在 ``||sprites: Sprites||`` 選單中，拖拉 ``||sprites: mySprite x ||`` 到第二個條件上的第一個 ``||logic:0||``。點擊 ``||sprites: x ||`` ，並揀選 ``||sprites: bottom ||``。在 ``||scene: Scene||`` 中拖拉 ``||scene: screen height ||`` 到第二個條件上的第二個 ``||logic:0||`` 上。

```blocks
game.onUpdate(function () {
    let mySprite: Sprite = 0
    // @highlight
    if ( ( mySprite.top < 0) || ( mySprite.bottom > scene.screenHeight())) {
        game.over(false)
    }
})
```

## 步驟 37 @fullscreen


在 ``||sprites:Sprite||`` 選單中，拖拉 ``||sprites:on sprite of kind player overlaps ...||`` 到主版中。點擊方塊中**最後**的一個 ``||sprites: Player||``，揀選 ``||sprites: Projectile||``。最後將 ``||game: game over LOSE||`` 拖到這個方塊之內。

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Player, SpriteKind.Projectile, function (sprite, otherSprite) {
    game.over(false)
})
``` 