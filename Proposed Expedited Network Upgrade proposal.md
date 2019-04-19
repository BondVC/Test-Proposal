
## Proposed Expedited Network Upgrade proposal v.2
The main reason of this proposal is to clarify all conditions and give more time for validators to upgrade the software
Changes:
1. Fixed typo of state export block number
2. Increased the time window from 2 hours to 9 hours

According to the expedited rules laid down in governance proposal #3 the following criteria needed to be met:
1. `v0.34.0` released by the development team
2. New testnet launched using that release.
3. No critical issues found during testing.

`v0.34.0` has been released, and the upgrade procedure that will be followed for mainnet was carried out on the`gaia-13002` test on April 8th. 
The network came up with no issues and has been running w/o problems since then. Seeing as the conditions of the expedited process have been followed, we propose the following upgrade path:

1. Final code hash for Hub 0.34 state machine is `0f7877c23b407e24e56056469e90fe6b8a78d84c`
2. `Gaia-13003` is a successful test of the upgrade procedure and final code
3. State export from `cosmoshub-1` is at block`500000`
4. Genesis time will be `2019-04-23T00:00:00Z UTC`
5. Validators can generate the new genesis file by running
`# must be run after the chain is stopped using v0.33.2 gaiad export —height=500000 —for-zero-height > cosmoshub-1-export.json # must be run after the upgrade to v0.34.0 python3 contrib/export/v0.33.x-to-v0.34.0.py —chain-id=cosmoshub-2 \  —start-time=2019-04-22T17:00:00Z \     cosmoshub-1-export.json > > genesis.json`

   Block 500,000 shall be known as the Adriana’s block as she proposed it for the upgrade.