# Props

    id
    initialRouteName
    screenOptions
    backBehavior
        firstRoute
        initialRoute
        order
        history
        none
    defaultStatus
        open or closed
    detachInactiveScreens
    useLegacyImplementation
        是否使用Reanimated 1
    drawerContent
        state
        navigation
        descriptors

# Providing a custom drawerContent​

    DrawerContentScrollView
    DrawerItemList
    DrawerItem
        label
            ({ focused, color }) => <Text style={{ color }}>{focused ? 'Focused text' : 'Unfocused text'}</Text>
        icon
            ({ focused, color, size }) => <Icon color={color} size={size} name={focused ? 'heart' : 'heart-outline'} />
        focused
        onPress
        activeTintColor
        inactiveTintColor
        activeBackgroundColor
        inactiveBackgroundColor
        labelStyle
        style
    Options
        title
        lazy
        drawerLabel
        drawerIcon
        drawerActiveTintColor
        drawerActiveBackgroundColor
        drawerInactiveTintColor
        drawerInactiveBackgroundColor
        drawerItemStyle
        drawerLabelStyle
        drawerContentContainerStyle
        drawerContentStyle
        drawerStyle
        drawerPosition
            left or right
        drawerType
            front / back / slide / permanent
        drawerHideStatusBarOnOpen
        drawerStatusBarAnimation

# Header related options​

    header
    headerShown

# Events

    drawerItemPress

# Helpers

    openDrawer
    closeDrawer
    toggleDrawer
    jumpTo
        navigation.jumpTo('Profile', { owner: 'Satya' });

# Checking if the drawer is open
    import { useDrawerStatus } from '@react-navigation/drawer';
    const isDrawerOpen = useDrawerStatus() === 'open';
