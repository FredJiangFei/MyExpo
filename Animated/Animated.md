# value
    Animated.Value()
    Animated.ValueXY()
# Configuring animations 三种动画类型
    Animated.decay()
    Animated.spring()
    Animated.timing()

# use animated
    Animated.timing({}).start(({ finished }) => {
        /* completion callback */
    });

# Using the native driver
    1. Computation = JS thread; Animations by Native OS
        a. compute
        b. serialize
        c. transfer it over the bridge to host OS
        d. deserialize
        e run the frame
    2. Everything by Native OS (useNativeDriver: true)
        a. serialize whole animation
        b. Native OS deserialize
        c. WIN

    different
        a. no more bridge transfer
        b. JS thread is free
        c. smoother animations

    原生代码在 UI 线程上执行动画，不会因JS 线程阻塞影响动画执行

# 组合动画
    Animated.delay() 延迟
    Animated.parallel() 同时启动
    Animated.sequence() 按顺序启动
    Animated.stagger() 按照给定的延时间隔

# 自定义动画组件
    组件必须经过特殊处理才能用于动画
        1. 把动画值绑定到属性上
        2. 避免 react 重新渲染和重新调和的开销
        3. 在组件卸载时做一些清理工作
    createAnimatedComponent() 方法正是用来处理组件，使其可以用于动画

    内置动画组件
        Animated.Image
        Animated.ScrollView
        Animated.Text
        Animated.View
        Animated.FlatList
        Animated.SectionList

# 合成动画值

# 插值
    interpolate()
   
    Example: 使用 Animated.Value 的值从 0 变化到 1 来让 position 从 150px 变化到 0px
      style={{
        opacity: this.state.fadeAnim, // Binds directly
        transform: [{
            translateY: this.state.fadeAnim.interpolate({
                inputRange: [0, 1],
                outputRange: [150, 0]  // 0 : 150, 0.5 : 75, 1 : 0
            }),
        }],
    }}

# 处理手势和其他事件
    Animated.event()