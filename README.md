# electrumBIP39
Version of the BIP39 Mnemonic Code Converter that works with Electrum Seeds

## **For "Legacy" seeds/wallets:**
1. Enter your Electrum seed at the top in the "BIP39 mnemonic" section (WARNING: NO checksum calculation is performed! TRIPLE check you have entered your mnemonic correctly mmmKay?)
2. Click the "BIP32" tab in the "Derivation Path" section.
3. Set "Client" to "Custom Derivation Path"
4. Set the "BIP32 Derivation Path" to m/0 for "receive" addresses (addresses/keys displayed at bottom of page)
5. Set the "BIP32 Derivation Path" to m/1 for "change" addresses (addresses/keys displayed at bottom of page)

## **For "SegWit" seeds/wallets ("bc1" aka bech32 addresses):**
1. Enter your Electrum seed at the top in the "BIP39 mnemonic" section (WARNING: NO checksum calculation is performed! TRIPLE check you have entered your mnemonic correctly mmmKay?)
2. Click the "BIP141" tab in the "Derivation Path" section.
3. Set the "Script Semantics" to P2WPKH
4. Set the "BIP32 Derivation Path" to m/0'/0 for "receive" addresses (addresses/keys displayed at bottom of page)
5. Set the "BIP32 Derivation Path" to m/0'/1 for "change" addresses (addresses/keys displayed at bottom of page)


You should probably download the .html and run it offline. I copied .html from https://github.com/iancoleman/bip39 and it seems "OK", but I haven't fully vetted the code and make NO promises that it doesn't contain any backdoors etc.

**_Run at your OWN risk!!_**

CREDITS: All credit goes to Ian Coleman https://github.com/iancoleman

Basically, I just copied his very useful BIP39 Mnemonic Code Converter and hacked it to work with an Electrum seed (removed the BIP39 checksum calculation, so make sure you type the seed properly! :P and I changed the default BIP39 passphrase from "mnemonic" to "electrum" as per the Electrum code). 

I forget exactly where I found that Electrum uses m/0 and m/1 derivation paths (for Legacy wallets), it was on a StackExchange thread I stumbled across. I figured out that Electrum had an extra "script type" value in the path for SegWit stuff by looking at the Electrum source code (hence the extra **0'** in the SegWit derivation path)
