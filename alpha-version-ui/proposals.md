# Proposals

Once connected, the Home screen recaps the list of the proposals;

Screen

The list of proposals can be:&#x20;

* Ordered (Time remaining ASC / DESC, Date submitted ASC/DESC, Date processed ASC/DESC)
* Filtered (Active / Status / Type)

Filtering items are the followings:

| Filter | Element | Indicator                                           |
| ------ | ------- | --------------------------------------------------- |
| Active | Yes     | Status is submitted OR accepted OR forced           |
| Active | No      | Status is aborted OR rejected OR executed OR failed |
| Active | All     |                                                     |

| Filter | Element         | Indicator |
| ------ | --------------- | --------- |
| Status | Voting period   |           |
| Status | Grace period    |           |
| Status | To be processed |           |
| Status | Processed       |           |

| Filter | Element    | Indicator |
| ------ | ---------- | --------- |
| Type   | Onboard    |           |
| Type   | Add Shares |           |
| Type   | Signal     |           |
| Type   | Whitelist  |           |
| Type   | Swap       |           |

Each proposal item includes:

* The title of the proposal
* The status of the proposal
* The time remaining before next status change
* The majority needed / the current majority (voting period) / the majority (non voting phase)
* The quorum needed / the current quorum (voting period) / the quorum (non voting phase)
* The number of YES votes & NO votes
* Buttons <img src="../.gitbook/assets/image (8).png" alt="" data-size="line"> and <img src="../.gitbook/assets/image.png" alt="" data-size="line">to vote&#x20;
