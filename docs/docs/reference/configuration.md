# Advanced Configurations

## Custom Callback URL

:::info
When specifying the callback URL to the Provider, please copy/paste it exactly. Any difference (e.g. a trailing `/`) could cause the Provider to reject the OAuth requests.
:::

By default, Nango Cloud uses the following callback URL: `https://api.nango.dev/oauth/callback`.

Because most OAuth providers show the callback URL on the Authorization page to the user, you may want to use a callback URL hosted on your own domain. For instance: `https://my-awesome-app.com/oauth-callback`.

Nango Cloud lets you customize the callback URL on your [Dashboard's project settings](https://app.nango.dev/project-settings).

When using a custom callback URL you should redirect any request made to your callback URL to `https://api.nango.dev/oauth/callback` AND pass along all parameters exactly as you received them. The simplest way to do this is to use a 308 redirect.

:::caution
Before changing the callback URL in Nango:

1. You should make sure that your redirect works
2. That your OAuth app, as registered with the provider, has the new callback URL whitelisted.

Otherwise the OAuth requests will fail or get rejected by the provider.
:::

Nango Self-Hosted also supports [custom callback URLs](nango-deploy/oss-instructions.md#custom-urls).

## Configuration API (programmatic integrations configuration)

If you need a way to programmatically create integrations in your Nango instance please reach out to us on the [Slack community](https://www.nango.dev/slack). A Configuration API is available, but we would love to hear more about your use case first.

## Something not working as expected? Need help?

If you run into any trouble with Nango or have any questions please do not hesitate to contact us - we are happy to help!

Please join our [Slack community](https://nango.dev/slack), where we are very active, and we will do our best to help you fast.
