

## Access 

Cyqur can be accessed by adding an extension to a browser such as Edge and Chrome from the Google Chrome webstore. Alternatively, the extension can be added by unpacking the code in developer mode in the browser or using a Microsoft policy behind a firewall. It can also be used directly from the Cyqur website.

As an extension, it can be called vey quickly. For packet imports we suggest it is expanded into its own window as uploading files into an extension can be frustrating.

## Sign In

![Sign In](/images/login.png)

Sign In is where a Main Password opens up the vault of secrets and allows access to the Settings When secrets are encrypted, the default password used is this Main password. Secrets can be encrypted with alternative password if extra security is required.

If there is no Main Password or you do not want to use it, click the Plus icon. If you want to start over, click the Cross icon - this will delete the Main Password.

If you have set the "Always Keep Logged On" option on the Setting page to Yes then when you open Cyqur, all the icons will be shown and the default page will be the Vault. However it will not show or store the Main Password as raw text. You will need to reenter and it will then be recorded in the text field for future use.

The setting for keeping logged on is in Settings / Options. This ensures all the icons are available when the app is reloaded.

Cyqur logs the average time it takes to enter a Main Password and depending on the settings will delete all records if the key entry is outside this average. 

The Token field is populated by a 2FA OTP generator for further authentication. You will need to have created an account at Cyqur to obtain the tokens. A single token will use spent when a transaction hash is created on a blockchain as proof of record. For fragments, the number of tokens spent will depend on other factors not considered here.

If the token is correctly validated by the server, a message will show you how many days to expiry along with how many tokens you have used.

The number of items in the Vault is noted against the Vault icon.

#### Languages

Cyqur can be run under various languages - fields and notifications will appear in the language of choice. At present this documentation is in English but will be translated in the near future into other languages.

#### Internet

Cyqur is safest without internet access. If there is no internet, this will be notified in the app at the top of the screen. Note that without internet, blockchain access and cloud fragmenation will not occur.

## View 

Decrypted data:

![Decrypted data](/images/view1.png)

Meta data:

![Meta data](/images/meta1.png)

![Meta data](/images/meta2.png)

Pasting in the encrypted secret along with the password used to encrypt it will reveal the secret. Also revealed is meta data such as the original tags, a public key generated at the time the secret was created and a rehash to prove the public key is correct. It also reveals a timestamp, the encoding used and the cryptography method. Finally the raw JSON data is revealed.


## Add Secret

There are 3 add secret screens. The first allows you to enter or paste in a secret. The second allows you to record seed phrases (e.g Ledger Nano). The third allows you to import packets.

#### General Add
 
![Meta data](/images/meta1.png)

Enter the Tags or keywords that may identify what is in the secret. This is used and recorded in the meta data when the secret is encrypted. It is suggested that this these tags be renamed in the Vault to make it more vague as to what the secret is.

Enter or paste in the secrets (be careful when pasting as other applications may have access to the clip board)

Below the screen the encrypted data can be seen real time.

An entry as a transaction is created on a blockchain. It acts as an index, and with a timestamp and other immutable properties can be used to verify the secret.

When ready, click the Secure button. This will add the secret and all the fragments to the Vault. If you have set up cloud services, it will also add fragments to the cloud.


#### Blockchain

If an account has been created at cyqur.app, the public key will be registered and a transaction hash created on a blockchain (currently Ethereum, Solano and Zilliqa). This is a proof of record and also allows for validation of the secret.

The blockchain meta data can be viewed in the Vault.

#### One Tab Rule

If Cyqur is open in more than one browser tab, a prompt will appear to close down the other tab(s) so they can continue. Cyqur works best in one Tab if used in the browser.

## Add Seed Phrases

Many crypto wallets which self custody the digital assets, created seed phrases for recovery purposes. Cyqur allows you to record them and validate each seed word.

Below shows the live encryption as each key stroke is entered

![Adding Seeds](/images/AddSeeds.png)

## Packet Management

![Packet Management](/images/packetManagement.png)

Packets are JSON formatted text files that contain some or all of your encrypted secret. Packets are accessible via the Vault and can be downloaded as text files or, under the Fragments section, each encrypted raw fragment viewed and copied. Packets are JSON wrappers. A packet may also contain

