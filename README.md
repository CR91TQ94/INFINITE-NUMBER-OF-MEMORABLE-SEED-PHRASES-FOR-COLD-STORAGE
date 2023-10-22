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

---
> [!WARNING]
> &#x1F534; **From now you will DISCONNECT from the internet. You will NEVER connect it again during this session.** &#x1F534;
---

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
### A) Creating the seed entropy by using a book. 
We will use New King James Bible of 1611 to create our first seed entropy.

---
> [!WARNING]
> &#x1F534; **Please, do not use the same book. It is possible that it can be used by quantum computers in the future. Use an obscure book you like. Be very careful that you don't make any typo. Try the system twice: once following this tutorial, and once making your own seeds.** &#x1F534;
---

Open CyberChef twice in two separate tabs or windows.

Under Hashing find Keccak and add to the ”Recipe”.

Choose size 256.

<img width="1222" alt="44935a765cd7eae93ac25" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/e3308602-2f31-4eeb-8ff0-60dc767d9ba0">


In the input window enter the first phrase of the Genesis 1:1:

`In the beginning God created the heaven and the earth.`

<img width="1227" alt="69145b7d2a96646c45077" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/759954a3-9626-4ffe-95ab-6f73c7fd368d">

---
> [!WARNING]
> &#x1F534; **WARNING: The entered text must be completely identical. Nothing now can be approximate. A text without period dot is not the same as with dot. A text with an extra space on the end is not the same as without an extra space. The computer reads all information. So "earth" is not same as "Earth". It must be 100% identical input. Even a small difference gives you a totally different output.** &#x1F534;
---

Click then on "copy to clipboard":

<img width="215" alt="f831cf3cc488566a26260" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/af4f413e-d662-4ee8-9979-92fe0125aea9">

Go to new CyberChef window and under section **Encryption** find and insert a new recipe **AES Encrypt**

<img width="1227" alt="fc5a058390cc5727c320b" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/4515ee32-6738-41a1-8866-475070533f67">

Make sure that it is **CBC mode** and all selected are **HEX**:

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
and paste it into the second CyberChef window as **key**:

<img width="346" alt="035a93abc012825f993db" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/13b16f04-b589-4818-9f70-fca0585faeed">

Now go to the first CyberChef window and insert Genesis 1:3:

`And God said, Let there be light: and there was light.`

Copy the text from the output again 
`8bc6485b22aeda0ea18c2695d64ee1831a610da3afef78e98f77340b471919f9` 

and insert it into the second CyberChef window into **IV**:

<img width="345" alt="98dee238f4ef5626f77d6" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/1d1202af-83ac-4bd7-8a50-c419944ebafb">

Finally you will get the following result in the output
`bef75166f4633c8dc060b26871cd2b74803ae2bbfa25869fed14932a4e36d8e6b3b7ab0317574388be127d3bc7615a19`

<img width="980" alt="9ab6c1fb4cf7a7702fc8b" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/37561952-d2b5-48d0-88cf-5b4197fe2208">

In order to make an infinite number of the seeds (thus also wallets) we will flush it with MD2 hash with numbering ("rounds" or "passes"), **before** the AES encryption. Under "hashes" find MD2 and drop it before AES Encrypt:

<img width="394" alt="3d99e63eff6ffdcf954d9" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/015fc621-f8fd-4cac-8c29-943f3c8e938c">

