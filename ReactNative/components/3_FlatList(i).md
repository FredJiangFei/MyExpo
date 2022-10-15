# Props

    renderItem
        renderItem({ item, index, separators })
        onShowUnderlay ?
        onHideUnderlay ?
    data
# extraData
    keyExtractor
    ItemSeparatorComponent
    onRefresh
        下拉刷新
    refreshing
        加载新数据时， 显示一个正在加载的符号

# horizontal
        水平布局
# numColumns ?
        horizontal必须是false
    columnWrapperStyle ?
        当numColumns>1时，作用在每行容器上的样式

# ListEmptyComponent
# ListFooterComponent
    ListFooterComponentStyle
# ListHeaderComponent
    ListHeaderComponentStyle

    initialNumToRender
        一开始渲染的元素数量
    initialScrollIndex
    getItemLayout
        优化，只加载范围内的元素

# onEndReached
# onEndReachedThreshold
    当距离底部多远时触发onEndReached

    inverted

# Methods

    flashScrollIndicators()
    getNativeScrollRef()
    getScrollResponder()
    getScrollableNode()
    recordInteraction()
# scrollToEnd()
        滚动到底部
# scrollToIndex()
    scrollToItem()
    scrollToOffset()
