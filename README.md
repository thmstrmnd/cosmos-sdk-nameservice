# Ignite/Cosmos Nameservice Tutorial

BuyName
SetName
DeleteName

🙂 Created account "alice" with address "cosmos1ql23mw0krw9p7eevt9fje6v3xg535z4vyxyfys" with mnemonic: "hen shock wrong neck small candy chuckle cupboard sail tourist famous fish return tennis work crawl report hard huge dirt then raise wire unaware"

🙂 Created account "bob" with address "cosmos1lfsaerjc9ly2pgfy5h073swmc2txj96stkslrk" with mnemonic: "poverty original remain weasel author daughter survey hub over gentle casino knock tray add fork base dentist essence middle tool lion rack fame immense"

🌍 Tendermint node: http://0.0.0.0:26657
🌍 Blockchain API: http://0.0.0.0:1317
🌍 Token faucet: http://0.0.0.0:4500

## Test Your Blockhchain
* Run your blockchain where -r flag erases all the prior state
    ```
    ignite chain serve -r
    ```
* Buy a new name
    - must be greater than 10token
    ```
    nameserviced tx nameservice buy-name foo 20token --from alice
    ```
* Query the chain for a list of names
    ```
    nameserviced q nameservice list-whois
    ```
* Set a value to the name
    ```
    nameserviced tx nameservice set-name foo bar --from alice
    ```
* Buy an existing name
    ```
    nameserviced tx nameservice buy-name foo 40token --from bob
    ```
* Query the bank balance
    ```
    nameserviced q bank balances $(nameserviced keys show alice -a)
    ```
* Test an unauthorized transaction (should produde an error message)
    ```
    nameserviced tx nameservice set-name foo qoo --from alice
    ```

