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

!(/main/assets/44935a765cd7eae93ac25.png)
