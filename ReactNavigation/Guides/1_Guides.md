# Authentication

    SecureStore
    navigationKey

# Supporting safe areas

    SafeAreaView
    react-native-safe-area-context
    Landscape Mode
    edges
    useSafeAreaInsets

# Hiding tab bar in specific screens

    Stack.Navigator
        HomeStack(Tab.Navigator)
            Home (Screen)
            Feed (Screen)
            Notifications (Screen)
        Profile (Screen)
        Settings (Screen)

# Different status bar configuration based on route

    Stack
        <StatusBar barStyle="light-content" backgroundColor="#6a51ae" />
        <StatusBar barStyle="dark-content" backgroundColor="#ecf0f1" />
    Tabs and Drawer
        FocusAwareStatusBar

# Opening a modal

    screenOptions={{ presentation: 'modal' }}

# Multiple drawers

# Screen options with nested navigators

    Stack.Navigator
        Home (Tab.Navigator)
            Feed (Screen)
            Profile (Screen)
            Account (Screen)
        Settings (Screen)

    ***************getFocusedRouteNameFromRoute***********************
    navigation.setOptions

# Custom Android back button behavior

# Preventing going back

    beforeRemove event

# Call a function when focused screen changes

    focus event
    useFocusEffect
    useIsFocused

# Access the navigation prop from any component

    非screen的component接收不到navigation
    useNavigation

# Navigating without the navigation prop

    Redux navigation

# Deep linking

# Configuring links

# Server rendering

# Screen tracking for analytics

    onReady
    onStateChange

# Themes

    Built-in themes

# State persistence

    initialState
    onStateChange
    Development Mode
        __DEV__
