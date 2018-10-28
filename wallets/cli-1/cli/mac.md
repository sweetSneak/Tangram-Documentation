---
description: Tangram CLi Wallet installation for macOS
---

# Mac & Linux

## Step 1: Installation Prerequisites

Before you can install the Tangram CLi Wallet on macOS, you will need to install a few prerequisites. Fortunately this process is pretty straightforward.

### Install Git for macOS

The first prerequisite you need to install is Git for macOS. Download Git for macOS [**here**](https://git-scm.com/download/mac), and follow the installer instructions.

{% hint style="info" %}
Note: You can use the default options for the installer.
{% endhint %}

### Install Node.js

The next step is installing Node.js. Download Node.js for macOS [**here**](https://nodejs.org/en/#download)**,** and follow the installer instructions.

{% hint style="warning" %}
Ensure you download Node.js version 8.12.0 \(LTS\)
{% endhint %}

{% hint style="info" %}
Note: You can use the default options for the installer.
{% endhint %}

### Open the Terminal

1. Press `⌘` + `Space` 
2. Type `Terminal` and press `Enter`

### Verify Node.js and NPM installation

1. Type `node --version` and press `Enter`
2. Type `npm --version` and press `Enter`

If Node.js and NPM have installed successfully, these commands should return the versions installed, e.g.:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
v8.12.0
6.4.1
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Step 2: Install the Tangram CLi Wallet

In the Terminal enter the following command to download the Tangram Wallet CLi NPM package:

1. Type `npm i -g @tangrams.io/tangram-cli-wallet` and press Enter

{% hint style="info" %}
Downloading and installing the Tangram CLi Wallet may take several minutes depending on your internet connection. Tor and vault.js will take up the majority of the download time.
{% endhint %}

Once you see the following text, the Tangram CLi Light-wallet has finished installing:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
Vault download finished!
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Next steps <a id="next-steps"></a>

{% hint style="success" %}
Congratulations! You have finished installing the Tangram CLi wallet, and can now move on to running the wallet.
{% endhint %}

{% page-ref page="../running-cli.md" %}



