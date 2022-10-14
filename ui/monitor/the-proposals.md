# The Proposals

The "Proposal" page allows&#x20;

<figure><img src="../../.gitbook/assets/OTC VOTING modified.png" alt=""><figcaption></figcaption></figure>

Screen

The list of proposals can be:&#x20;

* Ordered (Time remaining ASC / DESC, Date submitted ASC/DESC, Date processed ASC/DESC)
* Filtered (Active / Status / Type)

Filtering items are the followings:

| Filter | Element | Indicator                             |
| ------ | ------- | ------------------------------------- |
| Active | Yes     | Status is voting + grace + to process |
| Active | No      | Status is rejected + processed        |
| Active | All     |                                       |

| Filter | Element       | Indicator                                                                              |
| ------ | ------------- | -------------------------------------------------------------------------------------- |
| Status | Voting period | Status is submitted & t\<voting period                                                 |
| Status | Grace period  | Status is submitted & t>voting + \<grace period AND  quorum + majority                 |
| Status | Rejected      | Status is submitted & t>voting AND/OR majority + voting                                |
| Status | To process    | Status is submitted & t>voting + >grace period AND  quorum + majority AND not executed |
| Status | Processed     | Executed                                                                               |

| Filter | Element    | Indicator |
| ------ | ---------- | --------- |
| Type   | Onboard    |           |
| Type   | Add Shares |           |
| Type   | Signal     |           |
| Type   | Whitelist  |           |
| Type   | OTC Swap   |           |
| Type   | AMM Swap   |           |

Each proposal item includes:

* The title of the proposal
* The status of the proposal
* The time remaining before next status change
* The majority needed / the current majority (voting period) / the majority (non voting phase)
* The quorum needed / the current quorum (voting period) / the quorum (non voting phase)
* The number of YES votes & NO votes
* Buttons <img src="../../.gitbook/assets/image (5).png" alt="" data-size="line"> and <img src="../../.gitbook/assets/image (7).png" alt="" data-size="line"> to vote on the proposal (if voting period and applicable to the role)
* A button <img src="../../.gitbook/assets/image (6).png" alt="" data-size="line"> to access...
* A btton to process the proposal (if ....)