Change number 18 into number 1 (but you can start with another as the #1 wallet, for instance year of your birth, in that case type 1980 or so, but here the example shows "1"):

<img width="371" alt="e1a5fcf7723a84e53648c" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/9e7b74b7-80bc-4ced-98c7-a856369ce995">

So this will be used to generate our FIRST seed, or the first wallet. The final output looks like this:

`86793e0d01c7169f8e0be36f0d1f01eba783d53368ad2ed921449997db6c154d`

<img width="977" alt="d799f6bfcb5a0a0acc94f" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/27ddd4e9-060c-45a6-baaa-f99a86eba5df">

### B) Creating the seed from the entropy.

_In CyberChef we have created a long string of numbers and letters called a hex string. We will use it to create our seed. 
_
Copy the output from CyberChef second window `86793e0d01c7169f8e0be36f0d1f01eba783d53368ad2ed921449997db6c154d` and go to Ian Coleman BIP39 tool page.

<img width="976" alt="6b582213c67b7e3706e55" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/b2a5f9d0-832a-4e07-b3e0-99885d4b012a">

Click on **Generate** to initialize (don't worry it stays 15 words):

<img width="598" alt="48555fa276352f4f35e70" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d31c83aa-2f27-425c-b6f2-c10f66e8c9bd">

Now, click on **Show entropy details**

<img width="195" alt="80837af274b66d9b41ecd" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/b91cd052-b771-4bff-ac1f-4815e956f4b9">

When ckecked, a new field above called **entropy** will open. Select the text inside of the field and delete it. Next, paste the text you copied from CyberChef `86793e0d01c7169f8e0be36f0d1f01eba783d53368ad2ed921449997db6c154d`:

<img width="854" alt="92daf5bcff3e238297684" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/b927815c-bec6-432c-b56d-d5194f0b7e66">

**IMPORTANT: Select 24 words as mnemonic length (or 12 if you prefer, here 24):**

<img width="647" alt="24b2dab7651ae152029f4" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/aa018d11-5e52-41ce-a5ee-6f5d800a44b6">

Finally we have got our 24 word mnemonic phrase:

<img width="951" alt="95a7d044ff74f22003926" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/c29f7da9-cc00-48a0-948e-8522f78983c9">

The phrase is:

`accident angry rent manage fade foot sudden beauty parade deal maple among learn affair plug slim high depth urge swarm swallow lazy camera gain`

This is your seed for the Wallet #1.

### C) Receiving addresses 

Now we can proceed to get information about our incoming addresses, the Bitcoin is already selected. Be sure that you use BIP44 derivation path:

<img width="275" alt="2a793d666cd72decf17c0" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/3b291c80-3db7-4865-aad1-53abf460d54f">

The Bitcoin is automatically selected, here is the address. Remember, do not change any other settings. Your first address (0, i.e. zero) is the correct first receiving address:

<img width="624" alt="f08dfc964ec75798d875d" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/94ce9bea-6be9-4013-a73e-32153ec1e25b">

Your BTC address is:

`1NWS1jfrtLSY2YwjNnLmWZkmtM2awuVeCY`

For other coins select the desired coin:

<img width="482" alt="8ffe6e89c2fc258e09761" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/664e5e20-407d-4909-bd98-dff8b4368e76">

Ripple/XRP:

<img width="640" alt="4687c8d75c6c2be0504df" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d96525d0-9a29-4c30-b22a-2540432266aa">

Ripple XRP address is:

`rQBWfyvfh1kMi5DFAdebUHKhTbWeEwpyin`

Ethereum:

<img width="699" alt="160c5a5689a8c3ae37071" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/8ff00f2d-e63a-402a-a061-d57a5a2b7c08">

Ethereum ETH (and other L2 addresses) is:

`0x5CCE7e6A7d2110B6ca93Ae572CDf173AfFFe0C36`

### D) VERIFY the addresses in the wallet.

We will use OneKey to import our seed and see if we get the same addresses.

---
> [!WARNING]
> &#x1F534; **REMEMBER: keep the computer offline all the time.** &#x1F534;
---

Open OneKey, start by importing a wallet using the seed:

<img width="276" alt="cf03ddc942572f2abb846" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/e794588b-3b6b-493c-8fb7-72baf232513f">

<img width="270" alt="f68dac89f8fb5c77f29b9" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/f991b81e-e222-42d0-a1e5-c0ce985ab153">

<img width="224" alt="25394329cd7b4da760e79" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/beebfe45-38a1-481e-b229-c15813d4a7ab">

And paste the seed you have generated in BIP39 tool:

`accident angry rent manage fade foot sudden beauty parade deal maple among learn affair plug slim high depth urge swarm swallow lazy camera gain`

#### Now we will see if we get the same addresses.
Click on Ethereum (here I am using online computer therefore the green dot. Because you use the offline computer, it will not be green and the icons will be missing, that is OK) and generate new address:

<img width="155" alt="1ddf4322932344bde0dba" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/c406bf44-0eb4-401c-b4ac-c108d2b15b74">

Click on Receive to see the address:

<img width="178" alt="84078a53385e18663695d" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/cc85342c-a26f-408d-b1cf-a6028a030982">

<img width="376" alt="a6d1b22f66c5551d9242e" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/197d9683-2fd1-4ee7-872b-ee511635d1e5">

**Good! It is the same address as in the BIP39 generator.**

Now check XRP. Click on the dropdown icon of the network and choose Ripple, and then Create account:

<img width="292" alt="a371fd1a404bd8e00e35d" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/973b0b5e-0a6d-495e-b7a3-e0b2e5294577">

Again, click on Receive to see the receiving address:

<img width="368" alt="37e36312e142285f00212" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/cc82e004-2f62-4db0-b4f0-529a7a80f4dd">

**Good! It is the same address as in the BIP39 generator.**

Now let us do the same with Bitcoin.

Choose: Legacy. Click again on "Receive" to see the address:

<img width="372" alt="5460f5e1ceeeb114683b9" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/ed47eaab-01d7-4c3a-9bf2-459c3ed6088d">

**Good! It is the same address as in the BIP39 generator.**

Now, if you want to use a newer type of the Bitcoin address, select NATIVE SEGWIT.

Click on the wallet dropdown:

<img width="330" alt="6c21ff64a09fc6e3cb558" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/9ec634d6-ab3f-4afa-95f8-1dcf0b12cdf2">

Click on +:

<img width="382" alt="2999e31d897767194619e" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/687ee27a-8349-4024-a7c5-c04233ffda0f">

Click on add account:

<img width="245" alt="34afa92e18d1521810c4d" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d4b14e83-a5e7-43e2-bc5b-a1ce7b8ee681">

Choose Native Segwit, and click on the Receiving address:

<img width="373" alt="32071716aa3808c41ccff" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/b4438636-621b-46b8-ac80-7cb7061a8cdf">

Well, this is an unknown address. How it can happen?

Go to your BIP39 generator.

Instead of BIP44 use **BIP84** as the Derivation path:

<img width="389" alt="8c70c387ccb7cb1a83505" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/e93258ca-d169-4374-9886-72047204b74d">

Well, this is the same address as in the OneKey wallet, so everything is good!!

<img width="689" alt="6aaf234049fddb026987e" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/b20124d2-586c-44c3-91d9-85e048c91963">

#### SYSTEM OF WALLETS
1. BTC uses BIP84 nowadays and you should use it as well.
1. All other coins use BIP44. Please check Coinomi's tool (fork of the Ian Coleman's BIP39 generator) for missing coins. Search for it.
1. Every coin wallet starts with derivation path that is 0 (zero). It is the FIRST wallet. You should use that address, but for the privacy reasons using a wallet "online", you can increase your privacy by using other addresses from the same wallet seed. However HERE WE WILL USE ONLY THE FIRST, because it will be our cold storage, and you don't need any privacy for that reason.
1. Some networks still don't have import function (Hedera's HBAR), so you cannot use your own seed, unfortunately. 
1. Some coins are not available in BIP39 tool (Quant or Kaspa). Still you can use your 24-word seed phrase to create wallets for these coins in their respective wallets. In order to do it you need to use a separate wallet app just for these coins. However, be sure that you should always enter your seed into an offline device to get the receive address and afterwards you will wipe the device without one second connected on the Interntet. For that purpose you can use numbered wallets for different coins. Read below now Step 4!

