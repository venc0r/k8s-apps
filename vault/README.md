## After applying the application.yaml the vault must be initialized and unsealed

# Init: just run the following command in the vault pod
```
kubectl exec -it -n vault vault-0  -- vault operator init
```

# Unseal: you have to pass +3+ unseal keys to the vault pod
```
kubectl exec -it -n vault vault-0  -- vault operator unseal <unseal_key>
```

