# CLi

## CLi

### Supported Platforms

| **MacOS** | **Windows** | **Linux** |
| :--- | :--- | :--- |
| [**Installation guide**](cli/mac.md) | [**Installation guide**](cli/windows.md) | [**Installation guide**](cli/mac.md) |

### Checklist  <a id="checklist"></a>

1. Ensure you're running Python 2.7
2. Ensure you download Node.js version 8.12.0 \(LTS\)

## Re-Installing the CLi

With the v1.0 CLi wallet there is no recovery function if you lost your keys and cannot unlock your Vault. A recovery function is planned for the mainnet wallet. At this time, the only option is to uninstall/reinstall the CLi wallet.

### Step 1: Uninstall Tangram CLi wallet

Launch the Command Prompt by pressing `Win`+`R` then typing `cmd` and pressing `Enter`

```text
npm uninstall -g @tangrams.io/tangram-cli-wallet
```

### Step 2: Delete Existing Vault Data

Delete `.tangramcli` and `.kadencecli` from the home directory.

#### Mac

Delete `@tangrams.io` from `.npm-global > lib > node_modules`

#### Windows

Delete `@tangrams.io` from `C:\Users\(UserName)\AppData\Roaming\npm\note_modules@tangrams.io`

### Step 3: Reinstall Tangram CLI wallet

Now just reinstall with `npm i -g @tangrams.io/tangram-cli-wallet` and you should be up and running with a new vault.