## Step 3: RECOVER THE SYSTEM
After you have got the receiving addresses for your crypto, and confirmed in the wallet they exist, try to repeat the same process once again. I will lead you through this process.

1. Reboot.
1. Boot to Linux Live
1. Go and download: wallet app (OneKey), CyberChef and BIP39 generator.
1. Go offline.
1. Repeat the process of getting the entropy for your seed, from your favorite poet:
   - Generate three Keccak hashes (HEX hashes), 256 size of the three verses. The longer the text - the better.
   - Create flow of AES encryption using CBC mode, the first hash above goes as the input, second as Key, third as IV.  
   - Check everything is HEX.
   - add MD2 with "round 1" before the AES encryption.
1. This output copy and go to BIP39 tool.
   - click Generate to initialize
   - click on "Show entropy details"
   - delete the current Entropy and paste your HEX from the CyberChef.
   - Choose 24 words length.
1. Verify that you have got the same seed.
1. If verification gives the same seed - you have succeeded!
1. Try again to import into OneKey the same seed. Check and verify if the addresses are the same. 
1. If yes, you can proceed by importing the receiving addresses into your phone. Just scan the receiving addresses in order to import in your phone wallet as WATCH ONLY.
1. Reboot normally.
1. You can send a small amount of your crypto to the new address. Check on the chain explorer if it is present (visible as received). Pay attention that it is the correct address you watch.
1. Repeat once again the process from 1.-11. and pay attention to the final receiving address. Is it the same? If yes, than good! Now you can send all your cryptos to the new addresses.

