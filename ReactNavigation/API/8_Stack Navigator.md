# Props

    id
    initialRouteName
    screenOptions
    detachInactiveScreens
        inactive screen是否被清除
    keyboardHandlingEnabled
        跳到一个新页面，键盘自动dismiss

# Options

    Stack.navigator > screenOptions
    Stack.Screen > options

    title
    presentation

    card
        cardShadowEnabled
        cardOverlayEnabled
        cardOverlay
        cardStyle

# Header related options

    header > use custom header
        * navigation
        * route
        * options
        * layout
        * progress
        * back
        * styleInterpolator
        -- Specify a height in headerStyle to avoid glitches​
        -- Set headerMode to float for custom header animations​
    headerMode
    headerShown

    headerBack
        headerBackAllowFontScaling
        headerBackAccessibilityLabel
        headerBackImage
        headerBackTitle
        headerBackTitleVisible
        headerTruncatedBackTitle
        headerBackTitleStyle

# Events

    transitionStart
    transitionEnd
    gestureStart
    gestureEnd
    gestureCancel

# Helpers

    push
        navigation.push('Profile', { owner: 'Michaś' });
    pop
        navigation.pop();
    popToTop
        navigation.popToTop();

# Animations
