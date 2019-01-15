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

## Contribute

Feel like contributing to this repo? We're glad to hear that! Before you start contributing please visit our [Contributing Guideline](https://github.com/auth0-community/getting-started/blob/master/CONTRIBUTION.md).

Here you can also find the [PR template](https://github.com/auth0-community/auth0-chrome-sample/blob/master/PULL_REQUEST_TEMPLATE.md) to fill once creating a PR. It will automatically appear once you open a pull request.

## Issues Reporting

Spotted a bug or any other kind of issue? We're just humans and we're always waiting for constructive feedback! Check our section on how to [report issues](https://github.com/auth0-community/getting-started/blob/master/CONTRIBUTION.md#issues)!

Here you can also find the [Issue template](https://github.com/auth0-community/auth0-chrome-sample/blob/master/ISSUE_TEMPLATE.md) to fill once opening a new issue. It will automatically appear once you create an issue.

## Repo Community

Feel like PRs and issues are not enough? Want to dive into further discussion about the tool? We created topics for each Auth0 Community repo so that you can join discussion on stack available on our repos. Here it is for this one: [auth0-chrome](https://community.auth0.com/t/auth0-community-oss-auth0-chrome-sample/15979)

<a href="https://community.auth0.com/">
<img src="/Assets/join_auth0_community_badge.png"/>
</a>

## License

This project is licensed under the MIT license. See the [LICENSE](https://github.com/auth0-community/auth0-chrome-sample/blob/master/LICENSE) file for more info.

## What is Auth0?

Auth0 helps you to:

* Add authentication with [multiple authentication sources](https://docs.auth0.com/identityproviders), either social like
* Google
* Facebook
* Microsoft
* Linkedin
* GitHub
* Twitter
* Box
* Salesforce
* etc.

**or** enterprise identity systems like:
* Windows Azure AD
* Google Apps
* Active Directory
* ADFS
* Any SAML Identity Provider

* Add authentication through more traditional [username/password databases](https://docs.auth0.com/mysql-connection-tutorial)
* Add support for [linking different user accounts](https://docs.auth0.com/link-accounts) with the same user
* Support for generating signed [JSON Web Tokens](https://docs.auth0.com/jwt) to call your APIs and create user identity flow securely
* Analytics of how, when and where users are logging in
* Pull data from other sources and add it to user profile, through [JavaScript rules](https://docs.auth0.com/rules)

## Create a free Auth0 account

* Go to [Auth0 website](https://auth0.com/signup)
* Hit the **SIGN UP** button in the upper-right corner
