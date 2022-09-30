# Tab navigation

    npm install @react-navigation/bottom-tabs

# Customizing the appearance

    tabBarIcon
        focused, color, size
    tabBarActiveTintColor
    tabBarInactiveTintColor

# Add badges to icons

    tabBarBadge: 3

# Jumping between tabs

    navigation.navigate

# A stack navigator for each tab

    Tab.Navigator
        HomeStack(Stack.Navigator)
            Home (Screen)
                navigation.navigate('Details')
            Details (Screen)
        SettingsStack(Stack.Navigator)
            Settings (Screen)
                navigation.navigate('Details')
            Details (Screen)
