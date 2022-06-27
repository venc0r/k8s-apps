## Split install yaml into parts:

install download yq from github:
```
 wget https://github.com/mikefarah/yq/releases/download/v4.25.3/yq_linux_amd64 -O ~/.local/bin/yq && chmod +x ~/.local/bin/yq
```

## Split document into files with the names based on its values in the given keys

```
yq install.yaml -s '$index + "__" + .kind + "_" + .metadata.name'
```
in pwsh the double quotes must be doubled

The cdr files don't get the correct file name.

