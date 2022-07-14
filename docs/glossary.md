
## Terms we use

#### Actor
A person or legal entity. The Actor maybe the Owner Actor who controls the secret with the Main Password. A Bad Actor is an actor who wants to get hold of the secret. A Custodian Actor is a passive actor who may control access to the secret such as a Lawyer or Custodian.
#### Secret
A Secret is data that may have value such as the combination number to a safe, a credit card number or the private key to unlocking a public key. 
#### Offline
Offline is where Cyqur is used but where the device is not connected to the internet or any other network.
#### Custodian of Last Resort (COLR)
A COLR is an Actor that passively looks after fragments or fragments. There could be 1 COLR such as a lawyer or many such that they must engage in Thresholding to gain access to the Full Packet.
#### Risk Appetite
Risk appetite is usually a trade-off between ease of use and how damaging it would be if the secret was revealed. If the secret value is very high, then a low risk appetite could indicate the Actor would consider high fragmentation and very few if any trusted COLR.
#### Digital Assets
Secrets that have value such as private keys to digital asset wallets, or NFTs.
#### Blockchain / Distributed Ledger
A repository that records an index to a secret for purposes of proof of record and existence along with verification purposes
#### Fragmentation
Fragments are like pieces of a jigsaw. Cyqur breaks the encrypted secret into 10 parts. Depending on how these parts are stored and distributed, it makes it more difficult for a Bad Actor to find all the pieces. It also makes it more challenging when the Bad Actor does not have the completed picture and struggles to work out where the pieces go; if they have all the pieces; and if all the pieces are usable.
#### Packets
Packets are collections of Fragments. A Full Packet is a collection of all fragments. If the password is known, a Full Packet can be decrypted and the secret revealed.
#### Thresholding
Thresholding is the process of determining how many actors are required to recompile a Full Packet.
#### Double Password
Double Password is where the Full Packet has a different password to the password used to encrypt the fragments.
#### Cloud
The Cloud is any server or device that can store text files or representations of the contents of a packet. The cloud maybe operated by a third party e.g Azure or by the Owner Actor. It may also be a block on a blockchain. It may also be a portable drive. A paper Cloud is where the packet has been transcribed onto a piece of paper.
#### Encryption
Encryption is where a human readable secret (plain text) is scrambled into an unreadable secret (called cipher text) using a Password as the the key to lock and unlock. The default cryptography algorithm for Cyqur is AES-GCM which is an authenticated encryption mode that uses the Advanced Encryption Standard block cipher in counter mode with a polynomial MAC based on Galois field multiplication. AES-GCM is available in most browsers. It is anticipated more will become available in due course.

https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto/encrypt
#### Decryption
Using a password and a decryption algorithm such as AES-GCM to decode a secret.
#### Cloud Scattering
Cloud scattering is the process of putting file fragments onto various clouds. A controller keeps a record of the locations and the order the fragments must be appended together in.
#### Spoof Fragments
Spoof fragments are fragments that are not part of the full packet of fragments. They are a means to make it more difficult for Bad Actors to recompile the Full Packet.

