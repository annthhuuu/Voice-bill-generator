# Test Cases

Record actual outcomes only after executing the tests.

| ID | Scenario | Input / Preconditions | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| TC-01 | Clear voice input | Supported clear command | Speech is captured and recognized | Not run | Not run |
| TC-02 | Noisy audio | Command with background noise | Ask user to repeat or correct | Not run | Not run |
| TC-03 | Valid product extraction | Known product and quantity | Correct item and quantity extracted | Not run | Not run |
| TC-04 | Unknown product | Product absent from catalogue | Ask user to select or add product | Not run | Not run |
| TC-05 | Missing quantity | Product spoken without quantity | Request quantity or use defined default | Not run | Not run |
| TC-06 | Line calculation | Quantity 2, unit price 50 | Line total is 100 | Not run | Not run |
| TC-07 | Multiple items | Two or more valid items | Correct lines and grand total | Not run | Not run |
| TC-08 | Correct an item | Edit quantity before confirmation | Recalculate total correctly | Not run | Not run |
| TC-09 | Confirm bill | Valid preview approved | Bill saved/exported | Not run | Not run |
| TC-10 | Storage failure | Save operation fails | Show error; do not report success | Not run | Not run |

## Execution Summary
- Total: 10
- Passed: 0
- Failed: 0
- Not run: 10

Update this summary based on real test execution and attach evidence where possible.
