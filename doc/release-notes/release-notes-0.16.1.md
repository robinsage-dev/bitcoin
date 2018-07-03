Kala Core version 0.16.1 is now available from:

  <https://github.com/robinsage-dev/kala/releases/download/v0.16.0krc1/kala-v0.16.1krc1-x86.64-linux-gnu.tar.gz/>

This is the first major release for Kala along with a new minor version release from Bitcoin, with various bugfixes as well as updated translations.

Please report bugs using the issue tracker at GitHub:

  <https://github.com/robinsage-dev/kala/issues>

How to Install
==============

Run the installer (on Windows) or just copy over `/Applications/Bitcoin-Qt` (on Mac)
or `bitcoind`/`bitcoin-qt` (on Linux).

Compatibility
==============

Kala Core has only been tested on Linux.

Bitcoin Core is extensively tested on multiple operating systems using
the Linux kernel, macOS 10.8+, and Windows Vista and later. Windows XP is not supported.

Bitcoin Core should also work on most other Unix-like systems but is not
frequently tested on them.

Notable changes
===============

Change major blockchain parameters that affect block time, miner subsidy, and added a spendable premine.

See Bitcoin release notes for versions after v0.15.1 for contributions from Bitcoin developers.


0.16.1 change log
------------------

### Policy
- Automatically enforce all BIPs up until Bitcoin v0.16.1 release from block 1.

### Mining
- Change subsidy halving interval to 2100000 blocks to maintain 4 year interval.
- Change difficulty adjustment interval to 60 blocks (1 hour).
- Change miner subsidy to 4285 KALA.
- Change target blocktime to 1 minute.

## Transactions
- Change mainnet address prefixes to: 9 (pubkey address) and K (script address).
- Change testnet and regtes address prefixes to: z (pubkey address) and k (script address).

### P2P protocol and network code
- Change default ports to: 7332, 17332, and 17443.
- Change CHAIN_SYNC_TIMEOUT to 2 minutes.
- Change STALE_CHECK_INTERVAL to 1 minute.
- Change magic message to 0x93b8d89d.
- Remove checkpoint data.

### Block and transaction handling
- Allow genesis block to have low difficulty, and for its coinbase (3B KALA premine) to be spendable and larger than normal coinbase transactions.

### Tests and QA
- Skipped various tests inluding functional, qt-related, and wallet-related.
- Skipped checkinputs_test in txvalidationcache_tests.cpp

### Documentation
- Customized README for Kala

Credits
=======

Thanks to bitcoin team for the majority of the code in this release.
