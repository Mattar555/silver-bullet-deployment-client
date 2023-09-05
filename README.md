# README


## Proposed Structure

This is just for purposes of demonstration. Clients can modify this as they see fit.

In this example, end users/clients are allocated a directory. Two subdirectories exist within the aforementioned directory. They are:

1) conf
2) assets


As their names implies, the configuration YAML would be placed in the former, and any associated assets in the assets directory.

This would be cloned, some logic to obtain the diff (additions/updates) would be received, and the script with the conf flag pointing to the cloned yaml file (which implicitly points to the cloned assets - it is important the directory structure be retained appropriately)

As an example:

1) Clone on above repo
2) Obtain diff (assume new additions were Marwan/conf/conf.yaml and Marwan/assets/asset.yaml)
3) Next Tekton task (or step) to copy the above files (from shared workspace say) and run the main file.

## Note

Jianbin and Rutvik: Please feel free to modify this as you see fit. The above is just an example.
