# Create a New Vault

With the v1.0 CLi wallet there is no recovery function if you lost your keys and cannot unlock your Vault.  A recovery function is planned for the mainnet wallet.  At this time, the only option is to uninstall/reinstall the CLi wallet.

## Step 1: Uninstall Tangram CLi wallet

Launch the Command Prompt by pressing `Win`+`R` then typing `cmd` and pressing `Enter`
```
npm uninstall -g @tangrams.io/tangram-cli-wallet
```

## Step 2: Delete Existing Vault Data

Delete  `.tangramcli` and `.kadencecli` from the home directory.

### Mac
Delete @tangrams.io from .npm-global > lib > node_modules.
### Windows
Delete @tangrams.io from C:\Users\(UserName)\AppData\Roaming\npm\note_modules@tangrams.io

## Step 3: Reinstall Tangram CLI wallet
