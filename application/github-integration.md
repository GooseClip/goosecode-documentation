---
icon: github
---

# GitHub Integration

To start working with GitHub in GooseCode you first need to authenticate one or more clients.&#x20;

{% hint style="info" %}
We recommend using fine-grained tokens if you're familiar with them, as they require explicitly provisioning access and can be set with an expiration.  OAuth2 tokens in GitHub grant access beyond what we actually require and as such **do not** follow the `least access principle`.
{% endhint %}

{% hint style="success" %}
We understand code is sensitive - see [security.md](security.md "mention") for more details.
{% endhint %}

## Authenticating

To begin authenticating, navigate to GitHub tab in the [#explorer-pane](canvas.md#explorer-pane "mention") click the :heavy\_plus\_sign: next to clients.

### OAuth2

{% hint style="success" %}
This is the easy option.
{% endhint %}

{% hint style="warning" %}
OAuth2 grants broad access - we recommend fine-grained token.
{% endhint %}

{% stepper %}
{% step %}
### Click "Github OAuth2"
{% endstep %}

{% step %}
### Complete Sign-In
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Organization access may require additional configuration.

Refer: [#organization-access](github-integration.md#organization-access "mention")
{% endhint %}

### Fine-grained Tokens

{% hint style="warning" %}
Authenticating with fine-grained tokens can lead to misconfigurations.
{% endhint %}

{% stepper %}
{% step %}
### Click "Advanced"

You will see an input for your token as well as a warning about how misconfiguration might make parts of the app behave unpredictably.
{% endstep %}

{% step %}
### Click "click here to open token settings in GitHub"

This will open GitHub to the correct page. If you're not already logged in, do so now.
{% endstep %}

{% step %}
### Click "Generate new token"
{% endstep %}

{% step %}
### Name your token

e.g. goosecode-readonly
{% endstep %}

{% step %}
### Select  "Resource Owner"

{% hint style="info" %}
If the resource owner is not your own user it is highly likely you should first follow the organization setup instructions - [#organization-access](github-integration.md#organization-access "mention")
{% endhint %}
{% endstep %}

{% step %}
### Select "Expiration"

We recommend as a best practice to set a 30 day or less expiration while you trial the app.
{% endstep %}

{% step %}
### Configure "Repository Access"

This will control which repositories you will be able to view in GooseCode.
{% endstep %}

{% step %}
### Configure "Permissions"

#### Contents

\[Required] - Read-only

#### Issues

\[Optional]\[Recommended] - Read-only&#x20;

#### Pull Requests

\[Optional]\[Recommended] - Read-only

#### Metadata

\[Required] - Auto-populated by GitHub
{% endstep %}

{% step %}
### Click "Generate Token"

You will be prompted to confirm. Check the details and click "Generate Token" again.
{% endstep %}

{% step %}
### Copy Token

Click the copy button to copy your token to clipboard.

{% hint style="warning" %}
You will not be able to return to this page an copy again so don't miss this step!
{% endhint %}
{% endstep %}

{% step %}
### Return to GooseCode
{% endstep %}

{% step %}
### Paste your token and click "Submit"
{% endstep %}
{% endstepper %}

## Using your GitHub client

Once you've authenticated you should see a client with a green indicator in the `client picker`.

> We've learned that many clients are required for different purposes, especially when working with fine-grained tokens with organization specific scoping.

### Searching for GitHub projects

1. Click the :mag: search icon.
2. Find a repository:
   1. Use the search bar to find from your authenticated repositories.
   2. Manually explore repositories.
   3. Swap to `public` to search for open-source repositories.
3. Click the project you want to use or click :star: to favourite it for later.&#x20;

### Repository Resources

{% hint style="info" %}
Use the breadcrumb at the top to navigate back
{% endhint %}

#### Branches

1. Expand `Branches`.&#x20;
2. Select the branch to view e.g. main
3. Explore a commit:
   1. Click a commit to view a simple diff.
   2. Expand files to view the files _for that commit._
4. Click :star: on files to favourite the files for easy access later.&#x20;

#### Pull Requests

1. Return to the `repository view` by clicking the repository name in the breadcrumb.
2. Expand `Pull Requests` .
3. Select a pull request to view its details.

#### Issues

1. Return to the `repository view` by clicking the repository name in the breadcrumb.
2. Expand `Issues` .
3. Select an open issue to view its details.

{% hint style="info" %}
We currently only show `open` issues.
{% endhint %}

## Favourites

{% hint style="info" %}
Return to the home of the GitHub tab by clicking `home` in the breadcrumb.
{% endhint %}

If you have favourited any GitHub resources you should see them now in the `home` of the GitHub tab.

{% hint style="success" %}
We recommend favouriting `files` to have quick access to files to add to the canvas.
{% endhint %}

## Adding Files to the Canvas!

Adding files is as easy as clicking or dragging a file from the file view into the canvas.

{% hint style="info" %}
You can preview the file first by hovering the file tree and clicking :eye: the eye icon.
{% endhint %}

## Organization Access

### OAuth2

#### Option 1 - Authorize GooseCode via your personal settings

1. Navigate to your personal settings in GitHub (click your avatar in the top right).
2. Select `Applications` in the _Integrations_ section.
3. Click the tab `Authorized OAuth Apps` .
4. Approve GooseCode.

{% hint style="info" %}
GooseCode will not show if you haven't first logged in with GooseCode. If this doesn't work, you may have to log in with the OAuth flow in GooseCode again.
{% endhint %}

#### Option 2 - Remove restrictions for all apps

{% hint style="danger" %}
We do NOT recommend doing this and provide this guide only for situations where you own the organization for personal works and cannot get option 1 to work.
{% endhint %}

1. Navigate to your organization settings in GitHub.
2. Click `OAuth app policy` .
3. Select remove restrictions.



### Fine-grained tokens

{% hint style="warning" %}
You will need an organization admin to perform the following.
{% endhint %}

{% hint style="info" %}
You may not be required to complete this step if you're the organization owner.
{% endhint %}

1. Set up your fine-grained token with the specific organization set for `Resource Owner` - refer [#fine-grained-tokens](github-integration.md#fine-grained-tokens "mention") (step 5).
2. Navigate to your organization settings in GitHub.
3. Expand `Personal access tokens` .
4. Select `Pending requests` .

> Example URL:
>
> https://github.com/organizations/YOUR\_ORGANIZATION/settings/personal-access-token-requests
