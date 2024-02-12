# react-native-appchecker

check third party app installation and open app

## Installation

```sh
npm install react-native-appchecker

For ios add in info.plist
	<key>LSApplicationQueriesSchemes</key>
	<array>
		<string>your_app_schema</string>
	</array>

```

## Usage

```js
import AppChecker from 'react-native-appchecker';

// ...


  const checkThirdPartyApp = async (appName) => {
    try {
      const isAppInstalled = await AppChecker.checkThirdPartyApp(appName);
      console.log(`Is ${'appName'} installed? ${isAppInstalled}`);
    } catch (error) {
      console.error('Error checking third-party app:', error);
    }
  };
  const openThirdPartyApp = async (appName) => {
    try {
      const isAppInstalled =  await AppChecker.openThirdPartyApp(appName);
      
    } catch (error) {
      console.error('Error checking third-party app:', error);
    }
  };
```

## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT
