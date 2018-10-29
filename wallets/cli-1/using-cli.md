# Operation

## How to start using the Tangram CLi wallet

### Running the Tangram CLi Wallet

Type `tangram-cli-wallet` into your Terminal / Command Prompt and press `Enter`

{% hint style="info" %}
Before you can start issuing wallet commands in your Terminal / Command Prompt, you will need to unseal your Vault. You will need to do this each time you access your wallet.
{% endhint %}

### Unsealing Your Vault

1. When the text ``Please type `vault unseal` to finish unsealing the Vault.`` appears, type `vault unseal` and press `Enter`
2. At the prompt `Key:` copy one of the four saved KEYS given to you during the initial run of`tangram-cli-wallet` paste it into your Terminal / Command Prompt and press `Enter`

**EXAMPLE OF KEYS:**

```text
KEY 1: 9964cad01f6713fc825f6b8b87c6c9c5c23db246028f1fe7a698f55737fb3905ea
KEY 2: cd5bf39ca2d2ba8374d1865fd1d4551b9257a7a2712c629b3a27e07388d62cb3e6
KEY 3: 60608d3e03769e9057c105a2b6148529b0a44741e8c7bb27ea4c00e8e32dccb86c
KEY 4: da9ec762cf11c7414580ab466035e50ad2d6e4724a5906ac8aeca3aa43f26f851f
```

{% hint style="success" %}
Once Vault been successfully unsealed, you will see the following message:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Vault unsealed!
Would you like to automatically connect to your last known node endpoint? (Y/N)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Type `Y` and press `Enter`

{% hint style="info" %}
If you do not see the prompt to connect to the last known node endpoint, follow the instructions to `setnodeendpoint`, found [**here.**](https://tangram-docs.gitbook.io/docs/wallets/cli-1/running-cli#connecting-to-a-node)\*\*\*\*
{% endhint %}

{% hint style="success" %}
You have now successfully unsealed your Vault and connected to a Tangram node, and you can start issuing wallet commands.
{% endhint %}

### Errors

{% hint style="danger" %}
If at any time the following message appears:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
"msg":"exiting, killing child services, cleaning up"
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Then `tangram-cli-wallet` has stopped running. This may have occured due to an error, an incorrect entry such as a wrong password, or from the wallet timeout function. 

If this occurs, you must restart the Tangram CLi wallet by running `tangram-cli-wallet` and `vault unseal`, and then reconnecting to a node.

### Help

If at any point you need a list of available commands,  simply type `help` or `h` and press `Enter`.  This will return the following:

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Commands:

    help [command...]  Provides help for a given command.
    exit               Exits application.
    setnodeendpoint    Set Kadence contact Endpoint.
    wallet create      Create new wallet.
    wallet address     Add new address.
    wallet reward      Reward wallet.
    wallet transfer    Transfer funds to link account or inter-account.
    wallet balance     Get wallet balance.
    wallet get         Get wallet.
    wallet list        List wallets.
    vault unseal       Unseal vault using key(s).
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Exit

When you want to exit the Tangram CLi wallet, simple type `exit` and press `Enter`

{% hint style="success" %}
You have successfully exited the Tangram CLi wallet when you see the following message:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
"msg":"exiting, killing child services, cleaning up"
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Creating a Wallet 

1. Type `wallet create` and press `Enter`
2. At the prompt `Password:` enter an appropriate password. and press `Enter`

{% hint style="danger" %}
**Store your password in a secure place and do not lose or forget it, as in this release it cannot be reset or recovered.**
{% endhint %}

{% hint style="success" %}
Once your new wallet has been generated, you will see a message with your new wallet ID, such as the following:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Generated wallet id_0b3dbbc922ba44cc41ad3d6d00a6463820f30cf1
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
You can retrieve your wallet IDs at any time by typing `wallet list` and pressing `Enter`
{% endhint %}

{% hint style="info" %}
 If you use multiple passwords within Vault, you may want to save your new wallet ID with it's corresponding password in a secure place.
{% endhint %}

### Adding an Address to Your Wallet

1. Type `wallet address` and press `Enter`
2. At the prompt `Identifier:` type or paste the wallet ID that you wish to add an address to and press `Enter`
3. At the prompt `Password:` enter your wallet password and press `Enter`

{% hint style="success" %}
Once your new address has been generated, you will see a message containing secret, public, and private keys, and your new wallet address.
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
base58: 'tgm_vJmvC3JtBFHr3PQQno7mWFh25AqcKiyH67DgiJAit3WkdBfApa9cquhAVEVxM1kyxVvYKpLRNtsZngVfX6Ph5z94azZ6eF8My8TBV2'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
Save your new base58 wallet address in an accessible location.
{% endhint %}

{% hint style="info" %}
The secret, public, and private keys returned here are stored in Vault and do not need to be recorded by the user.
{% endhint %}

### Rewarding Your Wallet with $TGM

{% hint style="info" %}
This function is for testing puposes only.
{% endhint %}

1. Type `wallet reward` and press `Enter`
2. At the prompt `Identifier:` type or paste the wallet ID of the address you wish to reward, and press `Enter`
3. At the prompt `Address:` type or paste the wallet address that you wish to reward to and press `Enter`
4. At the prompt `Amount:` type the amount that you wish to reward to and press `Enter`
5. At the prompt `Password:` type your wallet password and press `Enter`

**EXAMPLE INPUT:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Identifier: id_28999a3990ad23f2191f82fad7a93090f06e6c63
Address: tgm_vJmshBCmUUt2GpEnjueCktd43hF8tgEiic5VarKMLXYqNZmyxRmFVvd7YcqwdiVgSSuA1SaZm8UhvZCK4HoeLeJgXWHDgqpJX3aGGL
Amount: 99999999
Password: ********
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="success" %}
Your wallet address has been rewarded once you receive the following message:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
{ reward_block: '99d451732b78c989053cb4e43a799e08bed9217a44c5e6228d8d82b60baec1a159ac72c8e1abcc18e513a625648ac766778d336a514f58a4f97186e221835a62' }
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Transferring or Sending $TGM

1. Type `wallet transfer` and press `Enter`
2. At the prompt `Identifier:` type or paste the wallet ID of the address you wish to transfer from and press `Enter`
3. At the prompt `Account:` type or paste the wallet address that you wish to transfer from and press `Enter`
4. At the prompt `Change:` type or paste the wallet address that you wish to transfer the change to and press `Enter`
5. At the prompt `Link`: type or paste the wallet address \(base58\) that you wish to transfer the amount to and press `Enter`
6. At the prompt `Amount:` type or paste the amount that you wish to transfer and press `Enter`
7. At the prompt `Password:` type your wallet password and press `Enter`

{% hint style="info" %}
If you do not wish to completely empty the address you are sending from, enter the same address at the `Account:` and `Change:` prompts.
{% endhint %}

**EXAMPLE INPUT:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Identifier: id_28999a3990ad23f2191f82fad7a93090f06e6c63
Account: tgm_vJmshBCmUUt2GpEnjueCktd43hF8tgEiic5VarKMLXYqNZmyxRmFVvd7YcqwdiVgSSuA1SaZm8UhvZCK4HoeLeJgXWHDgqpJX3aGGL
Change: An address you own (can be same as above) 
Link: An address you own or a payee address
Amount: 590.5
Password: ********
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="success" %}
Your transfer has completed once you receive the a message with the transaction details, such as the following:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
account: '9aa0b96bcd1343d413867a0e7646bfbe1f165754',
previous: '99d451732b78c989053cb4e43a799e08bed9217a44c5e6228d8d82b60baec1a159ac72c8e1abcc18e513a625648ac766778d336a514f58a4f97186e221835a62',
link: 'f7a8f18c6a3cdf3e44fd8ca09c08194e50beb23a',
signature: 'ba9afffa763f36ae70f61edc826c7b416212c86115464c12cc747071f12c0a51a58998f532ada039e0723083a21f275690d56d7e3313bfe7d5197c5929a2f404',
cipher: 'wq81BcKpLCpPRXTDvcOswotOw4zDhsKvDALCuiDDiAUjFjfCpMOcw63CvkknKSHDghNzworDiFnDnHoxwrvDj1/Ds1khNsOcwr4tCcOqHX/DhCzDm2/DnMKWwrFNBEAbR8OowqbDmMK3KsOBw7/CuWzDjjgPw5RQw5nDhAVDwoLDrsKTYMKNwrRnGzl5dFsAwrHDrX8eLHxvw4HCqcOLIhBGwoEuwrg5NcOVwp8qwrPDo3zDmcKBwrN4w6YUMDVvw73DhQtiwq3ChsOBCcO2wrzCuk7CoUA5FSrDsMOvH3DDvTTDu3rDi8K/w78yw4Fpw4fCpTzDh8OqwoxLMMKBw4HDr8ONw73CkWMaw6nDtsOjwrzDtsOEw7opwpjDnm3DvQrDliNNwppRdWx8bXXCvjRUwoBnAWbDtgzDssOkfcOiSsKwwqLDgTF+S8KtVQkJwonCkgrChMOaw75Iw614OsO8d3XCusKOQsKJwooPMUzDkTt8fWrDkDfDkRfCniVDw6rDlUxmM8OVwq0ywoDDmgZFw7l3Swkgw4w1Rw7Cj1nCisOZXgzCm8KIWgTCqBbDh8Kow5w7w7/ChVAQdcOgcHR9dMO7wr/Dl8O3w7NWw6LDt8KjwoTCisOLw7TClwfCnsKZw7jCt2FFO8KFw67DisK3c8KUTMOtwpbDqilVwq4GVcOHAjDDsMKLDE0nw5Ysw7YLw7Rpw7rChcK3Gi7CncKaa8O/CMOgw6puZ8KpIcO1WlDCvTRRQMOjwpVlw6DClsONNcOYGUprwoQJwo8KaFB/TMKUN8K8woMYwr7CiUPCu3fDsjx5w5J4wrXCiMKCwrLCgsKJKUvDlcOcDwZowr7CvGZqW8Oyw5PDn8KMwo7CocOVw55Ew5LCo8KKw7lbwqPChMKfw7c0LHHCpE84w63DoVHDlsOvwpLDlMO1wq56AHTCtzzDh8K6E8K3w7LDrsOmw6jDv0s5w5FLwrvCpMKnAV3Dm0dFAcKJwp7ChxDDkwVew6YwK8Kjawd4w5NBw6vDv8KMezTCqw7DkWnDmcKYeB7CqQNCw5HCswXCrz3Co8Kkw7F1axXDumnDt1IawofDjMKTw7ozMTPClHdpwqvDnsKIwoB2HcOZw4/DlCkEwqXCm8KWPGrDucKmwpjChsKDVsKYw6DCuRPCjMODwpLDnwnCvMO8KENgw7tgeAXCqHBFw4TDtx7DuzlvKEHClcKQDwB1JMKkwqnCksKcP8OEZG7DhMOZCTU=',
opcode: '0245a057230701a1836abd31175e096df49b350bd4dea1e1ae1fc66bea5fffc04e',
work: 399,
hash: '004359c5fa781ad95f6f0aa191e24e649372cefaf856e04511d1a629190de5d210ecfcd7348c842524e4de56d33392a75221cc869802bed9a3d83f1a39239a4a',
timestamp: 7.154572501545772 }
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Check Wallet Balance

1. Type `wallet balance` and press `Enter`
2. At the prompt `Identifier:` type or paste the wallet ID whose balance you want to check and press `Enter`
3. At the prompt `Account:` type or paste the wallet address whose balance you want to check and press `Enter`
4. At the prompt `Password:` type your wallet password and press `Enter`

**EXAMPLE INPUT:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Identifier: id_28999a3990ad23f2191f82fad7a93090f06e6c63
Account: tgm_vJmshBCmUUt2GpEnjueCktd43hF8tgEiic5VarKMLXYqNZmyxRmFVvd7YcqwdiVgSSuA1SaZm8UhvZCK4HoeLeJgXWHDgqpJX3aGGL    
Password: ********
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="success" %}
Your wallet balance will display in a message such as the following:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
{ Balance: '8968.500000000000' }
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Wallet Get

1. Type `wallet get` and press `Enter`
2. At the prompt `Identifier:` type or paste the wallet ID whose data want to get and press `Enter`
3. At the prompt `Password:` type your wallet password and press `Enter`

**EXAMPLE INPUT:**

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
Identifier: id_28999a3990ad23f2191f82fad7a93090f06e6c63
Password: ********
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="success" %}
You will receive a message such as the following:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
{"id":"id_28999a3990ad23f2191f82fad7a93090f06e6c63","hash_pwd":null,"secret":null,"key_pairs":[],"stealth":[{"keyPairs":{"index":1,"secretKey":"3cbe2040d724949e851ac14d231236b7509f91c26e892500a85f7b0b931017be4a1feca56a5dae33be08ebe983f8d3cb950d8392862760252d7c1f856c6594f5d9041e500ad7957b6ec111803cd67fe8f9120e509b730e55e520d32d02258a99e4e05873fd2509db2761d51c94a2b96ed04ba4b18a495841bbae348f3424d0f1f15d5a488128b8795c00a32dc34623c3b0c3c642e207a6da1e138e73bc73cae701723d7d35541e08ce60d3e8e651979daa0946ccbab7ff0eeaa60a31b6c666fa502c3b518a36bbf3f1fdc6b7313d5206a53fc2b6314ce5b052f4fcba7c4b9549754fee3c10fdb43494d8a83438da07ff845ce38ce08aa00f261ac2b1bb7cba0c2a5c790d91a185b73555d2aebed55d7831db4030c8fa68768bf87a22bc04fab19bf41d6211e9fcaa59c6e32ded6a2bc8eb3b6a3f8c1dd22642666017248a98ffeec85a8246e0d8ea2cf700fae095ce6fc6552256e8f607b4ffe312e471f3c1ef93f1f09607fc9f69a4dbd084b0214320b2732c09c4b5607e8384c18616440fb3069f49c2f14c3a9b085b6a20d9ecd88236c9200fb4d69280332e498f38b38db02f864a0e0a64fe767c09fb96d033e91052f1b0b58d7e723b78d88b67158b8d775b657ffe7f7960e2f987061c27e796bcec4c637061dfa9eca5717f1eac2ed8c2cb313f72ccfb5d76f636d03c6c3f35ad7302549a487a6605352256f6f9a6041a",
"publicKey":"tgm_e007b55780102a7c4f051b1bd1688f90c0c18bd6bc9a3d8e92d37d2c9537bb92"},
"payload":{"privateKey":"131329adb8d07f6073826560e7d2fcdacb9011b7c45b19178f42bf0ea1087149",
"publicKey":"039507106ea86c976e772ff2a10124b339fda6b5f641e1868936bfcd8a71e4155d"},
"scan":{"privateKey":"21b94d76e6b6f56f0e21d34f0b0dbca3205dc3d10720f1f01a79e61ebaefad2f",
"publicKey":"03790efa324f901912c39afb61a1e5df693994ffcbe2a6b0a7c081bd2b9c944747"},
"base58":"tgm_vJmxuz6fre7RQUbFKcCDnUeqnPMeuLviTdAzzkKSyWZty5JXiN2a6nDLTQgXh4St7fLqiELvhXgwYb1rzE1s5xYDed5R9oViuR7aqk"},
{"keyPairs":{"index":1,"secretKey":"06420edd5a4d4584b2ea1c66b75dd773d28f80ad69636864799db55224c2d612c4bc0af58f8dfb65b546c2ef79f74fe78e959fbcbfddc7bfd09a9323ec5bd9ac580ffbec66b3069c636b8370213016975541740e2ce054f708831915425aa7754cac6759e7deb9c6a7f1b9757590170f10d5cdb210e820066b1676db89ae2c171e6539c4a0d3007f0e660efedae6ec4f74150d45b270faec6c63364b9138127dec945197db3e97f1702e26d8b7a3e0e2d1f0655161a802cda2f9ea56476c28bf9d60db7c5ef503a701b8c1020763e421a727370f28f4533138963129d9b57c0926df0d51e03ef8033960226ec947e76ba3c59cf93e5352dd1e6e6f2e59f00ad6b1eadf0b2e83de87e6fbaa62e7ae6b32172b6d3466349252e31b984a938320e593d307722ba9c1c3788099db35ac9e39a5b0a6a283bb24448cc1581c282f7f68dff19285d70d618dd0a56fc1bf826fd12b22372297061416f8fa13c211888ffc1e29b2cb24f17e1b2999e1b5fd113fe5e824059d99e0d4292bd0ddef18f0b6204ba7468dcf4f906a0885ab2c7dae0cfa3237909ead9862ee53d0209df19a253c2f0e0ce81ed799fa2e20f898a6442aba919950872f6749c81698ed4e5ba55fa12bd9e6beead55eb823e9697b625cb8035c1dd56312a4186e6b969c5ba9dd75ac551eb21e23e8e4112a7e832a37fab167752d5f718145f7bf8c0e45bdb97267b6","publicKey":"tgm_c4f292f1baab57e12fdd60f137ce714b73c406dd4d9ea28db1eb821f3a0c3d3a"},
"payload":{"privateKey":"2648ef9e49964c81d51c0813641d5c6952f5fe617e3112852e9c01635c98eb1b",
"publicKey":"023c9bf9e949f1e54771e4978a6d109fc561939925034e6f4d50240971775bcf90"},
"scan":{"privateKey":"b2e698089f133e636b17f00534f9b9f03288ae2ebf61ebef8a2087373c8db3f3",
"publicKey":"02175981e6e65e7faedc8810e4a0e1363fd0f1831080f8c2a36815a6dfaa7be0f6"},
"base58":"tgm_vJmshBCmUUt2GpEnjueCktd43hF8tgEiic5VarKMLXYqNZmyxRmFVvd7YcqwdiVgSSuA1SaZm8UhvZCK4HoeLeJgXWHDgqpJX3aGGL"}],
"box_seal":[{"privateKey":"HsKqfntYZcKFRMKRwpEhw5DCghouw54/wpwuwo3Crw1vfEPCpz7Ctx4bLMOC",
"publicKey":"YRhNwoY6flfCgn7DkC3DnsO3wr8Sw7HCiUbDsA/Ds0wiw50fJcOzw4AzbcOIEg=="}],
"homomorphic":[{"privateKey":"esOJIsKAXMODFzlhwo7CrF/CrsKowrQXPcKLw6EfFsOSEmV2NMKEwrl7wp/DjB7Ck3k3PsOAVwjCucKDw43CvGjCs0TDnhokw6JTQMO/w7YLSTVhUcO6wqTDvjEg",
"publicKey":"cH3Dr8KBRsKow5XDtcOHwqAvUcO0w57DscKfAm0hw53DhcKVXRnCngfDj8OFFcO0Yw3CtxnDpH/DnEEew5l4wp4PDEPDqnLCvMKHw6bCs8KZIwlJLcOIPnUFw4JdwqkUwonDjsKwwpgMw7nDncKFASBAdwbDsAZBc0gZIsOnwqbCs8OYwplAw6pTasKrAcKX"}]}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
The `wallet get` command will be updated in future releases. For now this command is only used as an FYI.
{% endhint %}

### Wallet List

1. Type `wallet list` and press `Enter`

{% hint style="success" %}
You will receive a message containing the list of wallets associated with your Vault:
{% endhint %}

{% code-tabs %}
{% code-tabs-item title="Terminal \(Tangram Wallet CLi\)" %}
```text
[ 'id_28999a3990ad23f2191f82fad7a93090f06e6c63/',
  'id_5f35657e7dd880c9f5d1edfe248d1f500fa792a1/',
  'id_8ecb0b94f3a4c52e1239b28431f9388900e294ff/',
  'id_9555cffdc029022d59ddad768f3f7fe3f6cf64fe/',
  'id_ebecd6e7a4dbce84b6eee03a1395a6d4bcbd0702/' ]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

