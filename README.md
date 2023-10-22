# INFINITE NUMBER OF MEMORABLE SEED PHRASES FOR COLD STORAGE
_This represents a genuine cold storage wallet, designed to safeguard your cryptocurrencies with the utmost security. Utilizing this system eliminates the vulnerability of potential hacking associated with 'hot' crypto wallets, the risk of malicious backdoors being embedded within software wallets, and the peril of losing physical devices like Tangem or Ledger, or exposing them to potential damage due to accidents._
 
_With this solution, your wallet addresses remain exclusively accessible within the ledger and blockchain, while you retain an unlimited supply of cryptographic keys stored securely within your memory. This not only guards against the event of your home succumbing to a fire or your computer falling victim to compromise, but it also ensures the preservation of your valuable crypto assets._

## INTRODUCTION
How can one generate an endless number of seed phrases while utilizing a straightforward recovery system? This utility caters to individuals seeking a secure method for safeguarding their cryptocurrencies without the necessity of accessing them online. The assurance of reproducibility is guaranteed owing to the inherent mathematical constancy of the generated output.

For the setup you will need 

• BIP30 tool: https://github.com/iancoleman/bip39/releases

• CyberChef: https://gchq.github.io/CyberChef/

• Live Linux: Fedora ( https://fedoraproject.org/workstation/download ) , Ubuntu, Debian, Kali or similar.

• A crypto wallet, available on Linux, such as OneKey ( https://www.onekey.so/ )

## STEP ONE: Linux boot
1) Create a live USB drive and boot your computer from it. 

2) Connect to the Internet. In the software depository search for crypto wallet and install the wallet you need. For instance, if you use only BTC, just install Electrum. Otherwise, you can use OneKey wallet for multiple currencies.

3) go to Ian Coleman BIP39 and download the repository.

4) go to CyberChef and download the repository.

Check now that you have downloaded 1) wallet 2) BIP39 tool 3) CyberChef

!!! YOU CAN ALSO DOWNLOAD ONTO THE SECOND USB DRIVE ALL THESE FILES (point above 2, 3 and 4) ONTO YOUR REGULAR MACHINE, INCLUDING THE WALLET APP, AND BY DOING THIS YOU NEVER CONNECT TO THE INTERNET WHEN USING LIVE MACHINE. !!!

&#x1F534; **From now you will DISCONNECT from the internet. You will NEVER connect it again during this session.** &#x1F534;
## STEP TWO: Create system of entropy seed and Wallet #1
We must generate seed entropy, and to accomplish this, we will employ CyberChef.

You are tasked with establishing a reproducible system, one that you can execute multiple times. The system should be something familiar to you but undisclosed to others. During this phase of the procedure, it is imperative that you meticulously write your chosen system onto paper by hand. Upon the completion of the wallet creation, the paper containing your system should be securely incinerated.

The system can use some known to you ideas for implementation such as:

• a book, you like the most.

• ISBN numbers of your top 3 books.

• phone numbers of your family members,

• chemical formulas

• engine numbers of Mercedes E class

• MIDI numbers of a musical piece.

Below will use a book to create 3 hashes, flush it through AES encryption, and make one numbered final hash.
### A) Creating a seed entropy by using a book. 
We will use New King James Bible of 1611 to create our first seed entropy.

&#x1F534; **Please, do not use the same book. It is possible that it can be used by quantum computers in the future. Use an obscure book you like. Be very careful that you don't make any typo. Try the system twice: once following this tutorial, and once making your own seeds.** &#x1F534;

Open CyberChef twice in two separate tabs or windows.

Under Hashing find Keccak and add to the ”Recipe”.

Choose size 256.

<img width="1222" alt="44935a765cd7eae93ac25" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/e3308602-2f31-4eeb-8ff0-60dc767d9ba0">


In the input window enter the first phrase of the Genesis 1:1:

`In the beginning God created the heaven and the earth.`

<img width="1227" alt="69145b7d2a96646c45077" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/759954a3-9626-4ffe-95ab-6f73c7fd368d">

#### &#x1F534; WARNING: The entered text must be completely identical. Nothing now can be approximate. A text without period dot is not the same as with dot. A text with an extra space on the end is not the same as without an extra space. The computer reads all information. So "earth" is not same as "Earth". It must be 100% identical input. Even a small difference gives you a totally different output. &#x1F534;

Click then on "copy to clipboard":

<img width="215" alt="f831cf3cc488566a26260" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/af4f413e-d662-4ee8-9979-92fe0125aea9">

Go to new CyberChef window and insert a new recipe "AES Encrypt"

<img width="1227" alt="fc5a058390cc5727c320b" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/4515ee32-6738-41a1-8866-475070533f67">

Make sure that it is CBC mode and all selected are HEX:

<img width="344" alt="f074a99ef46b273c86386" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/7e0c8b2e-82f0-4908-974a-1f332cefb7a5">

Now, paste the copied text 
`950b5cfa2facafab5c5bb71b86856832be322262e69eb4025fc170b58aeed2b8` 
from the previous window into the input window:

<img width="633" alt="5b37c0172a3a5806f50d8" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/ba26e506-fe7c-4e9d-aea1-fc3f7af1f7a7">

Now, go to the first CyberChef window and instead of the Genesis 1:1 enter content of 1:2:

`And the earth was without form, and void; and darkness was upon the face of the deep. And the Spirit of God moved upon the face of the waters.`

<img width="985" alt="f2405952c3095811b7302" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/04b4b2c0-6823-465b-96ce-e360dd02a93b">

Copy the output 
`bf8cfd392cbce445e528c00028f62ffe59b2de4b23b9d6a17759383e7d5bcec9` 
and paste it into the second CyberChef window as "key":

<img width="346" alt="035a93abc012825f993db" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/13b16f04-b589-4818-9f70-fca0585faeed">

Now go to the first CyberChef window and insert Genesis 1:3:

`And God said, Let there be light: and there was light.`

Copy the text from the output again 
`8bc6485b22aeda0ea18c2695d64ee1831a610da3afef78e98f77340b471919f9` 
and insert it into the second CyberChef window into IV:

<img width="345" alt="98dee238f4ef5626f77d6" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/1d1202af-83ac-4bd7-8a50-c419944ebafb">

Finally you will get the following result in the output
`bef75166f4633c8dc060b26871cd2b74803ae2bbfa25869fed14932a4e36d8e6b3b7ab0317574388be127d3bc7615a19`

<img width="980" alt="9ab6c1fb4cf7a7702fc8b" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/37561952-d2b5-48d0-88cf-5b4197fe2208">

In order to make an infinite number of the seeds (thus also wallets) we will flush it with MD2 hash with numbering ("rounds" or "passes"), **before** the AES encryption. Under "hashes" find MD2 and enter it before AES Encrypt:

<img width="394" alt="3d99e63eff6ffdcf954d9" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/015fc621-f8fd-4cac-8c29-943f3c8e938c">

Change number 18 into number 1 (but you can start with another as the #1 wallet, for instance year of your birth, in that case type 1980 or so, but here the example shows "1"):

<img width="371" alt="e1a5fcf7723a84e53648c" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/9e7b74b7-80bc-4ced-98c7-a856369ce995">

So this will be used to generate our FIRST seed, or the first wallet. The final output looks like this:

`86793e0d01c7169f8e0be36f0d1f01eba783d53368ad2ed921449997db6c154d`

<img width="977" alt="d799f6bfcb5a0a0acc94f" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/27ddd4e9-060c-45a6-baaa-f99a86eba5df">











