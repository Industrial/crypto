# Crypto
This project documents the safest way to generate, store and use cryptocurrency wallets.

Many cryptocurrency wallets and password managers that did not think the problem through very well will generate secret values for you in plain text and then ask you to write them down on a piece of paper. This is a terrible idea because it leaves your secret values vulnerable to theft and loss.

Instead of using a plain text input field to generate a secret into, we will use a password field that uses asterisk/dots to obscure the secret along with a copy button to copy the secret to the clipboard. This way, we can generate, store and use the seed phrase and private key safely.

We create a program that is just a plain HTML file so that anyone can download it and use it on their air-gapped device. An air-gapped device is a device that does not have any internet access.

Say you have two phones, phone A and phone B. Phone A has internet access and phone B does not. Phone B is the air-gapped device. You use a wallet application on both phones and whenever you want to create a transaction, phone A's wallet generates a QR code which can then be scanned and approved by phone B's wallet that in turn generates a confirmation QR Code. Phone A now scans that QR code and then the transaction is made (through the internet connection of phone A).  This way, phone A and the north korean hackers on the internet that might hack phone A will never be able to access the secrets stored on phone B and your crypto will forever stay safe, even if you get really rich and have a gazillion coins on that wallet. My advice is to put phone B in a bank safe that is guarded and to use it as an actual bank account.

This covers all possible attack vectors. Please correct me if I am wrong.

## Step by Step Guide

### Phone B
1. Buy a Google Pixel phone. These are easy to customize and put a different operating system on to.
1. Replace Android with GrapheneOS. Download and install GrapheneOS on the phone. Please refer to the [GrapheneOS website](https://grapheneos.org/) for instructions.
1. Download the HTML file in this project.
1. Download [KeePassDX](https://keepassdx.com/) and install it on the phone.
1. Download a wallet application that specifically supports both the QR Code functionality and pasting the seed phrase or private key into the wallet. I recommend the app [AirGap Vault](https://airgap.it/vault/).
1. Disconnect the phone from the 5G, Wifi, Bluetooth, NFC and any other connections. Put it in flight mode.
1. Generate the seed phrase and private key using this HTML file in the browser.
1. Copy the seed phrase and private key into the password manager.
1. Create a new wallet in Airgap Vault using the Private Key or Seed Phrase.

### Phone A
1. Download and install the companion app (to AirGap Vault) called [AirGap Wallet](https://airgap.it/wallet/) on Phone A.
1. Pair your AirGap Wallet on Phone A with the AirGap Vault on Phone B by scanning the QR code presented on Phone B in the Airgap Vault app.

That's it. You are all set.
