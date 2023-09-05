# README


## Proposed Structure

This is just for purposes of demonstration. Clients can modify this as they see fit.

In this example, end users/clients are allocated a directory. Two subdirectories exist within the aforementioned directory. They are:

1) conf
2) assets


As their names implies, the configuration YAML would be placed in the former, and any associated assets in the assets directory.

This would be cloned, whereupon logic to obtain the diff (additions/updates) would be run. Finally, the script (as found in the image) with the conf flag pointing to the cloned yaml file would be run.

As an example:

1) Clone on above repo
2) Obtain diff (assume new additions were Marwan/conf/conf.yaml and Marwan/assets/asset.yaml)
3) Downstream Tekton task (or step) to copy (retaining directory structure)  the above files (from, say, a shared workspace) and run the main file.
4) (Optional): Notification informing user completion of automation. For instance, a Slack Notification task.

## Note

Jianbin and Rutvik: Please feel free to modify this as you see fit. The above is just an example.
