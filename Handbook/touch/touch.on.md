### 模拟手指接触屏幕 \(**touch\.on**\)


#### 声明
```lua
触摸事件 = touch.on(横坐标, 纵坐标)
```


#### 参数及返回值
- 横坐标, 纵坐标
    - 整数型，需要接触的点于当前旋转坐标系的坐标
- 触摸事件
    - 触摸事件对象，通过调用 [`touch.on`](/Handbook/touch/touch.on.md) 函数可以并获得一个用于操控当前触摸的事件对象


#### 说明
> 模拟手指接触屏幕指定位置，并返回一个用于操纵本次触摸过程的触摸事件对象  
> **注:** 该函数会占用一个手指 id，手指 id 的数量是有限的 (大约 30 个) ，超出限制再调用 [touch.on](/Handbook/touch/touch.on.md) 或 [touch.tap](/Handbook/touch/touch.tap.md) 会抛出 `finger pool overflow` 错误，注意不要**同时占用**过多手指 id，及时调用 :off 方法释放手指  


#### 示例  
```lua
touch.on(100, 100):move(200,200):off() -- 模拟一个手指于点 100, 100 的位置接触屏幕，然后匀速滑动到点 200, 200 的位置，然后松开
```

