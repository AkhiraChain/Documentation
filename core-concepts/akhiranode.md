# akhiranode

**akhiranode** is a command line blockchain application for running akhirachain nodes and validators. It is built using Cosmos SDK and Tendermint and generated with [Starport](https://github.com/tendermint/starport).

{% embed url="https://github.com/akhirachain/akhiranode" %}

## Command Line Interface

`akhiranoded` is for launching the node and manipulating node related files, e.g. adding accounts into `genesis.json`.

Chain data, consensus key, node key and configuration files will be stored in `.akhiranoded` folder, default location is `$HOME/.akhiranoded`

`akhiranoded init` Initialize private validator, p2p, genesis, and application configuration files `

`akhiranoded collect-gentxs` Collect genesis txs and output a genesis.json file

`akhiranoded migrate` migrate Migrate genesis to a specified target version `

`akhiranoded gentx`gentx Generate a genesis tx carrying a self delegation `

`akhiranoded validate-genesis`validate-genesis validates the genesis file at the default location or at the location passed as an arg `

`akhiranoded add-genesis-account` Add a genesis account to genesis.json `

`akhiranoded debug`Tool for helping with debugging your application `

`akhiranoded start`Runs the full node `

`akhiranoded unsafe-reset-all` Resets the blockchain database, removes address book files, and resets `priv_validator.json` to the genesis state

`akhiranoded tendermind` Tendermint subcommands for export state to JSON

`akhiranoded version` Print the current version of akhiranoded `
