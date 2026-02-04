---
icon: circle-question
---

# Troubleshooting

## Bugs, feature requests, documentation

If you've found a bu, please report it via the issues repo in GitHub.

&#x20;<a href="https://github.com/GooseClip/goosecode-issues" class="button primary">Report an issue or suggest a change </a>

***

## Known Issues

### Linking Anonymous Account

After linking anonymous account with Apple, Google or GitHub you may not be able to create or open projects due to a token invalidation issue.

{% hint style="info" %}
Observed 2.0.4
{% endhint %}

{% hint style="success" %}
Workaround -> Log out and log in again
{% endhint %}

## IDE

### Connection Issues

{% hint style="warning" %}
Connection is currently only possible with IPv4.
{% endhint %}

{% hint style="info" %}
Check that the GooseCode server is started or enable `Start Automatically` in the extension settings.
{% endhint %}

{% hint style="info" %}
Check for port conflicts. You can change your port using in the extension settings.
{% endhint %}

{% hint style="info" %}
If you're connecting across devices, ensure `localhost only` is disabled. Refer [#cross-device-connection](../ide-integration-alpha.md#cross-device-connection "mention")
{% endhint %}

### Resetting Access

You can reset the access to your IDE by running the command:

`GooseCode: Purge Certificates and Regenerate Password` in the command palette.

### Code Source Not Showing

Try toggling the code source off and on in the GooseCode IDE pane.



***

## GitHub Setup

Please refer to [github-integration.md](../github-integration.md "mention").
