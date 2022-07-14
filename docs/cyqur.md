
# Cyqur

## Overview

Cyqur is a simple but powerful encryption and decryption app. 

Cyqur facilitates the storage and transmission of data asset secrets.

Key features include:

1. In Browser Offline storage of digital assets
2. Fragmentation of the encrypted secrets
3. Cloud scattering
4. Creation of a transaction hash on a blockchain
5. Custodian of last resort
6. Full code transparency
7. Minimal code exposure to third parties
8. Serverless as far as possible
9. Zero knowledge as far as possible

Cyqur uses a Main Password to encrypt your secret data and then allows you to unencrypt (or decrypt) the same data with the main password or another password. It uses browser cryptography and aims to minimise exposure to third party code or services and the key features work offline for added security.

Cyqur also fragments the encrypted secret and allows you to download these and forward to trusted parties such as lawyers, custodians and trustees. This means in an event where you are no longer able to access your secrets, these trusted third parties (we call them Custodians of last resort or COLR) are able to collectively recompile your encrypted secrets. Unlike password managers that store the data on the device and often a server too, Cyqur stores all your data in the browser. Password managers often scan the active tab of your browser for password and logon text boxes and fill or grab the data and often store all your passwords on your device, tucked away, such that it can be accessed at anytime; Cyqur keeps things simple.

Since your Cyqur data is secured in the browser, you can delete part or everything at the click of a button. This leaves no audit trail and there is no way to recover. However, if recovery is important then you can download the packets and store in a password manager, email, cloud or elsewhere. This contains your encrypted data so if the full packet is compromised the actor would need the password to access the data. If you stored the partial packets then a bad actor would need to have access to the location of all the packets along with the password to reveal the secret.

## Use Cases

Use Case 1:
Simple encryption and decryption.

You enter some data and a password and the encrypted data appears. This encrypted data can be copied and texted to someone else. If they have the password, they can decrypt the secret using Cyqur. 

Use Case 2: 
Storing a secret that has value if lost or misappropriated (e.g seed words to a crypto wallet).

You follow these steps: Use a browser with no other extensions installed Turn off the internet Open Cyqur and enter a memorable password Enter the secret Download the full packet Store the full packet in your local folders (not ones that are auto stored on iCloud, Dropbox or other helpful cloud service) Wipe eveything (settings) Close and reopen the browser Turn the internet on and email or message the encrypted package 

Use Case 3: 
Fragmenting the secrets, distributing and hiding. 

Once cloud settings have been provided, the encrypted secret is cut into 10 parts and distributed across the cloud. A packet records the location. The packets are then distributed to interested parties. This means all the Cyqur data can be deleted as the fragments will be held on the Cloud.


