# Uninstallation

## Step 1: Uninstalling The Tangram CLi Wallet

Launch the Terminal or Command Prompt, type `npm uninstall -g @tangrams.io/tangram-cli-wallet`  
and press `Enter`

Once the process has finished, close the Terminal or Command Prompt window.

{% hint style="success" %}
The Tangram CLi Wallet has now been uninstalled.
{% endhint %}

Although the wallet has been uninstalled, your Vault data remains.  If you reinstall the wallet at this point, your Vault will remain intact, with the same four keys as the initial install.  You will also retain access to all your TGM.

Proceed to Step 2 if you wish to erase your Vault data and completely uninstall the Tangram CLi wallet.

## Step 2: Delete Existing Vault Data

{% hint style="danger" %}
**WARNING: this step will erase your Vault data and you will lose all your TGM.**
{% endhint %}

### Mac:

Select the Finder and press `Cmd` + `Shift` + `G`.  A drop-down box will appear: paste the path **`~/npm-global/lib/node_modules`** into it and press enter.

Delete the folder named **"@tangrams.io"**

Press `Cmd` + `Shift` + `G` again.  Type **`~`** into the drop-down box and press enter.

Delete the two folders named **".tangramcli"** and **".kadencecli".**  

{% hint style="info" %}
You will need to enable hidden folders to see these two folders.
{% endhint %}

### Windows:

Navigate to **C:\Users\\(**_**YourUserName**_**\)\AppData\Roaming\npm\node\_modules** and delete the folder named **"@tangrams.io"**.

Delete the two folders named **".tangramcli"** and **".kadencecli"** from the home directory.

{% hint style="success" %}
Done!  You have now erased your Vault data and may reinstall if you wish.
{% endhint %}



