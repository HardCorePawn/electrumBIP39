# electrumBIP39
Version of the BIP39 Mnemonic Code Converter that works with Electrum Seeds

1. Enter your Electrum seed at the top in the "BIP39 mnemonic" section (WARNING: NO checksum calculation is performed!)
2. Click the "BIP32" tab in the "Derivation Path" section.
3. Set "Client" to "Custom Derivation Path"
4. Set the "BIP32 Derivation Path" to m/0 for "receive" addresses (addresses/keys displayed at bottom of page)
5. Set the "BIP32 Derivation Path" to m/1 for "change" addresses (addresses/keys displayed at bottom of page)


You should probably download the .html and run it offline. I copied .html from https://github.com/iancoleman/bip39 and it seems "OK", but I haven't fully vetted the code and make NO promises that it doesn't contain any backdoors etc.

Run at your OWN risk.

CREDITS: All credit goes to Ian Coleman https://github.com/iancoleman

Basically, I just copied his very useful BIP39 Mnemonic Code Converter and hacked it to work with an Electrum seed (removed the BIP39 checksum calculation, so make sure you type the seed properly! :P and I changed the default BIP39 passphrase from "mnemonic" to "electrum" as per the Electrum code). 

I forget exactly where I found that Electrum uses m/0 and m/1 derivation paths, it was on a StackExchange thread I stumbled across.