The tags when created
The date and time the secret was encrypted
The unique identifier that groups similar packets together
Any cloud the packet has been uploaded to including blockchain
Any internal hash used to check the integrity and therefore proof of the secret
The encoding used (defaulting to base64) including the encryption algorithm used
This packet is for the first fragment (f1):
    
    "f1": "RHN4WWtJUFlaczkvaEhhjUdvaDNRZERpTXBiZ3ZTcEF3S2hpOVdEM3E1RndaMElhOFBVY2NZMFdhSE5MZXF3aGZwZU44azdWc1BFcDRONnBX",
    "f2": "",
    "f3": "",
    "f4": "",
    "f5": "",
    "f6": "",
    "f7": "",
    "f8": "",
    "f9": "",
    "f10": "",
    "hash": "",
    "puk": "df4567f90ebe37d6bfd2dd3ad2c97c4171f5b5161j465db3cb888aa397727530",
    "tags": "",
    "text": "",
    "cloud1": "no",
    "cloud2": "no",
    "cloud3": "no",
    "timeStamp": 0  

This fragment has no timeStamp or tags or details of cloud activity. This means it is impossible to ascertain what this secret may contain and when it was created. The tags and the timeStamp are encrypted along with the secret.

#### Full Packet
A full packet contains all the fragments and meta data such as tags and timeStamp. If it is imported into Cyqur, and the correct password applied, the JSON format will look like something like this:
    
    "secret":"M1lSeUxoaCUyRmkyc0JHa1JrdjRYNnIxaVF4cnR3QXZ6bDV3OUtqcDlQQWk2eGdPQzV0NWslMkY4TldJY1ZaZ3QzTjJ0dmRYJTJGSkZJcW5hJTJGWjdqZUdjJ4NlNWNUFEcWQlMkI2RGZrNlVpZW5VdGdvV0I1WEJXMTN4Q3ptclAwek9FYno3d3dZUThiN2FpVksyMUQ5eDFGVUZXJTJCM0ZjRGxjcSUyRkFoc1M4T0hONDhUJTJCVXNhcmdUeHo0Nm5jJTJGMkZrNnVBWmpocFBmV2xyciUyQm1VM3VReTVod21RZVdxWW9QZWkxd0R6MlBSa244ZnhaJTJCa1J0UEg2U3IxcFJmSSUyQlVrRzdD",
    "tags": "credit card banko2",
    "puk": "a249a2053ca4e80c96ada1ecb3503cc4c7396140743e71c466ec274b1a7af075",
    "meta": "1650900007860",
    "encoding": "base64 AES-GCM"
    

Another round of decryption on the secret / value will reveal the secret. The puk is recalculated against that stored internally to ensure the file has not been tampered with. The meta is the millisecond timeStamp in UNIX format.

#### Single Packet

A single packet, as above, contains details of 1 fragment and its location in the chain of fragments.

#### Packets (ABC)

Packets A,B and C contain groups of fragments.

Packet A contains fragments 1,2,3,8,9,10 
Packet B contains fragments 4,5,6,7,8,9,10 
Packet C contains fragments 1,2,3,4,5,6,7

These are used with COLRs. 3 Custodians, each with a packet. If they Full Packet needs to be created, only 2 Custodians are required. This is called Thresholding.

For Threat Models where many COLRs are required, a matrix can be created to create the Minimum and Maximum number of COLRs ever needed.

#### Import Process

On the Add page, Packet files can be imported (dragged and drop or from file systems). The number of fragments that Cyqur needs is 10 and it will highlight how many packets it currently has. When it has 10, it will try and decrypt using the Main Password. If an Alternative Password was used, then this must be entered.

#### Packet Storage

In Settings a full backup to a text file can be executed. This can imported into Cyqur using the Import Process.


## Backup

![Backup](/images/backup.png)

In Settings, Data the full internal storage can be backed up to one file. Cyqur can then be wiped clean.

#### Restore

To restore after a wipe, create a Main Password as usual and in Add select Import Packets. Upload the backup file ensuring the file name has not changed (Cyqur checks the file name and not its contents). Click upload and the Vault should be populated with the backup.

Note the backup does not currently backup cloud locations.

## Vault

![Vault](/images/vault.png)


This is where encrypted secrets are stored. They are held within the browser and not on your device or at a server.

Each secret can be Deleted from the browser. This is permanent and you cannot recover unless you have saved Packets. You will need all 10 fragments to recover.

Click on the open envelope icon to reveal the secret (with the correct password).

Click on the Encryoption to view the creation id, the encrypted secret ...

![Vault encryption](/images/vault-encryption.png)

Click on the Packets. You can download a full packet, a combination or individual packets. You can also down external packets (where the fragment has been saved to the cloud)

![Vault packets](/images/vault-packets.png)