### Flutter

    苹果政策规定只有使用 JavaScriptCore 作为引擎的应用才能动态更新.因此 Flutter 的热更新要先执行 JavaScript，再调用 Java/OC，然后才开始执行 Dart，这样 Flutter 的调用栈就变长、变复杂了。

#### React Native vs Flutter
    相同
        1. 组件化的、（伪）声明式的
        2. 对原生开发都有很高的依赖，只要稍微复杂点，都离不开原生的支持
        3. 高度依赖原生开发，因此它们常常需要使用原生应用或操作系统本身提供的组件或 API
    不同
        1. JavaScript / Dart
        2. 渲染引擎不一样