# FarmPlay — Sample Data and Test Cases

**Status:** Planned test cases for the proposed prototype  
**Note:** These cases describe expected behaviour. They have not yet been executed because the application is not implemented.

## 1. Sample data files
- `sample_data/farmers.json` — fictional farmer profiles.
- `sample_data/missions.json` — illustrative sustainable farming missions.

All records are fictional and intended for prototyping only.

## 2. Test cases

| ID | Feature | Test input / action | Expected result | Priority |
|---|---|---|---|---|
| TC-01 | Load missions | Open the mission catalogue with valid sample data | All valid missions are displayed | High |
| TC-02 | Mission details | Select `MIS001` | Title, description, category, duration, and points are shown | High |
| TC-03 | Complete mission | Complete an available mission once | Completion is recorded and the configured points are added | High |
| TC-04 | Duplicate completion | Complete the same mission again for the same farmer | No second points award; a clear message is shown | High |
| TC-05 | Score calculation | Earn 40 eligible points with a 100-point target | Illustrative score is 40/100 | High |
| TC-06 | Score upper limit | Earn more than the 100-point target | Illustrative score does not exceed 100 | Medium |
| TC-07 | Invalid mission ID | Attempt to complete a mission that does not exist | Action is rejected without changing points | High |
| TC-08 | Missing profile field | Load a farmer record without a required ID | Record is rejected or a clear validation error is shown | Medium |
| TC-09 | Empty mission list | Load an empty mission array | Show an informative “No missions available” state | Medium |
| TC-10 | Mobile layout | View the prototype at a narrow phone width | Content remains readable and controls are usable | High |
| TC-11 | Privacy | View a public leaderboard in a future version | Only opted-in display names and allowed data are shown | High |
| TC-12 | JSON validity | Parse both sample JSON files | Both files parse without syntax errors | High |

## 3. Example scoring check
For the proposed illustrative formula:

`score = min(100, total_eligible_points / target_points * 100)`

With `total_eligible_points = 40` and `target_points = 100`, the expected result is `40`.

With `total_eligible_points = 120` and `target_points = 100`, the expected result is `100`.

The formula is a prototype example, not a validated measure of real-world sustainability.

## 4. Test execution record
| Field | Value |
|---|---|
| Application build | Not available yet |
| Test execution status | Not run |
| Reason | Prototype implementation is pending |
| Next step | Execute these cases after the relevant features are built |

Update this section with actual results, date, and build/version once tests have been run.
