---
description: We take security very seriously.
icon: lock-keyhole
---

# Security

## How we keep your code secure and private

We go to great lengths to ensure your code and other sensitive content is secure and private far beyond that of regular canvas applications.&#x20;

### Encryption Everywhere

{% hint style="success" %}
Your code is encrypted at flight and at rest
{% endhint %}

#### Standard Security

We use TLS and AES to ensure all your data is encrypted in flight and at rest.

#### Enhanced Security

{% hint style="success" %}
Double encryption
{% endhint %}

Your project sensitive contents are encrypt client-side before ever hitting our servers. Each product has a derived encryption key that only users with access to the project can use. When you "open" a project, you're accessing the encryption key for that project.&#x20;

If you want to take the security to another level - add a project password which is used in the encryption key derivation algorithm (Argon2id).

{% hint style="info" %}
Blobs stored on your device are also encrypt
{% endhint %}

Double Encrypted Content:

* Code
* Media e.g. images
* Documentation e.g. PDF and Text Editor content

#### Metadata Enhanced Encryption

Some metadata we consider private to our users. This is data which may contain sensistive information so we also double encrypt before sending to the cloud.

Sensitive Metadata:

* Layer label text
* Labels / text in canvas e.g. text in shapes, section headers
* Comments

{% hint style="warning" %}
Canvas metadata like position and sizes are using the standard security model so that we can provide support when necessary - we **do not** consider this to be sensitive in nature&#x20;
{% endhint %}

## Secrets are Client-Side

{% hint style="success" %}
We do not upload or sync client secrets
{% endhint %}

This includes but is not limited to:

* GitHub authentication tokens
* IDE connection credentials

{% hint style="success" %}
Secrets are stored using your OS key store
{% endhint %}

## Security Notice

{% hint style="info" %}
Some things are visible to our **internal team.** This means we can view in the database without an&#x20;

additional encryption step. This data is still very secure.
{% endhint %}

Standard Security Only:

* Folder / project titles - these exist outside of the canvas security scope
* Bookmark names
* GitHub resources e.g. repository names

{% hint style="success" %}
We will continue to harden all user generated content
{% endhint %}
