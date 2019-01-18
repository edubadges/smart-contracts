An easy option is properly using the validana-cli (https://github.com/DvdGiessen/validana-cli). A user interface is still on the planning.
Attached are the contracts in json format, as expected by the validana-cli.
Start by creating the institution and then the entity contract.


*Example usage:*</br>
Make sure to update the url, prefix and signing key to that of the processor.

```javascript
validana-cli contract create --url wss://edubadges.com:8080/api/v1/ --prefix edubadges --signing-key KyJPCoYvgXaNpvTPshw52Nu5HyHq9jrUGmoCSkEvjbTgyQPWkJX5 --contract-file "path/to/contract/URL.json"
```

(Optional) 
```javascript
validana-cli transaction await --url wss://edubadges.com:8080/api/v1/ --prefix edubadges --id b043790915bc2f9b6bf8ae470f49c32d
```

Once all contract are created change call the url contract with the rest url of the server, e.g.:

```javascript
validana-cli contract execute --url wss://edubadges.com:8080/api/v1/ --prefix edubadges --signing-key KyJPCoYvgXaNpvTPshw52Nu5HyHq9jrUGmoCSkEvjbTgyQPWkJX5 --contract-type URL --payload '{"url":"https://edubadges.com/api/v1/"}'
```

(Optional) 
```javascript
validana-cli transaction await --url wss://edubadges.com:8080/api/v1/ --prefix edubadges --id b043790915bc2f9b6bf8ae470f49c32d
```
