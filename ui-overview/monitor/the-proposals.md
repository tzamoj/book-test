# The Proposals

## Tite

The **"Proposal" page** allows to submit new Proposals & monitor all the Proposals in the DAO.

1. The title of the Proposal
2. The dynamic description of the Proposal according to the type & parameters of the Proposal
3. The current status of the Proposal



* The time remaining before next status change if the Proposal status is in Voting Period OR Grace Period
* The majority needed & the current majority
* The quorum needed & the current quorum&#x20;



* The number of YES votes & NO votes
* Buttons <img src="../../.gitbook/assets/image (5) (2).png" alt="" data-size="line"> & <img src="../../.gitbook/assets/image (7).png" alt="" data-size="line"> to vote if the Proposal is in Voting Period
* A button <img src="../../.gitbook/assets/image (6).png" alt="" data-size="line"> to access granular details such as : type of Proposal / submission date / submitter address...
* A button "To process" if the Proposal status is "To Process"
* A button "Processed" if the Proposal status is "Processed"

<figure><img src="../../.gitbook/assets/OTC VOTING modified.png" alt=""><figcaption></figcaption></figure>

The Proposals are displayed as a list which can be:&#x20;

* Ordered (Time remaining OR Date submitted OR Date processed)
* Filtered (Active / Status / Type)

Filtering items are the followings:

## Filter "Status"

| Item          | Elements                                                                                                                                                                                          |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Voting period | The Proposal status is submitted AND the timer is less than Voting Period duration                                                                                                                |
| Grace period  | The Proposal status is submitted AND the timer is higher than Voting Period duration AND the timer is less than Grace Period duration                                                             |
| Rejected      | The Proposal status is submitted AND the timer is higher than Voting Period duration AND Majority AND/OR Quorum requirements are not met                                                          |
| To Process    | The Proposal status is submitted AND the timer is higher than Grace Period duration AND Majority AND Quorum requirements are met at the end of the Voting Period AND the proposal is not executed |
| Processed     | The proposal is executed                                                                                                                                                                          |

## Filter "Active"

| Item | Elements                                              |
| ---- | ----------------------------------------------------- |
| Yes  | Status is Voting Period OR Grace Period OR To Process |
| No   | Status is Rejected OR Processed                       |

## Filter "Type"

| Item       | Elements                    |
| ---------- | --------------------------- |
| Onboard    | Proposal Type is Onboard    |
| Add Shares | Proposal Type is Add Shares |
| Signal     | Proposal Type is Signal     |
| Whitelist  | Proposal Type is Whitelist  |
| OTC Swap   | Proposal Type is OTC Swap   |
| AMM Swap   | Proposal Type is AMM Swap   |