---
Finally, Our system looks like this:
<img width="977" alt="53d4591e0a7f588179154" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d3ca724e-e77b-4691-b2d1-2357c32ea399">
<img width="862" alt="135eb8b9c05d3e9325ca7" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/818d105d-7cff-48e3-abf1-da0d861699e0">

## Step 4: CREATING THE NEXT SEED for Wallet #2 and beyond
You can use the tool above to create your first wallet (seed). But maybe in 10 years, you will become rich and want to move your coins somewhere, or split to multiple wallets or similar. Once your wallet #1 is exposed online, it can be compromised. For that purpose you will use again a brand new Linux Live, you will create the new seed #2 and new wallet address #2.

For that purpose you will do exactly the same as above: creating it OFFLINE.
And you will choose **2** as rounds in MD2:
<img width="380" alt="d198d696e8250803d0e8b" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/7ae9866c-0a8c-4512-bffa-ae847c996a07">

This gives us a new entropy:

`88faec756a149c734f59e8e216ccfbe9bccc3bf5790c86b4c61306bcadb3f331`

<img width="1031" alt="dcd24ec68e0a5e8947585" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d4983915-2738-4a5c-9905-9d2bb06ff167">

And it gives us a new seed:

`fit basic slender engine mechanic amazing easily welcome rack flock bridge occur finish space little limb prison devote harsh enact lizard mechanic swallow love`

This wallet will be your new receiving address (Native SEGWIT):

`bc1qmnhyhl38tf3rcljt6k70t39wmytel2fvwchz2m`

---
So, if you have 100 BTC, and you want to move to an Exchange 10, and keep 90, do the following:

1. move 90 to your wallet #2 and 
1. 10 to the Exchange. 

So your wallet #1 will be now empty, and wallet #2 (never been online) with funds. Basically all wallets with funds will never go online. Once you wish to take it online, it is done 

a) on a brand new system, 
b) using a trusted wallet, 
c) you will move your funds always to the next offline wallet.

Basically, you can right now create all wallet addresses and give them names.

* Wallet #1: bc1q8vye7d7s46qwuvaxzgjem2yufj6n4vax8w6s0t
* Wallet #2: bc1qmnhyhl38tf3rcljt6k70t39wmytel2fvwchz2m
* Wallet #3: bc1qhkk0xn42yjya5rf4zkn8xfrtg7crjv4sjzcmdk
* Wallet #4: bc1qchn4w2j2xk3wzpc4ars48tg9qnurvpwcfehn9a
* Wallet #5: bc1qhdtnvsxzckczpfv04yl9w6e6228fz552dtfr6t
* ...etc.

Now you have the list of all receiving addresses and you can use it in this order.

---
> [!WARNING]
> &#x1F534; **Caution: It is imperative that you maintain the confidentiality and security of these incoming addresses. If your large funds are known, you might be attacked. Employ KeePass database or an encrypted text file, protected by a PGP key, to safeguard these addresses. While it may not pose an insurmountable issue if these encrypted files are lost, recreating them can be an arduous undertaking, particularly if it necessitates the repetitive booting into a Linux environment and executing the entire process. &#x1F534;
---

Act prudently by securing these addresses without delay, as this will enable you to effortlessly enter them into exchanges using a copy-paste method when acquiring your cryptocurrencies, facilitating their subsequent transfer to your cold storage wallets.

## Step 5: SAFEGUARD YOUR SYSTEM
In order to replicate your actions consistently, it is imperative to retain a detailed recollection of your previous steps. **It is advised against storing your system in an accessible manner, especially on digital devices such as computers or phones.**

