# ScrollView 必须有一个确定的高度才能正常工作

ScrollView 会简单粗暴地把所有子元素一次性全部渲染出来
FlatList 会惰性渲染子元素，只在它们将要出现在屏幕中时开始渲染。

# Props
