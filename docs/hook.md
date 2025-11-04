[{"inputs":[{"internalType":"address","name":"_marketingWallet","type":"address"},{"internalType":"address","name":"_payoutWallet","type":"address"}],"stateMutability":"nonpayable","type":"constructor"},{"anonymous":false,"inputs":[{"indexed":true,"internalType":"address","name":"owner","type":"address"},{"indexed":true,"internalType":"address","name":"spender","type":"address"},{"indexed":false,"internalType":"uint256","name":"value","type":"uint256"}],"name":"Approval","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"internalType":"address","name":"previousOwner","type":"address"},{"indexed":true,"internalType":"address","name":"newOwner","type":"address"}],"name":"OwnershipTransferred","type":"event"},{"anonymous":false,"inputs":[],"name":"TradingOpen","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"internalType":"address","name":"from","type":"address"},{"indexed":true,"internalType":"address","name":"to","type":"address"},{"indexed":false,"internalType":"uint256","name":"value","type":"uint256"}],"name":"Transfer","type":"event"},{"inputs":[{"internalType":"address","name":"owner","type":"address"},{"internalType":"address","name":"spender","type":"address"}],"name":"allowance","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"spender","type":"address"},{"internalType":"uint256","name":"amount","type":"uint256"}],"name":"approve","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"account","type":"address"}],"name":"balanceOf","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"buyTax","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"decimals","outputs":[{"internalType":"uint8","name":"","type":"uint8"}],"stateMutability":"pure","type":"function"},{"inputs":[{"internalType":"address","name":"account","type":"address"},{"internalType":"bool","name":"value","type":"bool"}],"name":"excludeFromFee","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"marketingShare","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"marketingWallet","outputs":[{"internalType":"address payable","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"maxTaxSwap","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"name","outputs":[{"internalType":"string","name":"","type":"string"}],"stateMutability":"pure","type":"function"},{"inputs":[],"name":"openTrading","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"owner","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"payoutShare","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"payoutWallet","outputs":[{"internalType":"address payable","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"renounceOwnership","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"rescueETH","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"tokenAddress","type":"address"}],"name":"rescueToken","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"sellTax","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"_marketingWallet","type":"address"}],"name":"setMarketingWallet","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_payoutWallet","type":"address"}],"name":"setPayoutWallet","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"_marketingShare","type":"uint256"},{"internalType":"uint256","name":"_payoutShare","type":"uint256"}],"name":"setShareRatios","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"_buyTax","type":"uint256"},{"internalType":"uint256","name":"_sellTax","type":"uint256"}],"name":"setTax","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"uint256","name":"threshold","type":"uint256"}],"name":"setTaxSwapThreshold","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[],"name":"symbol","outputs":[{"internalType":"string","name":"","type":"string"}],"stateMutability":"pure","type":"function"},{"inputs":[],"name":"taxSwapThreshold","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"totalSupply","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"pure","type":"function"},{"inputs":[],"name":"tradingOpen","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"recipient","type":"address"},{"internalType":"uint256","name":"amount","type":"uint256"}],"name":"transfer","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"sender","type":"address"},{"internalType":"address","name":"recipient","type":"address"},{"internalType":"uint256","name":"amount","type":"uint256"}],"name":"transferFrom","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"newOwner","type":"address"}],"name":"transferOwnership","outputs":[],"stateMutability":"nonpayable","type":"function"},{"stateMutability":"payable","type":"receive"}]# Setup

For direnv to work properly it needs to be hooked into the shell. Each shell
has its own extension mechanism.

Once the hook is configured, restart your shell for direnv to be activated.

## BASH

Add the following line at the end of the `~/.bashrc` file:

```sh
eval "$(direnv hook bash)"
```

Make sure it appears even after rvm, git-prompt and other shell extensions
that manipulate the prompt.

## ZSH

Add the following line at the end of the `~/.zshrc` file:

```sh
eval "$(direnv hook zsh)"
```

## Oh my zsh

Oh my zsh has [a core plugin with direnv](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/direnv) support.

Add direnv to the plugins array in your zshrc file:

```sh
plugins=(... direnv)
```

## FISH

Add the following line at the end of the `~/.config/fish/config.fish` file:

```fish
direnv hook fish | source
```

Fish supports 3 modes you can set with the global environment variable `direnv_fish_mode`:

```fish
set -g direnv_fish_mode eval_on_arrow    # trigger direnv at prompt, and on every arrow-based directory change (default)
set -g direnv_fish_mode eval_after_arrow # trigger direnv at prompt, and only after arrow-based directory changes before executing command
set -g direnv_fish_mode disable_arrow    # trigger direnv at prompt only, this is similar functionality to the original behavior
```

## TCSH

Add the following line at the end of the `~/.cshrc` file:

```sh
eval `direnv hook tcsh`
```

## Elvish (0.12+)

Run:

```
~> mkdir -p ~/.config/elvish/lib
~> direnv hook elvish > ~/.config/elvish/lib/direnv.elv
```

and add the following line to your `~/.config/elvish/rc.elv` file:

```
use direnv
```

## Nushell

Add the following hook to your `$env.config.hooks.env_change.PWD` list in `config.nu`:
```nushell
{ ||
    if (which direnv | is-empty) {
        return
    }

    direnv export json | from json | default {} | load-env
}
```

> **Note**
> you can follow the [`nu_scripts` of Nushell](https://github.com/nushell/nu_scripts/blob/main/nu-hooks/nu-hooks/direnv/config.nu)
> for the always up-to-date version of the hook above

## PowerShell

Add the following line to your `$PROFILE`:

```powershell
Invoke-Expression "$(direnv hook pwsh)"
```

## Murex

Add the following line to your `~/.murex_profile` file:

```sh
direnv hook murex -> source
```
