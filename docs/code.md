
## General Principals

Cyqur is a Chrome extension and is governed by the rules of what an extension can and cannot do. All the javascript code is held in the public domain such as this website or a repository.


https://github.com/Binarii-Labs-Products/cyqur-0.0.0.1-production/

As with most code, there are always ways to improve its speed, redundancy and security and upgrades with aim to follow community best practice. 

There are no third party libraries such as jquery or calls to CDNs and if there is any code with MIT or other licence notifications they are prominently disclosed. However, if there is integration with cloud providers or token providers, we aim to disclose how this interaction works. We also aim to create threat models to help users understand their own risk appetites.

The code is minified and can be unminified easily. There is no obscurification.
The encrypted secret saved to the Vault is in JSON format. The secret is encrypted as a name / value. The JSON is also encrypted. 

#### Storage

Certain data is stored in the Browser. This can be in hidden fields on the webpage; session Storage; local Storage; local IndexedDB; Cookies (although Cyqur does not use Cookies). 

No data is sent to a server or requested from a server. The only exception is where a token has been given to the user for the purposes of being able to backup fragments to other services along with tokens issued for usage of the app. Third party cloud service providers may also be used to store and for retrieval of fragmented secrets.

The Vault uses the IndexedDB storage. Local Storage is used for faster interaction and as a cache.

#### Wipe Everything

In Settings, the Wipe Everything deletes all the browser data. However, the indexedDB may be open and may not delete properly so it is advised the app and Browser are closed down and then reopened.

Example LR00 is Localstore containing Raw data (encrypted) where 00 = full packet of all fragments; 01 = fragment 1; CR00 - C represents the fragment is stored on a cloud and a url is available. On decryption, a JSON object with have the D and MD. The integrity of the packet can be established by Encrypting the Data and TS and proving PUK. Local database uses the PUK as an index. The local storage is used as a temporary cache. This is currently raw JSON text.


## White Paper


#### Summary
Encrypt and decrypt data strings. Fragment and cloud scatter. Record locations. Index on a blockchain. Transmit to COLR. Backup. Import. Delete audit trail.

#### Glossary

D = Raw data / plain text
ED = Encrypted Data / cipher text
MP = Main Password
AP = Alternative Password
MD = Meta Data which includes
TS = date and time stamp when encryption was made
TG = Tags or keywords describing what is in the secret
PUK = Public Key
BPUK = Blockchain Public Key
H = Internal hash
E = Encoding of the data such as base64 with URI encoding for non Latin1 character sets
EP = Encryption Algorithm used (e.g AES-GCM)
NORF = Number of real Fragments
NOF = Number of real and spoofed Fragments (for later use)

#### Calculations

NORF = 10
FD = D + MD in JSON format. 
ED = Encrypt(FD, MP/AP, EP). 
PUK = sha256(ED + TS) implies low collision. 

L = Localstore. L records ED and fn = ED/NORF fragments. 
I = Local database used for searching purposes
LR00 = Local Raw Full Packet
LRnn = Local Raw Packet
LR0X = Local Raw Packet where X=A or B or C
CE00 = Cloud Encrypted Full Packet using Double Password
BC?? = Blockchain related meta
BCBC = Blockchain / Protocol
BCTX = Transaction Hash


#### Actions and Events

##### View

Expand into own tab
Open in View
Enter in secret
Enter password
View decrypted secret
View meta data

##### Sign In

Change language
Enter Main Password
Alert: Logged on
Alert: Cross indicates must add password to access
Alert: Internet access is off / on
New password must have > x characters
Enter token
Alert: Token accepted
View Help

On successful logon:

##### Add

Select template option

1. General:
Override password with different password
Generate random password
Enter tags / keywords / title
Enter secrets
Check > x characters
View real time encrypted raw data
Start Over
Secure
Alert: Progress including cloud scattering
Alert: Close other tabs if using Cyqur
Alert: Success / Failure
Alert: Number fountain on Vault

2. Seed Phrases:
Enter twice and color validation

3. Import Packets:
Drag or select backup cyqur-backup-settings.txt
Drag or select packets
Alert: Number of fragments vault has

Proof of secret
Blockchain or other public repository put / write

Vault
View secrets in vault
Update tags (encrypted tags not changed)
View each encrypted fragment
Copy fragments
View packets (raw, full, clouded)
Download packets as text files
Delete from vault
View secret

Settings
Enter cloud settings
Data - backup to text file
Data - wipe everything (vault, log files, cloud settings, local cache)
View log files
