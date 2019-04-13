# DEPRECATED

This repository is archived and will not be maintained.

The CashShuffle plugin went through many revisions here and in another repository and is now included as a standard part of Electron Cash.

You can find CashShuffle documentation at [github.com/cashshuffle/spec](https://github.com/cashshuffle/spec).

You can find Electron Cash at [github.com/Electron-Cash/Electron-Cash](https://github.com/Electron-Cash/Electron-Cash).

----------


This plugin for electron-cash BCH wallet. It allows user to make a coinjoin shuffled transaction.

## Installation
1. place the `shuffle` folder to electron-cash `/plugins` folder
2. add the link to plugin to electron-cash setup.py with adding `'electroncash_plugins.shuffle'` to setup packages list.
3. re-install electron-cahs

```
sudo python3 setup.py install
```
## Getting started

1. Enable plugin from 'tools/plugins' menu

![Settings](/images/settings.png)

2. Press `Settings` and enter the server connection string

![Server settings](/images/server_settings.png)

3. Close the settings dialog window. The shuffle tab will appear

![Server settings](/images/shuffle_tab.png)

## Making shuffle

1. Form `Shuffle input address` choose coin which you want to shuffle. The list of coins formed from utxo's of your wallet.

2. From `Shuffle change address` choose the address for the change. You can leave default setting if you don't want to get any change back.

3. From `Shuffle output address` choose the address for shuffled output

4. In the amount block choose the amount of coins for shuffling.

5. Fee is fixed and unchanged  

6. If amount of coins in input grater then sum of shuffling amount fee then `Shuffle` button will become enabled

7. Pressing the `Shuffle` will start shuffling process. After 5 players registered on server shuffling process will starts.

8. If all goes good you will see the outputs and transaction dialog window in the end. If something goes wrong you will see the errors in output.

9. In this version of protocol one of the players should press `broadcast` on transaction dialog window.    
