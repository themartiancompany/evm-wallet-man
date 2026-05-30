..
   SPDX-License-Identifier: AGPL-3.0-or-later

   -------------------------------------------------------
   Copyright © 2024, 2025, 2026
               Pellegrino Prevete

   All rights reserved
   -------------------------------------------------------

   This program is free software: you can redistribute it
   and/or modify it under the terms of the
   GNU Affero General Public License as published by
   the Free Software Foundation, either version 3 of the
   License, or (at your option) any later version.

   This program is distributed in the hope that it will
   be useful, but WITHOUT ANY WARRANTY; without even the
   implied warranty of MERCHANTABILITY or FITNESS FOR A
   PARTICULAR PURPOSE.
   See the GNU Affero General Public License
   for more details.

   You should have received a copy of the
   GNU Affero General Public License
   along with this program.
   If not, see <https://www.gnu.org/licenses/>.


=====================
eoa-fingerprint
=====================

-----------------------------------------------------------
Ethereum External Account (EOA) fingerprint tool
-----------------------------------------------------------
:Version: eoa-fingerprint |version|
:Manual section: 1


Synopsis
========


      "",
      "  seed               A seed path or a seed phrase",
      "",
      "  target-network     Chain ID or RPC address, optional.",
      "",
      "  api-key-path       Etherscan-like service API key, optional.",
      "",
      "  output-file        If specified will save the output",
      "                     to a file, otherwise will print it.",
      "",
      "options:",
      "",
      "  -h, --help         Displays this help.",
      ""

eoa-fingerprint *[options]* *quiet* *seed* ( *target-network* *api-key-path* *output-file* )


Description
===========

Returns the EOA fingerprint of a seed (the address)",


Commands
=========

* get  *wallet-name*  *key*

  Retrieves information about specific items of single wallets.

* set *wallet-name* *key* *value*

  Sets information about specific items of single wallets.

* list *filter*

  Display contacts information for wallest respecting the filter.

* send *address* *amount*

  Sends balance to an address.


Get and set arguments
=======================

* address

  Returns wallet address.

* balance

  Returns balance for the wallet.

* seed

  Returns wallet seed phrase.


List arguments
=================

* filter

  Restrict the listing to wallets respecting the filter.
  It can be a regex.


Networks
=========

All those supported by
'evm-chains-info' as
well as direct RPC addresses.


Options
========

-u measure-unit, --measure-unit measure-unit             Measure unit for the transaction
                                                         value. It can be 'ether' or 'wei'

-l balance-lifespan, --balance-lifespan seconds          Maximum threshold in seconds
                                                         from now after which to consider
                                                         balance to be outdated.

-a, --all-networks                                       Operation valid for all available
                                                         networks.
-P tasks-parallel, --tasks-parallel integer              Tasks to perform in parallel.


List options
==============

-o output-type, --output-type output-type                Output type for the list option.
                                                         It can be 'name', 'address',
                                                         'fingerprint'.


Network options
================

-n network, --network network                            EVM network name. Accepted values
                                                         are all those supported by
                                                         evm-chains-info and RPC addresses.

-S rpc-selection, --rpc-selection rpc-selection          RPC selection method.

-E explorer-selection, --explorer-selection criterion    Network explorer selection method.
                                                         See 'evm-chains-info' manual page for
                                                         details.

-r retries-max, --retries-max retries-max                Maximum number of retries before
                                                         failing.


Credentials options
=====================

-w wallet-path, --wallet-path wallet-path                Wallet path.

-p wallet-password, --wallet-password wallet-password    Wallet password.

-s wallet-seed, --wallet-seed wallet-seed                Wallet seed path.

-k api-key, --api-key api-key                            Etherscan-like service key.

-Q <y/n>, --qr-support <y/n>                             Quantum-resistant ciphers
                                                         support.


Application options
=====================

-h, --help                                               This message.

-c, --color                                              Enable color output. Only in the
                                                         Bash implementation.

-v, --verbose                                            Enable verbose output


Bugs
====

https://github.com/themartiancompany/evm-wallet/-/issues


Copyright
=========

Copyright Pellegrino Prevete. AGPL-3.0.


See also
========

* evm-wallet
* erc20-token-send
* gas-transfer
* mkseed
* ether2wei
* evm-chains-info
* evm-chains-explorers
* evm-contract-call
* key-gen

.. include:: variables.rst
