---
description: Learn more about common error codes and how to resolve them.
---

# Errors

{% hint style="info" %}
**This page is under construction \(ongoing\).**
{% endhint %}

## General Errors

## "Exiting, Killing Child Services, Cleaning Up"

Although this message is not an 'error' as such, it has been included here for the sake of clarity.  You may receive the message `exiting, killing child services, cleaning up` at any time while you are using your wallet.  

{% hint style="info" %}
**Tip:** "Exiting, killing child services" may sound like a crime is being commited, but it's actually programming-speak for "making sure the program has closed correctly" :\)
{% endhint %}

**Example of exit message:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
{"name":"kadence","hostname":"My-MacBook-Pro.local","pid":1491,"level":30,"msg":"exiting, killing child services, cleaning up","time":"2018-10-16T04:54:30.709Z","v":0}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

This message may occur at any time, and simply means that your wallet has closed and your Vault has been sealed for your security.  There are a variety of reasons why this message may appear, such as:  

1. You forgot to connect to a node.
2. An error occurred.
3. An incorrect entry such as a wrong password.
4. The wallet timeout function activated.

{% hint style="success" %}
You will need to reopen the Tangram CLi wallet.
{% endhint %}

Reopen your wallet by running `tangram-cli-wallet` again, unseal your Vault, and reconnect to a node.

