blockchain_wallet:
Your new startup is focusing on building a portfolio management system that supports not only traditional assets like gold, silver, stocks, etc, but crypto-assets as well! The problem is, there are so many coins out there! It's a good thing you understand how HD wallets work, since you'll need to build out a system that can create them. You're in a race to get to the market. There aren't as many tools available in Python for this sort of thing, yet. Thankfully, you've found a command line tool, hd-wallet-derive that supports not only BIP32, BIP39, and BIP44, but also supports non-standard derivation paths for the most popular wallets out there today! However, you need to integrate the script into your backend with your dear old friend, Python. Once you've integrated this "universal" wallet, you can begin to manage billions of addresses across 300+ coins, giving you a serious edge against the competition. In this assignment, however, you will only need to get 2 coins working: Ethereum and Bitcoin Testnet. Ethereum keys are the same format on any network, so the Ethereum keys should work with your custom networks or testnets.



#function of hd wallet:

HD wallets can allow for an entire suite of crypto-wallets to be generated from a single seed phrase.HD wallet is a public/private key tree all starting from a root node (master node). Here’s a g


 the wallet is built with these needed dependencies:
 
• Install PHP on my os
• Clone hd-wallet-derive tool into my project 
  directory folder 
• bit Python Bitcoin library
• web3.py Python Ethereum library

 Project set up:
 
•Create a symlink called derive for the hd-
 wallet-derive/hd-wallet-derive.php script 
 into the top level project directory like so:
 ln -s hd-wallet-derive/hd-wallet-derive.php 
 derive
 
•to make the connection with hd wallet:
 run def derive_wallets (mnemonic, coin, num):
 command = f'./derive -g --mnemonic="
 {mnemonic}" --coin="{coin}" --numderive="
 {num}" -  
cols=index,path,address,privkey,pubkey,pubkeyha
 sh,xprv,xpub --format=json'

p = subprocess.Popen(command, stdout=subprocess.PIPE, shell=True)
(output, err) = p.communicate()

keys = json.loads(output)

return keys


•For the BTC Test transactions and ETH 
 transaction  i wanted to use command from 
 wallet import *, to iniate a funding of my
 wallets and then  create_tx, and send tx


•For the Ethereum transactions i would have run 
 FROM WALLET IMPORT *, and i would have 
 used ganache with prefunded ether to send
 ether  to my child wallet from hd wallet 
 wallets



