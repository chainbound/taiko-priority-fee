# Taiko Priority Fee Analysis

## Analysis
The analysis can be found in [`main.ipynb`](main.ipynb). Make sure you select the correct Python environment in the top right corner (from the virtual environment).

## Running / Replicating

Replicating this analysis requires [mise](https://mise.jdx.dev/getting-started.html#installing-mise-cli). On MacOS, use `brew install mise`.

After that, initialize the environment and install dependencies:
```
mise i
mise r init
```

Collect proposals, mainnet basefee and mainnet transactions if not present (can configure params in [`mise.toml`](mise.toml)):
```
mise r collect-proposals
mise r collect-mainnet-basefee
mise r collect-mainnet-txs
```


## Optimizing Settlement
- Pack calldata better
- Remove `BlockParams[] blocks` from `BatchProposed` event (in `BatchInfo`)