If you are unsure how to do this, follow the Tangram CLi wallet operation instructions found [**here**](https://tangram-docs.gitbook.io/docs/wallets/cli-1/using-cli)**.**

## "EACCES: Permission Denied" - "Missing Write Access"

At the beginning of the wallet installation on macOS, the following error may occur:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
npm WARN checkPermissions Missing write access to /usr/local/lib/node_modules
npm ERR! path /usr/local/lib/node_modules
npm ERR! code EACCES
npm ERR! errno -13
npm ERR! syscall access
npm ERR! Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
npm ERR!  { Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
npm ERR!   stack: 'Error: EACCES: permission denied, access '/usr/local/lib/node_modules'',
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'access',
npm ERR!   path: '/usr/local/lib/node_modules' }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator (though this is not recommended).
```
{% endcode-tabs-item %}
{% endcode-tabs %}

This error occurs because NPM does not have write access to the directory\(s\) it is trying to access during a global installation.

{% hint style="success" %}
To rectify this issue on macOS, configure NPM to use a different directory.
{% endhint %}

To configure NPM to use a different directory; follow these steps:

1. In your terminal, type `mkdir ~/.npm-global` and press `Enter`
2. Type `npm config set prefix '~/.npm-global'` and press `Enter`
3. Type `export PATH=~/.npm-global/bin:$PATH` and press `Enter`
4. Type `source ~/.profile` and press `Enter`

After this you will need to reinstall the CLi wallet by typing `npm i -g @tangrams.io/tangram-cli-wallet` and pressing `Enter`

## "Permission Denied" During Address Creation

During wallet address generation, the following error will occur:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
1 error occurred:

* permission denied
```
{% endcode-tabs-item %}
{% endcode-tabs %}

After this error, you will see a message containing secret, public, and private keys, and your new wallet address.  Your new address has been correctly generated and can be used. 

This error presenting is a known issue and will be resolved in subsequent builds.

{% hint style="success" %}
No action required; this error can safely be ignored.
{% endhint %}

## Line Wrap \(Text Overflow\) in Terminal / Command Prompt

This condition occurs when the line of text entered into your Terminal / Command Prompt window exceeds the width of the window, and appears to 'overflow' to the lines below.

**Example of error condition:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
tangram$ wallet balance
Identifier: id_54ff849a1b87e3b793965cb8fae2fbe7f8edce0d
Address: tgm_vJmvC3JtBFHr3PQQno7mWFh25AqcKiyH67DgiJAit3WkdBfApa9cquhAVEVxM1kyxVvYKpLRNtsZngVfX6Ph5z94azZ6eF8My8TBV2
4azZ6eF8My8TBV
4azZ6eF8My8TB
4azZ6eF8My8T
4azZ6eF8My8
4azZ6eF8My
4azZ6eF8M
4azZ6eF8
4azZ6eF
4azZ6e
4azZ6
4azZ
4az
4a
4
```
{% endcode-tabs-item %}
{% endcode-tabs %}

This is an issue with the commander used \(Vorpal\) and will be resolved in subsequent builds.  It is a display issue only, so you can keep entering commands and the overflowed text will get overwritten.

{% hint style="success" %}
To rectify this issue, either increase your window size, or set your Terminal / Command Prompt to disable line wrapping.
{% endhint %}

To disable line wrapping on Windows:

1. `Right-click` on the Command Prompt toolbar and select _Properties_
2. Select the _Options_ tab.
3. Increase the _Buffer Size:_ until the text wrapping issue no longer occurs.

To disable line wrapping on Linux:

1. Type `setterm -linewrap off` and press `Enter`
2. To re-enable, type `setterm -linewrap on`

To disable line wrapping on Mac:

1. Type `off: tput rmam` and press `Enter`
2. To re-enable, type `on: tput smam` and press `Enter`

## "Deprecated socks@1.1.10" During Wallet Installation

The following warning may occur at the beginning of the Tangram CLi wallet installation:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
npm WARN deprecated socks@1.1.10: If using 2.x branch, please upgrade to at least 2.1.6 to avoid a serious bug with socket data flow and an import issue introduced in 2.1.0
```
{% endcode-tabs-item %}
{% endcode-tabs %}

This warning is to inform you that there you are using a superseded version of "socks." 

{% hint style="success" %}
No action required; this error can safely be ignored.
{% endhint %}

## "Failed at Granax@3.1.4" During Wallet Installation

The following error may occur partway through the Tangram CLi wallet installation:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! granax@3.1.4 postinstall: `node script/download-tbb.js`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the granax@3.1.4 postinstall script.
npm ERR! This is probably not a problem with npm. There is likely additional log
ging output above.
npm ERR! Failed at the granax@3.1.4 postinstall script.
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Generally this occurs if your anti-virus or firewall is blocking the download of Tor.  Although your antivirus or firewall might allow Tor download and operation, it may flag the _automatic_ download and install of Tor.

{% hint style="success" %}
Temporarily disable your anti-virus or firewall until the installation is complete.
{% endhint %}

## "Timed Out Waiting For a Response"

You may receive `Error: Timed out waiting for response`  or  `gateway timeout` during execution of commands which require interaction with a node.

**Example of error occurrence:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
{ Error: Timed out waiting for response
    at KademliaNode._timeout (/Users/me/.npm-global/lib/node_modules/@tangrams.io/tangram-cli-wallet/node_modules/@kadenceproject/kadence/lib/node-abstract.js:229:15)
    at Timeout.setInterval [as _onTimeout] (/Users/me/.npm-global/lib/node_modules/@tangrams.io/tangram-cli-wallet/node_modules/@kadenceproject/kadence/lib/node-abstract.js:163:28)
    at ontimeout (timers.js:498:11)
    at tryOnTimeout (timers.js:323:5)
    at Timer.listOnTimeout (timers.js:290:5) type: 'TIMEOUT' }
tangram$ {"name":"kadtools","hostname":"My-MacBook-Pro.local","pid":1827,"level":40,"msg":"gateway timeout","time":"2018-10-16T06:48:37.035Z","v":0}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

This error occurs when your wallet did not receive the reply it was expecting from a node.  The command you entered will not have completed, e.g. if you received this error during a funds transfer, no $TGM will have transferred.  Any further commands you type will result in the message `exiting, killing child services, cleaning up`

{% hint style="success" %}
You will need to exit and reopen the Tangram CLi wallet.
{% endhint %}

Exit your wallet by typing `exit` and pressing `Enter`.  Reopen your wallet by running `tangram-cli-wallet` again, unseal your Vault, and reconnect to a node.

If you are unsure how to do this, follow the Tangram CLi wallet operation instructions found [**here**](https://tangram-docs.gitbook.io/docs/wallets/cli-1/using-cli)**.**

## Windows Error\(s\)

## "Could not install Visual Studio Build Tools" 

If you're a Windows user and the error of `Could not install Visual Studio Build Tools` appears, then note that there was an error in installing \*unknown and to mitigate the error you will need to download Visual Studio manually.

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram CLi Wallet\)" %}
```text
1 error occured: 

* Could not install Visual Studio Build Tools. 
Please find more details in the log files, which can be found at
C:\Users\...\.windows-build-tools

Now configuring Python... 

All done!

+ windows-build-tools@5.0.0
added 143 packages from 96 contributos in 46.59s

C:\Windows\system32
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Effects of error and why it occurs

{% hint style="success" %}
Download Visual Studio manually:

[https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=15](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=15)  
{% endhint %}

## Questions?

We're always happy to help with code or other questions you may have! Search our documentation, get in touch through our forum \(Coming Soon!\). You can also chat live with other developers and community members in the \#cli-discussion channel on [Discord](https://www.discord.tangrams.io).

