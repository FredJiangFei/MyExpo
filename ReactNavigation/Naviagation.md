# Installation

    npm install @react-navigation/native
    npx expo install react-native-screens react-native-safe-area-context

# wrap NavigationContainer

# stack navigator

    npm install @react-navigation/native-stack
    const Stack = createNativeStackNavigator();

# Moving between screens

    navigation.navigate('Details')
    navigation.push('Details')
    navigation.goBack()
    navigation.popToTop()
        goes back to the first screen in the stack

# Passing parameters

    navigation.navigate('Details', {
        itemId: 86,
        otherParam: 'anything you want here',
    });

    const { itemId, otherParam } = route.params;

# Updating params

    navigation.setParams({
        query: 'someText',
    });

# Initial params

    <Stack.Screen
        name="Details"
        component={DetailsScreen}
        initialParams={{ itemId: 42 }}
    />

# Passing params to a previous screen

    navigation.navigate({
        name: 'Home',
        params: { post: postText },
        merge: true,
    });
    merge ???????????????????????????????

# Passing params to nested navigators ??????????????????????????????????

    navigation.navigate('Account', {
        screen: 'Settings',
        params: { user: 'jane' },
    });

# Configuring the header bar

    # Setting the header title
        options={{ title: 'My home' }}

    # Using params in the title
        options={({ route }) => ({ title: route.params.name })}

    # setOptions
        <Button
            title="Update the title"
            onPress={() => navigation.setOptions({ title: 'Updated!' })}
        />

    # Adjusting header styles
        headerStyle
        headerTintColor
            back button and title color
        headerTitleStyle

        title: 'My home',
        headerStyle: {
            backgroundColor: '#f4511e',
        },
        headerTintColor: '#fff',
        headerTitleStyle: {
            fontWeight: 'bold',
        }

    # Sharing common options across screens
        screenOptions

    # Replacing the title with a custom component
        options={{ headerTitle: (props) => <LogoTitle {...props} /> }}

# Header buttons

    # Adding a button to the header
        headerRight: () => (
            <Button
              onPress={() => alert('This is a button!')}
              title="Info"
              color="#fff"
            />
        ),
    # Header interaction with its screen component
        React.useLayoutEffect(() => {
            navigation.setOptions({
                headerRight: () => (
                    <Button onPress={() => setCount((c) => c + 1)} title="Update count" />
                ),
            });
        }, [navigation]);
    ######## Customizing the back button #####################
        headerBackTitle
        headerBackTitleStyle
        headerBackImageSource

# Nesting navigators (important)

    Stack.Navigator
        Home (Tab.Navigator)
            Feed (Screen)
            Messages (Screen)
        Profile (Screen)
        Settings (Screen)

    behaviour
        own navigation history
        own options
        own params
        navigation handled bubble up
        drawer > stack (openDrawer, closeDrawer, toggleDrawer)
        stack > drawer (navigation.dispatch(DrawerActions.toggleDrawer());)
        tab > stack (won't receive tab events)

# Navigating to a screen in a nested navigator

    Stack.Navigator
        Root(Drawer.Navigator)
            Home (Screen)
            Profile (Screen)
            Settings (Screen)
        Feed (Screen)

    Feed > Root
        navigation.navigate('Root'); ====> show Home

    Feed > Profile
        navigation.navigate('Root', { screen: 'Profile' });

# Passing params to a screen in a nested navigator

    navigation.navigate('Root', {
        screen: 'Profile',
        params: { user: 'jane' },
    });

# Nesting multiple navigators

     Stack.Navigator
        Home(Tab.Navigator)
            Profile (Screen)
            Settings (Screen)
        EditPost (Screen)

# Best practices when nesting

    reduce nesting navigators to minimal
    Stack.Group

# Navigation lifecycle

    React Navigation lifecycle events
        focus
            useFocusEffect
            const isFocused = useIsFocused();
        blur

# Glossary of terms

    Navigator
        <Stack.Navigator> // <---- This is a Navigator
            xxxxxxx
        </Stack.Navigator>
    Router
        how to handle actions and state changes in the navigator
        custom navigator
    Screen component
         <Stack.Screen
            name="Home"
            component={HomeScreen} // <---- Screen component
        />
    Navigation Prop
        dispatch 
        navigate
        goBack
    Route Prop
        params, key and name
    Navigation State (important)
    Route
    Header
# Troubleshooting