Instead, commit your system to paper, preferably within the pages of a physical book, such as a handwritten cookbook, where it can be subtly concealed amidst unrelated content. Employ cryptic references, including terms like 'Keccak 256,' 'AES,' and 'MD2 1...,' making it less conspicuous and challenging for any observer to discern its significance.

To ensure the permanence of your system, periodically engage in the practice of reiterating the process, thus reinforcing your memory.

## USING OTHER INPUTS
Use always AES encryption + various hashes. **Never use "only hash" to generate the entropy.** Remember, in 10-20 years maybe we will have quantum computers, these will be able to check hashes of every single word or combination in all available books. So be smart. 

As an idea, you can use, instead of 3 verses, following inputs:

1. Use 3 ISBN numbers of exact edition of your top 3 books. This could be: 
ISBN 978-3828-4757-43-85, or similar.
1. 3 phone numbers of your family, incl. international call (example: +44578439574389)
Use 3 chemical formulas such as: (CH3)3CH, C12H16N2 or so.
1. 3 engine types of your beloved Mercedes cars such as: M260 E20 DE LA, M282 DE14 or similar
1. The first 30 notes in a three-part fugue, each voice is the separate input, such as: 64,67,61,62,66,63,63,62,68,69,65,63,63,62,68,69,6564,67,61 for voice 1 and so on.

So be creative, but not too creative, otherwise you will forget it! You can use something mathematical formulas with various lengths such as "pi^13.55". Remember: you should be able to remember it!

##  THE MATH
"But in 10 or 20 years these sites will maybe not work!"

Don't worry. Everything is the math. Creating Keccak 256 hash of a text string will always give the same hash string result even in other programs or tools. It is a mathematical principle that gives you the same result. It is the same with AES encryption. It will be same in forever. And it is the same with the seed. Everything is the math.

So, REMEMBER: you will be able to recreate the wallet using exact the same steps, even without CyberChef or BIP39 site above.

---
### Step 6:
If you think this was useful, I will be grateful for any donation, thank you, my unknown friend!

#### My wallets:

Bitcoin: 
`bc1qhnudrj5jlkrak5lv57wpt9txq7ys4u8xukk0qk`

<img width="199" alt="86b53183f7d4c3046b926" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d250bfb7-f66d-4476-b3ae-1660591095ec">

---
XRP:
`rMo7sjApwPLMtZji597KzvbQx9dVZB5RB1`

<img width="199" alt="5a21f4381abc73e94e921" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/76be418c-f46e-45f0-8e0d-c446a1e4a2bd">

---
Kaspa:
`kaspa:qqcs4ytttqw0c6047sycjrw2k0wzre8kcarydsm7et0ptsnhgp26vssx2v05w`

<img width="194" alt="f941b766a0af0b9dc3cdd" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/d5d46f05-6c01-4d6d-8834-e9fae0387ac3">

---
ETH /MATIC /Avalance /XDC:
`0xE13Bbb95f56e4832de7C2DB968C2dbCFf6ca5fB6`

<img width="192" alt="8f1762b7ef1c8de0c8cb1" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/21830d93-c762-4986-8600-eff68cda5aeb">

---
Solana:
`2VZ8a2nGa9T69hERERbSn4PPr3xcgr7nynX1Buy2pxxg`

<img width="194" alt="301a0e1068ba808db3ea9" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/4261cf86-2c0a-4615-907e-7d43a94539f7">

---
Hedera:
`0.0.3495787`

<img width="194" alt="0cad57a500c8dbd9430af" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/1133e898-5cc1-45f1-8b26-356c89578a38">

---
Monero:
`488zAEiixaVJdLDyCqNLFaPzuwybmzbAXaSme1EoUBFAKPLZ6vRQiJpLWGr1tyBH5eXvDHVqcdebvWf998n5722EV7SfSeW`

<img width="195" alt="e38ba04530d0973e3b0d3" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/da9b606d-0305-4388-851f-245ec0ec150d">

---
Dogecoin:
`DCnsHRu71kVuNijE9pULRhifayooP9hRqP`

<img width="194" alt="9d42d3e491d15df5a5877" src="https://github.com/CR91TQ94/INFINITE-NUMBER-OF-MEMORABLE-SEED-PHRASES-FOR-COLD-STORAGE/assets/148721952/695fc943-0f12-4a6f-9811-7855639bee1f">

# GOD LUCK AND PROSPER!
