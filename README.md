Zerozed (formerly "Crypt0z") integration/staging tree
================================

Website http://www.crypt0z.us/

Twitter https://twitter.com/zerozed_x0z

Exchange https://meanxtrade.com/trade/btc/x0z

BTC ANN https://bitcointalk.org/index.php?topic=4096286

Discord https://discord.gg/8GcFtUX

Telegram https://t.me/zerozed_x0z

IRC #zerozed https://webchat.freenode.net/

Pool 1 https://x0z.magnificentpool.com/

Pool 2 (DOWN) http://pool.fatpanda.club 

Pool 3 https://umine.org/

Block Explorer 1 http://18.217.129.225:3001/

Block Explorer 2 https://umine.org/explorer/x0z



Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2018 Zerozed Developers

What is Zerozed? (Zero Zed Ecosystem & Algorithm)
----------------

Zerozed is a Smart Inflation Cryptocurrency which utilises the Diffusion of Innovations to fairly distribute supply evenly among the population.

Mission Goal: 

Create an easily replicable software, hardware and decentralised autonomous organisational structure of which can be used to empower and advance emerging nations seamlessly into the present and beyond into a future without a centralised State run governance system required to sustain it.

In one line? An experiment on Blockspace Economics using a Diffusion of Innovations based incentive model.

Zerozed is a litecoin v0.8 fork using scrypt as a proof-of-work algorithm with 32MB block sizes and the diffusion of innovations in replacement of the standard halving adopted by 99% of cryptocurrencies. Everything else is pretty normal. Launched under "Crypt0z" branding.
 - 32 MB Blocksize (On-Chain Scaling)
 - 2 hour difficulty retarget
 - 2 minute block targets
 - 99% of coins produced over 5 years using DoI minting schedule
 - ~25 million total coins
 - +much more planned (Starting with Atomic Swaps)

Fifty percent of the world's net wealth belongs to one percent of the population. The emergence of Cryptocurrency has brought about a rapid disruption across many industries but none more than Finance and Economics. Due to the inherent flaw in Bitcoin and by extension 99% of Blockchain based Distributed Ledger Technologies, "Crypto" has succumbed to the same fate as Fiat. Riddled with systemic issues and mass centralisation of supply. 
    This is all due to the inflation model otherwise known as the "halving-mechanism", one of which no one has seemingly questioned. This paper seeks to solve these problems with an alternative model for incentive and inflation. In replacement to the standard halving-mechanism employed by the greater majority of Cryptocurrencies to-date, we demonstrate the modeling of an inflation schedule guided by the theory, Diffusion of Innovations.

We have proposed an inflation model for Cryptocurrencies yet to launch, as well as coins existing today, to set or retarget subsidy schedules in order to follow a more sustainable and diffusion-viable incentive model. By utilising the Diffusion of Innovations we can establish the Normal Distribution within a socioeconomic environment and the Zerozed team have set out to prove this via bootstrapping a brave new Cryptocurrency with our MVP, x0z.
    The Zerozed team will endeavour to contribute and assist with broader crypto innovations and interoperability in order to provide all the necessary conditions which provide the best chance of survival within the ever evolving space. If proven successful, the Zerozed project is expected to thrive well beyond the initial inflation cycle and is set to bring to light information that will assist the industry as a whole, in turn gaining broader acceptance and diffusion of Cryptocurrencies and Distributed Ledger Technologies throughout society.

Compiling is currently a nitemare. Sorry.

Easiest to compile with this untill rebase is done in the coming weeks http://old-releases.ubuntu.com/releases/16.04.3/ubuntu-16.04.3-desktop-amd64.iso  

(this might help as well) https://stackoverflow.com/questions/28958570/dependency-failure-while-installing-libboost-all-dev-on-ubuntu-core-14-04 https://askubuntu.com/questions/300872/help-installing-libboost-system-dev-et-al

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

License
-------
Zerozed is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Zerozed
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/calems/crypt0z/tags) are created
regularly to indicate new official, stable release versions of Zerozed.

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
    ./crypt0z-qt_test

