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


============
gas-transfer
============


---------------------------------------------------------
Gas transfer utility
---------------------------------------------------------
:Version: gas-transfer |version|
:Manual section: 1


Synopsis
========

gas-transfer *quiet* *wallet-seed-path* *target-address* *amount* (*network* *api-key-path* *measure-unit* *call-timeout*)


Description
===========

Transfer gas from an address to another.

Arguments
=========

* *quiet*

  Enable verbose output.
  Can be 'y' or 'n'.

* *wallet-seed-path*

  Path of the file containing the seed phrase.


* *target-address*

  Address to send some balance to.

* *amount*

  How much balance to send.

* *network*

  Network on which the contract resides.
  It can be a chain ID or an RPC address.

* *api-key-path*

  Path of the API key for the contract ABI
  service provider.

* *measure-unit*

  Token ABI file path (JSON).

* *call-timeout*

  How many milliseconds to wait for a return
  before declaring the call failed.


Options
=======

-h, --help              This message.
-v, --verbose           Enable verbose output


Bugs
====

https://github.com/themartiancompany/evm-wallet/-/issues


Copyright
=========

Copyright Pellegrino Prevete. AGPL-3.0.


See also
========

* evm-wallet
* mkseed

.. include:: variables.rst
