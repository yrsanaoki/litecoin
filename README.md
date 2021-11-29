Poohcoin integration/staging tree
================================

![coinlogo2](https://user-images.githubusercontent.com/94148011/142076556-3837e785-a1f5-477d-9cf2-173f363b1ff0.png)


http://www.poohcoin.org

https://discord.gg/sF7TfQR3Uc

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2021 Poohcoin Developers

What is Poohcoin?
----------------

Poohcoin is the first minable protest coin using scrypt as a proof-of-work algorithm (Litecoin fork).
 - 1 minute block targets
 - subsidy halves in 890.604 blocks
 - 890.604.000 total coins
 - '89-06-04
 - 500 coins per block
 - Based on fast and trusted Litecoin
 - Together angainst censorship

For more information, as well as an immediately useable, binary version of
the Poohcoin client sofware, see http://www.poohcoin.org.

License
-------

Poohcoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Poohcoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/poohcoin-project/poohcoin/tags) are created
regularly to indicate new official, stable release versions of Poohcoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./poohcoin-qt_test

UBUNTU DEPENDENCIES (Poohcoin v0.8.9.x only works on Ubuntu 18.04.2 for now)
-------------------

    sudo apt-get update

    sudo apt-get install build-essential gcc make perl dkms


    reboot


    sudo apt-get install git

    sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils

    sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev

    sudo apt-get install libboost-all-dev

    sudo apt-get install software-properties-common

    sudo add-apt-repository ppa:bitcoin/bitcoin

    sudo apt-get update

    sudo apt-get install libdb4.8-dev libdb4.8++-dev

    sudo apt-get install libminiupnpc-dev

    sudo apt-get install libzmq3-dev

    sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler 

    sudo apt-get install libqt4-dev libprotobuf-dev protobuf-compiler

    sudo apt-get install openssl1.0

    sudo apt-get install libssl1.0-dev
    
First Startup (DNS SEED)
-------------

1. In terminal `cd` to the `poohcoin-0.8.x/src` folder
2. type `make -f makefile.unix`
3. `cd..`
4. type `./poohcoin-qt`

If you get rpcuser/rpcpassword error of no connections found:
1. Go to your files and click Home
2. `ctr h` to show hidden files
3. Go to `.poohcoin` folder
4. Make a new file called `poohcoin.conf`
5. add: `addnode=vps-zap836081-1.zap-srv.com` 

Mining Poohcoin
---------------

In the wallet:

1. Help > Debug Window
2. Console
3. Type `setgenerate true`


From the terminal:

1. `cd` to the `src` folder
2. Type `./poohcoind`
3. Use `./poohcoind setgenerate true` to start mining
