### App credentials explained
    iOS
        * Distribution Certificate
            所有app用一个分发证书
            证书过期不会影响到已发布的app，需要发布新app或更新app就需要用到证书
        * Provisioning Profiles
            app-specific
            expire after 12 months

        * Push Notification Keys
            Apple Push Notification Keys(APN keys), send and receive push notifications
            maximum of 2 APN keys

        https://docs.expo.dev/app-signing/app-credentials/
    eas credentials

# local credentials
    credentials.json


# Security
    https://docs.expo.dev/app-signing/security/