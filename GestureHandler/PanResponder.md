# InteractionManager
    阻止 JS 事件打断手势活动

# 手势响应系统
    onStartShouldSetResponder 在用户开始触摸的时候
    onMoveShouldSetResponder 在每一个触摸点开始移动时再询问一次：是否愿意响应触摸交互

# 原生事件 nativeEvent
    changedTouches - 上一次事件后，所有移动过的触摸点
    identifier - 触摸点的 ID
    locationX - 触摸点相对于父元素的横坐标
    locationY - 触摸点相对于父元素的纵坐标
    pageX - 触摸点相对于根元素的横坐标
    pageY - 触摸点相对于根元素的纵坐标
    target - 触摸点所在的元素 ID
    timestamp - 触摸事件的时间戳，可用于移动速度的计算
    touches - 当前屏幕上的所有触摸点的集合

# gestureState对象
    stateID - 触摸状态的 ID。在屏幕上有至少一个触摸点的情况下，这个 ID 会一直有效。
    moveX - 最近一次移动时的屏幕横坐标
    moveY - 最近一次移动时的屏幕纵坐标
    x0 - 当响应器产生时的屏幕坐标
    y0 - 当响应器产生时的屏幕坐标
    dx - 从触摸操作开始时的累计横向路程
    dy - 从触摸操作开始时的累计纵向路程
    vx - 当前的横向移动速度
    vy - 当前的纵向移动速度
    numberActiveTouches - 当前在屏幕上的有效触摸点的数量

# 基本用法
    PanResponder.create({
        
      // 要求成为响应者：
      onStartShouldSetPanResponder: (evt, gestureState) => true,
      onStartShouldSetPanResponderCapture: (evt, gestureState) => true,
      onMoveShouldSetPanResponder: (evt, gestureState) => true,
      onMoveShouldSetPanResponderCapture: (evt, gestureState) => true,

# 开始手势操作。给用户一些视觉反馈，让他们知道发生了什么事情！
      onPanResponderGrant: (evt, gestureState) => {},

# 最近一次的移动距离为gestureState.move{X,Y}
      onPanResponderMove: (evt, gestureState) => {},
      onPanResponderTerminationRequest: (evt, gestureState) => true,

# 用户放开了所有的触摸点
      onPanResponderRelease: (evt, gestureState) => { },

# 另一个组件已经成为了新的响应者，所以当前手势将被取消。  
      onPanResponderTerminate: (evt, gestureState) => {  },

      onShouldBlockNativeResponder: (evt, gestureState) => {
        // 返回一个布尔值，决定当前组件是否应该阻止原生组件成为JS响应者
        // 默认返回true。目前暂时只支持android。
        return true;
      },
    });