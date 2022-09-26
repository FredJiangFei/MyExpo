### The Basic

### Environment Setup

### Workflow

    Fast Refresh
    Debugging
        LogBox
            LogBox.ignoreAllLogs() > production
        Chrome Developer Tools
            Debug JS Remotely
        Safari Developer Tools
        React Developer Tools
        Performance Monitor
        Native Debugging

### Testing

    Testing User Interactions
        TextInput > onChangeText
        Button > onPress
    E2E
        Detox
        Appium

### Using Libraries

    Linking Native Code on iOS
        CocoaPods
            npx pod-install
    Linking Native Code on Android
    Finding Libraries
        Does it work with React Native?
        Does it work for the platforms that my app supports?
        Does it work with my app version of React Native?

### Networking

    API Libraries

### Security

    Storing Sensitive Info
        Never store sensitive API keys in your app code.
        Choose the right type of storage
            Async Storage (unsafe)
                Async Storage is the React Native equivalent of Local Storage from the web
                DO USE ASYNC STORAGE WHEN...
                    Persisting non-sensitive data across app runs
                    Persisting Redux state
                    Persisting GraphQL state
                    Storing global app-wide variables
                DON'T USE ASYNC STORAGE FOR...
                    Token storage
                    Secrets
            Secure Storage
                iOS - Keychain Services
                Android - Secure Shared Preferences
                Android - Keystore

    Deep Linking
        不安全，不发送敏感信息
    OAuth2 and Redirects
    Network Security
        SSL encryption
        SSL Pinning

### Image

    my-icon.png / my-icon.ios.png / my-icon.android.png
    check.png / check@2x.png / check@3x.png
    为了使新的图片资源机制正常工作，require 中的图片名字必须是一个静态字符串, 不能使用变量

    Network Images
        use https => IOS App Transport Security
            https://reactnative.dev/docs/publishing-to-app-store#1-enable-app-transport-security
            <Image source={{uri: 'https://reactjs.org/logo-og.png'}} style={{width: 400, height: 400}} />

    Uri Data Images
        仅对非常小的图片使用 base64 数据
        <Image
            style={{
                width: 51,
                height: 51,
                resizeMode: 'contain'
            }}
            source={{
                uri: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAAzCAYAAAA6oTAqAAAAEXRFWHRTb2Z0d2FyZQBwbmdjcnVzaEB1SfMAAABQSURBVGje7dSxCQBACARB+2/ab8BEeQNhFi6WSYzYLYudDQYGBgYGBgYGBgYGBgYGBgZmcvDqYGBgmhivGQYGBgYGBgYGBgYGBgYGBgbmQw+P/eMrC5UTVAAAAABJRU5ErkJggg=='
            }}
            />
    Cache Control (iOS Only)
        cache: 'only-if-cached'

### Handling Touches

    Button
    Touchable
        TouchableOpacity
        TouchableNativeFeedback

### Navigating Between Screens

    React Navigation

### Animations

    Animated
    LayoutAnimation

### Gesture Responder System

    轻按手势
        区分 UI 线程和 JavaScript 线程
    拖拽动效
    1 + 8
        Tap
        Pan
        LongPress
        ....
    通用回调
        无论哪种手势都会有以上回调，只要用户和相关视图发生了交互行为，即便该手势并未真正触发
        onBegin；onTouchesDown；onTouchesMove；onTouchesUp；onFinalize。
    激活回调: 代表某个手势真正被触发了
        onStart；onUpdate；onChange；onEnd。
    系统取消回调
        onTouchesCancelled

    手势回调都返回哪些参数
        常用类回调参数
            state
            numberOfPointers
            x/y、absoluteX/Y 和 changedX/Y 区别
        场景类回调参数
            duration(longPress)
            rotation
            scale(缩放)
            allTouches
    常规手势冲突解决方案
        捕获冒泡机制
