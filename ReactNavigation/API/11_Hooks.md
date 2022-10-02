# useNavigation

# useRoute

# useNavigationState

    const index = useNavigationState(state => state.index);
    const state = useNavigationState(state => state);
    navigation.getState() / useNavigationState

# useFocusEffect

    useFocusEffect(
        React.useCallback(() => {
        const unsubscribe = API.subscribe(userId, user => setUser(user));

        return () => unsubscribe();
        }, [userId])
    );
    useCallback
    Running asynchronous effects
    blur
        don't do the following:
        useFocusEffect(
            React.useCallback(() => {
                return () => {
                // Do something that should run on blur
                }
            }, [])
        );

        use listen to the blur event
        React.useEffect(() => {
            const unsubscribe = navigation.addListener('blur', () => {
            // Do something when the screen blurs
        });

        return unsubscribe;
        }, [navigation]);

# useIsFocused

    const isFocused = useIsFocused();

# useLinkTo / useLinkProps / useLinkBuilder

    navigate to a screen / using a path / instead of a screen name

# useScrollToTop

# useTheme

    const { colors } = useTheme();
