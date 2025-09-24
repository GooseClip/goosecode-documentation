---
description: Convenience tools for every day developer tasks.
icon: toolbox
---

# Toolbox

## RGB

The `RGB` tool is to provide quick access to colors.

### Images

{% stepper %}
{% step %}
### Add an image

Either drag an image onto the pane, or click to select using the file explorer.&#x20;
{% endstep %}

{% step %}
### Grab a color

Select a color from the generated sample palette below the image or use the eye-dropper button to select a color from the image manually.&#x20;
{% endstep %}

{% step %}
### Pan / Zoom

Move around the image using pan and zoom to focus on the section relevant to your work.
{% endstep %}
{% endstepper %}

### Color Picker

Use the color picker to view a color you already have the hex for, or select a new color using either the HSL sliders, or from one of our presets.

{% hint style="info" %}
Hex input expects Alpha | Red | Green | Blue without a 0x prefix&#x20;
{% endhint %}

## 0B01

The `0B01` tool helps you convert between hex, decimals, binary and their text equivalent. The tool also helps quickly resolve epoch timestamps into a human readable format in both UTC and Local.

{% hint style="info" %}
To force the input to be interpreted in a as `hex` prefix it with `0x`. For `binary` use `0b`.
{% endhint %}

> The ambition with this tool is to not assume the format of the input but this leads to a number of edge cases so explicitly forcing the input is often required.

## Hash / B64

The `Hash / B64` tool helps us with all things related to encoded things.&#x20;

{% hint style="info" %}
Supports file input.
{% endhint %}

### Hash

Generate cryptographic hashes of your input string or file.

Generates:

* MD5
* SHA1
* SHA256
* SHA512
* SHA224
* SHA384
* SHA512-224
* SHA512-256

{% hint style="success" %}
Great for checking the SHA256 hash of a program downloaded from the internet.
{% endhint %}

{% hint style="success" %}
Verify your uploads to blob storage using MD5 e.g. Google Cloud Storage.
{% endhint %}

### Base64

Generate both encoded and decoded versions of your string without needs to know if it's already encoded or not.

{% hint style="info" %}
Supports file input.
{% endhint %}

### URL

Generate both encoded and decoded version of your URL without needing to know if it's already encoded or not.

### JWT

Paste your JWT to view its structure.

{% hint style="success" %}
The JWT never leaves your machine.
{% endhint %}

{% hint style="danger" %}
We do not verify the signature of the JWT - use for debugging purposes only.
{% endhint %}

## Encrypt

Encrypt and decrypt sensitive content.

{% hint style="info" %}
Supports file input.
{% endhint %}

{% hint style="warning" %}
To visualize in the UI we use some form of string encoding - this may lead to some confusion at first.
{% endhint %}

{% hint style="danger" %}
Do your own research - this is not intended as a bulletproof tool for production.

* Secrets, nonce and mac should be shared via a different medium than the encrypted content.
* Macs should always be checked.
{% endhint %}

{% hint style="success" %}
Good for sharing .env files securely if done right.
{% endhint %}

### Recommended use:

{% stepper %}
{% step %}
### Encrypt something
{% endstep %}

{% step %}
### Send share the encrypted content via 1 communication medium

e.g. Slack / Teams
{% endstep %}

{% step %}
### Share the decryption details via another secure communication medium

e.g. Signal / Telegram / SSH
{% endstep %}

{% step %}
### Decrypt using GooseCode

For the easiest use, request the receiver download GooseCode and paste the necessary decryption elements.&#x20;
{% endstep %}
{% endstepper %}

#### AES-256-GCM

This is the widely regarded as the better algorithm of the two.

> Unfortunately openssl doesn't support.

#### AES-256-CBC

CBC is widely adopted and therefore we can provide you with a decryption command using `openssl`.

{% hint style="danger" %}
The generated openssl command contains the secret, hash and nonce so do not share it on the same medium as the encrypted content.
{% endhint %}

{% hint style="warning" %}
The mac is generated only on the ciphertext - i.e. not including the nonce.
{% endhint %}

## DIFF

The `DIFF` tool helps identify subtle differences in two texts. We provide a view visualization modes, some are better suited to certain types of content. Play around with them to see what suits your best.

## Generator

&#x20;The `generator` tool can be used to generate commonly required development inputs.

### UUID

Select from one of 3 UUID generators to generate an ID.

#### UUIDv4 - random

This is the most popular UUID, a random UUID.

#### UUIDv5 - namespaced

Recreate a known UUID from namespace.&#x20;

UUIDv7 - timestamp

Recreate a known UUID from a timestamp.

### Secret

Generate a crypographically secure secret.

#### Random

Random secret with a fixed length.

#### SHA128 & SHA256

Generate a random secret then hash.

{% hint style="info" %}
Useful for creating secrets used for AES128 and AES256 e.g. creating a known password for [#encrypt](toolbox.md#encrypt "mention") &#x20;
{% endhint %}

### Placeholder

Generate latin text similar to lorem ipsum and fixed size images to use as placeholders in your UI.

### PKI

Public key infrastructure utilities for common development tasks - e.g. self signed certificates for local servers.
