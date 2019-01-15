# Auth0-Chrome Extension
<img src="https://img.shields.io/badge/community-driven-brightgreen.svg"/> <br>

This sample demonstrates how to add authentication to a Chrome extension with Auth0. It uses Auth0's hosted Lock widget with Chrome's `launchWebAuthFlow`.

For detailed instructions on integrating Auth0 in a Chrome extension, see the [full documentation](https://auth0.com/docs/quickstart/native/chrome).

This repo is supported and maintained by Community Developers, not Auth0. For more information about different support levels check https://auth0.com/docs/support/matrix .

## Getting started

Chrome extensions are packaged as `.crx` files for distribution but may be loaded "unpacked" for development. For more information on how to load an unpacked extension, see the [Chrome extension docs](https://developer.chrome.com/extensions/getstarted#unpacked).

### Installation

#### Sign up for Auth0 account

If you haven't already done so, [sign up](https://auth0.com/signup) for your free Auth0 account and create an application in the dashboard. Find the **domain** and **client ID** from your app settings, as these will be required to integrate Auth0 in your Chrome extension.

When loading your application as an unpacked extension, a unique ID will be generated for it. You must whitelist your callback URL (the URL that Auth0 will return to once authentication is complete) and the allowed origin URL.

In the **Allowed Callback URLs** section, whitelist your callback URL.

```bash
https://<YOUR_APP_ID>.chromiumapp.org/auth0
```

In the **Allowed Origins** section, whitelist your chrome extension as an origin.

```bash
chrome-extension://<YOUR_APP_ID>
```

#### Add your Application Keys

Rename `env.js.example` to `env.js` and provide your Auth0 credentials.

```js
window.env = {
AUTH0_DOMAIN: 'YOUR_AUTH0_DOMAIN',
AUTH0_CLIENT_ID: 'YOUR_AUTH0_CLIENT_ID',
};
```


#### Install the Dependencies

Install the dependencies with npm by running:

```bash
npm install
```

#### Load the Unpacked Extension

For testing purposes, Chrome allows you to load unpacked extensions from anywhere on your computer. Navigate to `chrome://extensions` in the URL bar and load the project as an unpacked extension.

## License

This project is licensed under the MIT license. See the [LICENSE](https://github.com/auth0-community/auth0-chrome-sample/blob/master/LICENSE) file for more info.
