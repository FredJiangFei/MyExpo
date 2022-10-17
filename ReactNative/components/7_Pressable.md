# 原理

    onPressIn 在按压时被调用
    onPressOut 在按压动作结束后被调用

    在按下 onPressIn 后，将会出现如下两种情况的一种
        1. 用户移开手指，onPressOut > onPress
        2. 按压持续 500 毫秒以上，onLongPress > onPressOut

    HitRect
        相对于包裹元素的有效触发距离。在 HitRect 内的任何地方都可以触发按压动作。

# Props


    disabled
        禁用按压行为
# hitSlop
        元素能够检测到按压动作的额外距离
    onPress
        onPressOut 之后调用
# onPressIn
        在 onPressOut 和 onPress 之前
# onPressOut
        松开手后调用
    onLongPress
        onPressIn 持续超过 500 毫秒后调用
# delayLongPress
        从 onPressIn 触发到 onLongPress 的间隔（毫秒）
        default: 500
# pressRetentionOffset
        onPressOut 额外的有效触控距离


# style
        style={({ pressed }) => [ baseStyle, { opacity: pressed ? 0.5 : 1} ]}