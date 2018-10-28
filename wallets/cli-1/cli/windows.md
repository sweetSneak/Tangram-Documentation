---
description: Tangram CLi Wallet installation for Windows
---

# Windows

## Step 1: Installation Prerequisites

Before you can install the Tangram CLi Wallet on Windows, you will need to install a few prerequisites. Fortunately this process is pretty straightforward.

### Install Git for Windows

The first prerequisite you need to install is Git for Windows. Download Git for Windows [**here**](https://git-scm.com/download/win), and follow the installer instructions.

{% hint style="info" %}
Note: You can use the default options for the installer.
{% endhint %}

### Install Node.js

The next step is installing Node.js. You can download the installer from [**here**](https://nodejs.org/en/#download).

{% hint style="warning" %}
Ensure you download Node.js version 8.12.0 \(LTS\) 
{% endhint %}

Launch the installer and follow the instructions.

### Install Windows Build Tools

Once Node.js is installed you will be able to install the rest of the pre-requisites. First up is Windows Build Tools.

Begin by launching the Command Prompt as an Administrator

#### Launching Command Prompt as an Administrator

<table>
  <thead>
    <tr>
      <th style="text-align:left">Windows 10</th>
      <th style="text-align:left">Windows 7</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Press <code>Win</code> + <code>R</code> then type <code>cmd</code> and press <code>Ctrl</code> + <code>Shift</code> + <code>Enter</code>
      </td>
      <td style="text-align:left">
        <p>Type <code>cmd</code> in the Start search, right-click on</p>
        <p>Command Prompt, and from the context menu select <em>Run as Administrator.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>Once Command Prompt is open, type `npm install --global --production windows-build-tools` and press `Enter`

For the remainder of this guide we will no longer need to run as an Administrator, so once the installation is complete, close the Command Prompt.

### Install node-gyp

Relaunch the Command Prompt by pressing `Win`+`R` then typing `cmd` and pressing `Enter`

{% hint style="warning" %}
Ensure you are _**not**_ running the Command Prompt as an Administrator.
{% endhint %}

Install `node-gyp` by typing `npm install -g node-gyp` and pressing `Enter`

## Step 2: Install the Tangram-CLi Wallet

Enter the command below into Command Prompt to download the Tangram CLi Wallet NPM package.

{% code-tabs %}
{% code-tabs-item title="Command Prompt" %}
```
npm i -g @tangrams.io/tangram-cli-wallet
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
Downloading and installing the Tangram CLi Wallet may take several minutes depending on your internet connection. Tor and vault.js will take up the majority of the download time.
{% endhint %}

Once you see the following text, the Tangram CLi Wallet has finished installing.

{% code-tabs %}
{% code-tabs-item title="Command Prompt" %}
```text
Vault download finished!
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Next steps

{% hint style="success" %}
Congratulations! You have finished installing the Tangram CLi wallet, and can now move on to running the wallet.
{% endhint %}

{% page-ref page="../running-cli.md" %}

