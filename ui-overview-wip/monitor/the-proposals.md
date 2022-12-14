# The Proposals

The **"Proposal" page** allows to submit new Proposals & monitor all the Proposals in the DAO.

Each Proposal card includes:

* The time remaining before next status change if the Proposal status is in Voting Period OR Grace Period
* The majority needed & the current majority
* The quorum needed & the current quorum&#x20;
* The number of YES votes & NO votes
* Buttons <img src="../../.gitbook/assets/image (5) (2).png" alt="" data-size="line"> & <img src="../../.gitbook/assets/image (7).png" alt="" data-size="line"> to vote if the Proposal is in Voting Period
* A button <img src="../../.gitbook/assets/image (6).png" alt="" data-size="line"> to access granular details such as : type of Proposal / submission date / submitter address...
* A button "To process" if the Proposal status is "Approved - ready to be process" or "Rejected - ready to be process"
* A button "Processed" if the Proposal status is "Approved" or "Rejected"

<figure><img src="../../.gitbook/assets/OTC VOTING modified.png" alt=""><figcaption></figcaption></figure>

The Proposals are displayed as a list which can be:&#x20;

* Ordered (Time remaining OR Date submitted OR Date processed)
* Filtered (Active / Status / Type)

Filtering items are the followings:

## Filter "Status"

| Item                        | Elements                                                                                                                                                                                           |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Voting period               | The Proposal is submitted AND the timer is less than Voting Period duration                                                                                                                        |
| Rejected - ready to process | The Proposal is submitted AND the timer is higher than Voting Period duration AND Majority OR Quorum requirements are not met                                                                      |
| Grace period                | The Proposal is submitted AND the timer is higher than Voting Period duration AND the timer is less than Grace Period duration AND NOT Rejected - ready to process                                 |
| Approved - ready to process | The Proposal status is submitted AND the timer is higher than Grace Period duration AND Majority AND Quorum requirements are met at the end of the Voting Period AND the proposal is not processed |
| Approved                    | An "Approved - ready to process" Proposal  is processed                                                                                                                                            |
| Rejected                    | An "Rejected - to ready process" Proposal is processed                                                                                                                                             |

## Filter "Active"

| Item | Elements                                                                                              |
| ---- | ----------------------------------------------------------------------------------------------------- |
| Yes  | Status is Voting Period OR Grace Period OR Approved - ready to process Or Rejected - ready to process |
| No   | Status is Approved OR Rejected                                                                        |

## Filter "Type"

| Item      | Elements                     |
| --------- | ---------------------------- |
| Onboard   | Proposal Type is Onboard     |
| Signal    | Proposal Type is Signal      |
| Whitelist | Proposal Type is Whitelist   |
| Blacklist | Proposal Type is Unwhitelist |
| OTC Swap  | Proposal Type is OTC Swap    |
| AMM Swap  | Proposal Type is AMM Swap    |

