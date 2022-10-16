# 本地

    source={require('@expo/snack-static/react-native-logo.png')}

# 网络

    source={{
          uri: 'https://reactnative.dev/img/tiny_logo.png',
        }}

# base64

    source={{
          uri: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAAzCAYAAAA6oTAqAAAAEXRFWHRTb2Z0d2FyZQBwbmdjcnVzaEB1SfMAAABQSURBVGje7dSxCQBACARB+2/ab8BEeQNhFi6WSYzYLYudDQYGBgYGBgYGBgYGBgYGBgZmcvDqYGBgmhivGQYGBgYGBgYGBgYGBgYGBgbmQw+P/eMrC5UTVAAAAABJRU5ErkJggg==',
        }}

# Props

    blurRadius
        模糊滤镜
        在 iOS 上 blurRadius最好不要低于5
    defaultSource
        在读取图片时默认显示的图片
    fadeDuration
        渐入的动画持续时间
    resizeMethod
        当图片实际尺寸和容器样式尺寸不一致时，决定以怎样的策略来调整图片的尺寸
        auto
        resize
        scale
# resizeMode
        'cover', 'contain', 'stretch', 'repeat', 'center'

    onError
    onLayout
    onLoad
    onLoadEnd
    onLoadStart
    onPartialLoadiOS
    onProgress

# getSize
# prefetch()
    预加载
# queryCache()
    查询图片缓存状态
