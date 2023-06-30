# IVO-Snapshots

run_summary.csv: every snapshot run logs get appended to this file, containing:

- CSV Filename: Used as the hourly commit message to this repo. Based on "ledger_state -> timestamp" output at the time of the snapshot.
- Total Validator Count: This is the total number of stakers at the time of the snapshot.
- Total Validator Stake: The total amount of XRD that is delegated to the Ethereal IVO Validator, at time of snapshot. 
- Current REAL per XRD: Every hour, 4528.9855072463 REAL are allocated for all stakers combined. The more XRD at the pool, the less REAL per XRD.

2023-XX-XXTXX:XX:XX.XXXZ_stakes.csv: every snapshot run, we dump a snapshot of the current staking situation at the validator, containing:

- Validator Address: Should always be rv1qtyutcs2thaqa4dq2m95yllhuqmms75x2yena3huh6758pfdhjkrsrvqvu3 as this is our validator address.
- Account Address: Wallet address of each staker.
- Total Stake: Total amount of XRD staked at the time of the snapshot.

2023-XX-XXTXX:XX:XX.XXXZ_stakes.csv_rewards.csv: REAL rewards accumulated that hour:

- Address: Wallet address of each staker.
- Rewards: REAL rewards accumulated for that snapshot only, based on current (REAL per XRD) x (Total Stake) of each wallet.

Rewards.csv: TOTAL up-to-date accumulated rewards for each Address participating in the IVO.
