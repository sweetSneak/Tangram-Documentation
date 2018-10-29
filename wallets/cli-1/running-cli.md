# Initial Run

## Step 1: Running the Tangram CLi Wallet

Once the Tangram CLi Wallet NPM package has downloaded successfully, you will need to run and initialise the Tangram CLi Wallet for the first time. 

1. Type `tangram-cli-wallet` into your Terminal / Command Prompt and press `Enter`

{% hint style="info" %}
If this command results in an error \(e.g. "command not found"\), ensure that you have NPM installed correctly.  You may need to reinstall the Tangram CLi wallet beginning from Step 2 of the installation instructions.
{% endhint %}

### Success! <a id="next-steps"></a>

You should see the below message in your Terminal / Command Prompt if you have successfully installed and run the Tangram CLi wallet for the first time:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
###########################################################
#                   !!! ATTENTION !!!                     #
###########################################################
    We noticed this is the FIRST time you've started       
    the Tangram wallet. Your wallet is encrypted in        
    Vault using Shamir's secret sharing algorithm.         
    Please store all of the following keys in a safe       
    place. When unsealing the vault you may use any        
    1 of these keys. THESE ARE NOT RECOVERY KEYS.          


KEY 1: 9ca251a8b5001a52d789df2f07abafb95b91b9dfd85246bdc70f8616d4c50c2d65
KEY 2: 6d20244156e7a862697cadf06fe15d47253d22c30cf610ea0277d1783f479c5f04
KEY 3: 5b6ce8994fd323a595671759a0c6305de8ee4000a47ff4cede0cf5017c0bffe551
KEY 4: 3337a92262a2c5189753332d79e761e828a9df8f51805a7757be4caae950e1c127
Ensure you save this somewhere easily accessible


    You will need to unseal the Vault everytime you        
    launch the CLI Wallet.                                 
    Please type `vault unseal` to unseal the Vault.        
###########################################################
#                   !!! ATTENTION !!!                     #
###########################################################
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="warning" %}
This message will only appear the first time you run the Tangram CLi wallet after installation.
{% endhint %}

{% hint style="danger" %}
**Before you continue, ensure you copy and save the four KEYS from your Terminal / Command Prompt to a safe place.**  
{% endhint %}

The initial run of `tangram-cli-wallet` creates four separate KEYS which you will thereafter use to `unseal` your wallet \(vault\). 

{% hint style="info" %}
Before you can start issuing wallet commands in your Terminal / Command Prompt, you will need to unseal your Vault and connect to a Tangram node.
{% endhint %}

### Unsealing Your Vault

1. When the text ``Please type `vault unseal` to finish unsealing the Vault.`` appears, type `vault unseal` and press `Enter`
2. At the prompt `Key:`, copy one of the four saved KEYS given to you during the initial run of`tangram-cli-wallet` paste it into your Terminal / Command Prompt and press `Enter`

{% hint style="success" %}
Once Vault been successfully unsealed, you will see the following message:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Vault unsealed!
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Connecting to a Node

1. Type `setnodeendpoint` and press `Enter`
2. At the prompt `Identity:` type or paste `180480e10af1df123f6cd35eae4118e3e6e1aed7` and press `Enter`
3. At the prompt `Endpoint:` type or paste `pduvx6ra3mim4msfeimbqkkyxaqlihm6mwjcpem6r7jg6b3xcpsagkid.onion` and press `Enter`
4. At the prompt `Port:` type `82` and press `Enter`

What you have typed should look like this:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
setnodeendpoint
Identity: 180480e10af1df123f6cd35eae4118e3e6e1aed7
Endpoint: pduvx6ra3mim4msfeimbqkkyxaqlihm6mwjcpem6r7jg6b3xcpsagkid.onion
Port: 82
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="success" %}
Once you have successfully connected to a node, you will see the following message:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Connected
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Exit Your Wallet

Type `exit` and press `Enter`

### Next steps <a id="next-steps"></a>

{% hint style="success" %}
Congratulations! You have run the Tangram CLi wallet for the first time, and can now move on to using the wallet.
{% endhint %}

{% page-ref page="using-cli.md" %}

