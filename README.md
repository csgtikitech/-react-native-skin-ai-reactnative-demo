# React Native Skin AI


A React Native module that allows module allows to capture faces or upload face images from the gallery and analyze data, give advice and treatment of aging problems, facial acne.

🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧

🚧🚧🚧🚧[Help & Input Wanted](https://github.com/csgtikitech/react-native-skin-ai/issues) 🚧🚧🚧🚧

🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧🚧



## React Native Compatibility
To use this library you need to ensure you match up with the correct version of React Native you are using.

p.s. React Native introduced AndroidX support in 0.60, which is a **breaking change** for most libraries (incl. this one) using native Android functionality.

| `@react-native-skin-ai` version           | Required React Native Version                                                     |
| ----------------------------------------- | --------------------------------------------------------------------------------- |
| `1.x.x`                                   | `>= 0.60`                                                                         |


## Getting Started

```
yarn add react-native-skin-ai

# RN >= 0.60
npx pod-install

# RN < 0.60
react-native link react-native-skin-ai
```

You will also need to add `UsageDescription` on iOS and some permissions on Android, refer to the [Install doc](docs/Install.md).

## Usage

```javascript
import SkinAI from 'react-native-skin-ai';

//  For more, read the [API Reference](docs/Reference.md).

/**
 * The first arg is email of user,
 * The second arg is apikey depend on type 
 * The third arg is the server link to post data
 * The last arg is the display language (vi / en)
 */
class App extends React.Component {
  render() {
    return (
      <SkinAI
        email = 'abc@gmail.com',
        apikey = 'apikey',
        linkserver = 'https://shrouded-brushlands-68077.herokuapp.com',
        language = 'en',
        exitPage={() => {}}
      />
    );
  }
}
```
#### Notes

For more, read the [API Reference](docs/Reference.md).


## License

[MIT](LICENSE.md)
