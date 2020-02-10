# Vault

* `vault status`
* `export VAULT_ADDR=http://0.0.0.0:8200`
*  See `Root Token` for `VAULT_TOKEN`
*  `vault login` then input token
   or
   browser to `http://localhost:8200`

## Write a secret
* `vault kv put [storepath]/[keyname] key=value`
* `$ vault kv put secret/coffee recipe=42`

