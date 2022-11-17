
### EAS Build 打包项目

### Creating your first build
    1. Install the latest EAS CLI
        npm install -g eas-cli

    2. Log in to your Expo account
        eas login

    3. Configure the project
        eas build:configure

    4. Run a build
        eas build --platform android
        eas build --platform ios
        eas build --platform all
### Apple Developer Program for build / $99 USD
### Google Play Store / $25 USD

    5. Wait for the build to complete
        eas build:list
        
    6. Deploy the build

### EAS Build Limitations
    12GB RAM memory and CPU limits
    limit 2 hours to run
    SDK 41 以下不支持
    .......

### Configuring EAS Build with eas.json
    Build profiles
        development, preview, and production
        eas build --profile <profile-name>(default production)
    Platform-specific and common options

    Sharing configuration between profiles
        "extends": "production"

    Development builds 开发测试用(包含developer tool)
        {
            "build": {
                "development": {
                "developmentClient": true,
                "distribution": "internal",
                "ios": {
                    "simulator": true
                }
                }
                // ...
            }
            // ...
        }
    Preview builds 团队测试用
        {
            "build": {
                "preview": {
                "distribution": "internal"
                }
                // ...
            }
            // ...
        }
    Production builds 发布到store


### Configuring your build tools
    Selecting build tool versions
        {
            "build": {
                "production": {
                "node": "16.13.0"
                }
                // ...
            }
            // ...
        }

        {
            "build": {
                "production": {
                    "node": "16.13.0"
                },
                "preview": {
                    "extends": "production",
                    "distribution": "internal"
                },
                "development": {
                    "extends": "production",
                    "developmentClient": "true",
                    "distribution": "internal"
                }
                // ...
            }
            // ...
        }

### Environment variables
    {
        "build": {
            "production": {
                "node": "16.13.0",
                "env": {
                    "API_URL": "https://company.com/api"
                }
            },
            "preview": {
                "extends": "production",
                "distribution": "internal",
                "env": {
                    "API_URL": "https://staging.company.com/api"
                }
            }
            // ...
        }
        // ...
    }
    https://docs.expo.dev/build-reference/variables/


### Internal distribution
    Setting up internal distribution
        https://docs.expo.dev/build/internal-distribution/#setting-up-internal-distribution
        1. Configure a build profile / eas.json
            Android
            IOS 
                available for all paid Apple Developer accounts. not available for free accounts
        2. Configure app signing
        3. Run a build with the internal build profile
        4. Installing and running the build
        5. Automation on CI (optional)

### Automating submissions
    eas build --auto-submit
    Selecting a submission profile
        --auto-submit 默认选择与build profile name相同的submission profile
        --auto-submit-with-profile=<profile-name>
    Build profile environment variables and submissions
        // eas.json
        {
            "build": {
                "production": {
                "env": {
                    "APP_ENV": "production"
                }
                },
                "development": {
                "env": {
                    "APP_ENV": "development"
                }
                }
            }
        }

        // app.config.js
        export default () => {
            return {
                name: process.env.APP_ENV === 'production' ? 'My App' : 'My App (DEV)',
                ios: {
                bundleIdentifier: process.env.APP_ENV === 'production' ? 'com.my.app' : 'com.my.app-dev'
                }
                // ... other config here
            }
        }

### Using EAS Update
    Channel
        {
            "build": {
                "production": {
                    "channel": "production"
                },
                "preview": {
                    "channel": "staging",
                    "distribution": "internal"
                }
            }
        }
    Binary compatibility and runtime versions
        {
            "expo": {
                "runtimeVersion": "2.718"
            }
        }
        Any time you change the native runtime (in managed apps, this happens when you add or remove a native library, or modify app.json), you should increment the runtime version.
        
### Triggering builds from CI