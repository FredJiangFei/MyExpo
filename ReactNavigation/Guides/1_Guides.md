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
