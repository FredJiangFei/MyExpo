# useSharedValue 值
    const offset = useSharedValue(0);

# useAnimatedStyle 根据值修改的样式
    const animatedStyles = useAnimatedStyle(() => {
        return {
            transform: [{ translateX: offset.value * 255 }],
        };
    });

# withTiming / withSpring 一定时间段，到达样式变化
    offset.value = withSpring(Math.random());

# cancelAnimation

# withDelay, withSequence and withRepeat