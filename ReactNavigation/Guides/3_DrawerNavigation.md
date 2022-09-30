# Drawer navigation

    @react-navigation/drawer

# Opening and closing drawer

    navigation.openDrawer();
    navigation.closeDrawer();
    navigation.toggleDrawer();

    navigation.dispatch(DrawerActions.openDrawer());
    navigation.dispatch(DrawerActions.closeDrawer());
    navigation.dispatch(DrawerActions.toggleDrawer());

    const isDrawerOpen = useDrawerStatus() === 'open';
