### The Basic

### Environment Setup

### Workflow

    Fast Refresh
    Debugging
        LogBox
            LogBox.ignoreAllLogs() > production
        Chrome Developer Tools
            Debug JS Remotely
        Safari Developer Tools
        React Developer Tools
        Performance Monitor
        Native Debugging

### Testing

    Testing User Interactions
        TextInput > onChangeText
        Button > onPress
    E2E
        Detox
        Appium

### Using Libraries

    Linking Native Code on iOS
        CocoaPods
            npx pod-install
    Linking Native Code on Android
    Finding Libraries
        Does it work with React Native?
        Does it work for the platforms that my app supports?
        Does it work with my app version of React Native?

### Networking

    API Libraries

### Security

    Storing Sensitive Info
        Never store sensitive API keys in your app code.
        Choose the right type of storage
            Async Storage
                Async Storage is the React Native equivalent of Local Storage from the web
                DO USE ASYNC STORAGE WHEN...
                    Persisting non-sensitive data across app runs
                    Persisting Redux state
                    Persisting GraphQL state
                    Storing global app-wide variables
                DON'T USE ASYNC STORAGE FOR...
                    Token storage
                    Secrets
            Secure Storage
                iOS - Keychain Services
                Android - Secure Shared Preferences
                Android - Keystore

    Authentication and Deep Linking
        
    OAuth2 and Redirects
