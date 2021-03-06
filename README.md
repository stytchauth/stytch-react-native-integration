# Stytch + React Native example app
![reactNativeExampleApp](https://user-images.githubusercontent.com/100632220/169424762-67caa828-2b05-43f7-9055-067014676316.png)

## Overview
This example app includes a mobile application powered by React Native. This app was created with `npx react-native init`

This application demonstrates a mobile friendly signup and sign in flow powered by Stytch. In this example the following Stytch products are used:
1. [SMS passcodes](https://stytch.com/products/sms-passcodes)
2. [Session management](https://stytch.com/products/session-management)

## Running locally

**Create a Stytch account**

First you will need to sign up and create a new project in [Stytch](https://stytch.com/). Then run the following commands in the terminal of your choice.

**Stytch Dashboard Configuration**

You'll need to take some steps in the [Stytch Dashboard SDK Configuration](https://stytch.com/dashboard/sdk-configuration) in order to enable your project to use the SDK.

1. Enable SDK for your project
2. Add `stytch.rn.test` as a Bundle ID
3. Enable SMS Passcodes (OTP)

**Clone repository**
```bash
git clone https://github.com/stytchauth/stytch-react-native-integration.git
cd stytch-react-native-integration
```

Next we need to create a `.env` file to store our API keys. Modify and run the command below to create a `.env` file. Then update `STYTCH_PUBLIC_TOKEN` with the API key found in your Stytch [project dashboard](https://stytch.com/dashboard/api-keys).
```bash
# in ./stytch-react-native-integration
echo "STYTCH_PUBLIC_TOKEN=GET_FROM_STYTCH_DASHBOARD" > .env
```

**Install Dependencies**
```bash
npm install
cd ios
pod install
cd ..
```

**Start Application**

Note that your development environment must be configured to run react native applications before you can run this demo. For more information, see the [React Native docs](https://reactnative.dev/docs/environment-setup) for environment setup.

```bash
react-native run-ios|android
```

## Documentation
Learn more about the Stytch products used in this example app:
- [SMS OTP API documentation](https://stytch.com/docs/api/sms-otp-overview)
- [React Native SDK](https://stytch.com/docs/sdks/react-native-sdk)
