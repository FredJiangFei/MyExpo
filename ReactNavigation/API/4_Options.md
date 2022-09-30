# Screen > options

    options={{ title: 'Awesome app' }}
    options={({ navigation, route }) => ({
        title: 'Awesome app',
        headerLeft: () => (
            <DrawerButton onPress={() => navigation.toggleDrawer()} />
        ),
    })}

# Group > screenOptions

    screenOptions={{ headerStyle: { backgroundColor: 'papayawhip' } }}
    screenOptions={({ navigation, route }) => ({ })}

# navigator > screenOptions

# navigation.setOptions
