Bitcoin's Blocksize Markets
=================================

The real world implementation of [the proposal here](http://www.truthcoin.info/blog/win-win-blocksize/).

As presented at [the September 2015 Montreal Bitcoin Scalability Conference](https://scalingbitcoin.org/montreal2015/).

What is Sidechain Elements?
-----------------

Sidechain Elements is a collection of experiments to bring more technical innovation to Bitcoin.

https://github.com/ElementsProject/elementsproject.github.io

Read details and future in the project documentation

What is the Blocksize Element?
-----------------------

Blocksize Market is a version of Bitcoin where user-activities are limited to the following:

1. Deposit Bitcoin (xfer coins, from the Bitcoin mainnet, to this Sidechain).
2. Withdraw Bitcoin (xfer coins, from this Sidechain, to the Bitcoin mainnet).
3. Buy shares.
4. Sell shares.
5. Set final market prices.

The 5th activity can only be performed by a pre-selected panel of Reporters, after August 1st, 2016.

How Can I Help?
-----------------------

1. Familiarize yourself with the Bitcoin / elements codebase.
2. Familiarize yourself with [trading via market scoring rules](http://www.truthcoin.info/papers/LogMSR_Demo.xlsx).
3. Help me combine the two!

Markets with MSRs are updated with a single formula, and single-party atomic state update (just like passing around a single Bitcoin). They have [already been implemented](https://github.com/truthcoin/truthcoin-cpp/blob/master/src/primitives/market.h) in my larger project, Truthcoin.

The remaining technical piece is a simple "freezing" of the market prices (also already implmented in Truthcoin) at their final values. However, while in Truthcoin this is very complex, here we want something different and simpler: 4 of 7 multisignature reports. 

From there, all that will be required will be to:
1. Select the Blocksize proposals which, we feel, merit inclusion.
2. Select the Reporters ("oracles").
3. Initialize the chain with our chosen market.
4. Test this on the Bitcoin testnet.
5. Launch it on the Bitcoin mainnet.

License
-------

The Blocksize Markets project is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see http://opensource.org/licenses/MIT.
