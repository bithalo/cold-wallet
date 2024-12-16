# cold-wallet
Cold wallet for web3

Please audit this and use it at your own risk. This is a simple web3 cold wallet. The idea is that the user never exposes their private key to the internet. The most important part of this method is using or creating a computer that does not have any internet capacity whatsoever. That computer should never connect to the internet, not even once. The ideology of this is if the computer is compromised with keyloggers it would still not be possible to hijack ones wallet unless there was something hidden in the hardware itself. As long as the libraries and dependencies are solid then this may be one of the safest wallets in the world. At some point a developer could try to make this multisig for further protection.

The method of secure account creation and use is as follows:
1) Set up a computer with no internet access with Firefox or Thorium or Chromium installed with no plugins(preferably Linux machine)
2) Put the website source code on the computer and run the python XMLRPC server and load the index.html page
2) Figure out your wallet address by logging in with a very strong and unique password.
3) Load that address without logging in on a second "online" computer or device using the same copy of the source code.
4) Export the account data to a USB drive after it loads
5) Login at the offline machine and load the data file from the USB
6) Sign a transaction and export the signature file to the USB drive
7) Load the signature file and broadcast from the "online" machine

As a bonus you may heavily insulate the offline device or block it with a farraday cage so that even if hardware was compromised it would not be able to send any signals via bluetooth, rfid, low frequency, wifi or internet. However at a minimum it should not have a network card. This software comes only as a demo and it was moderately tested so it's best to start with a few small test transactions to vindicate it.