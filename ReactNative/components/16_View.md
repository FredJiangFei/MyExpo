# Props

    onStartShouldSetResponder
    onStartShouldSetResponderCapture
    onMoveShouldSetResponder
    onMoveShouldSetResponderCapture
    onResponderGrant
        这个视图开始响应触摸事件。此时需要高亮告诉用户正在响应。
    onResponderMove
        当用户正在屏幕上移动手指时调用这个函数
    onResponderReject
    onResponderRelease
    onResponderTerminate
    onResponderTerminationRequest

    hitSlop
        触摸事件在距离视图多远以内时可以触发

    onLayout
    onMagicTap
        双指轻触(Magic tap)手势，系统会调用此函数
    pointerEvents
        当前视图是否可以作为触控事件的目标
        auto：视图可以作为触控事件的目标。
        none：视图不能作为触控事件的目标。
        box-none：视图自身不能作为触控事件的目标，但其子视图可以。
