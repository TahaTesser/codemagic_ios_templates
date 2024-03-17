# codemagic_ios_template

This repository is a starting point to setup `codemagic.yaml` configuration to build and publish a native iOS app on Codemagic.

## Getting Started

1.  Clone this repository or copy the [codemagic.yaml](./codemagic.yaml) file and add it to your existing native iOS project.

2. Follow the instructions in the [Codemagic documentation for iOS native apps](https://docs.codemagic.io/yaml-quick-start/building-a-native-ios-app/) to create a signing certificate and provisioning profile for your app.

4.  Update the [codemagic.yaml](./codemagic.yaml) file with your desired configuration.
Replace the `BUNDLE_ID` with your app's bundle identifier.
```yaml
    environment:
      ios_signing:
        distribution_type: app_store
        bundle_identifier: BUNDLE_ID # Replace with your app's bundle identifier
      vars:
        BUNDLE_ID: "BUNDLE_ID" # Replace with your app's bundle identifier
```

Replace the `XCODE_WORKSPACE` and `XCODE_SCHEME` with your xcode workspace and scheme.
```yaml
        XCODE_WORKSPACE: "xxx.xcworkspace" # Replace with your xcode workspace
        XCODE_SCHEME: "xxx" # Replace with your xcode scheme
```

Replace the `0000000000` with your app store apple id.
```yaml
        APP_STORE_APPLE_ID: 0000000000 # Replace with your app store apple id
```

5. If you've set up your signing certificate and provisioning profile, you can now build your app on Codemagic and publish to Test Flight. ✨
