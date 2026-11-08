# HW01: Python basics

Status: original attempt reviewed on 8 November 2026; corrections pending. The notebook is a byte-for-byte copy of the supplied attempt, renamed to `hw01.ipynb`. Its code and saved outputs have not been rewritten.

## Review

All eight cells and their saved outputs were read. The four code cells were executed in order in a fresh Python namespace, and the results were compared with independently calculated totals. The last code cell reproduces the saved `TypeError: 'int' object is not callable`.

The Base section is required; Standard and Challenge are optional according to the notebook. This review is feedback, not an instructor's grade.

### Fix the runtime error first

In the Standard cell, `sum = 0` assigns an integer to the name of Python's built-in `sum` function. The Challenge cell later tries to call that integer while building `day_revenue`, causing the error. Choose a distinct name for the savings accumulator and update its uses. Then restart the kernel and run all cells; rerunning only the last cell will keep the old name binding.

### Task-by-task findings

| Task | Result | Feedback |
| --- | --- | --- |
| 1. Clean city names | Correct | Spaces and case are normalized correctly for the supplied data. |
| 2. Convert amounts | Correct | Every amount becomes an integer. |
| 3. Count, total, rounded mean | Small requirement gap | The values are correct: 12 orders, total 203,760, mean 16,980.0. Explicit rounding to an integer is missing; this dataset happens to have an integral mean. |
| 4. Unpaid orders | Correct | 3 unpaid orders totaling 95,400. |
| 5. Order table | Formatting gap | `zip` and the f-string are correct. Use the requested `city | amount | status` separators instead of comma-separated labels. |
| 6. Revenue by city | Incorrect | The current 82,660 combines both cities. The task asks for separate paid totals: Almaty 60,160 and Astana 22,500. |
| 7. Largest paid order | Incorrect | The selected Astana order at index 5 is unpaid. The largest paid order is Almaty, index 10 (order 11 when counting from one), amount 41,000. Apply the paid condition before selecting the maximum. |
| 8. Weekend order share | Incorrect | The code measures the share of order amounts, giving 25.37%. The task asks for a count: 3 weekend orders out of 12, or 25%. |
| 9. Savings months | Correct, with a style issue | Both answers are correct: 27 months at a fixed contribution and 18 with increasing contributions. The shared loop keeps accumulating the second balance after its target is reached; separate calculations would be clearer. Avoid the variable name `sum`. |
| 10. Sorted city revenue lists | Correct | The two lists stay aligned and paid revenue is sorted in descending order. No dictionary or library is used for this task. |
| 11. Median | Incorrect | The code takes middle positions from the unsorted list and gets 29,150. Sort a copy before choosing the middle values. The middle pair is 9,900 and 12,500, so the median is 11,200. |
| 12. Daily histogram | Runtime and formatting issues | No histogram is produced because of the `sum` error. The print format also omits the numeric total shown beside the bars in the example. See the revenue interpretation note below. |
| 13. Reflection | Missing | Add your own Markdown cell with the requested 2-3 sentences about the data problems you encountered. |

### Check values

Task 10 should pair these lists in the same order:

| City | Paid revenue |
| --- | ---: |
| Almaty | 60,160 |
| Astana | 22,500 |
| Karaganda | 12,500 |
| Aktobe | 9,900 |
| Atyrau | 3,300 |
| Shymkent | 0 |

For task 12, the wording says "revenue" but does not explicitly repeat "paid only." Earlier revenue tasks do require paid orders, so paid-only totals are the consistent interpretation. Treat this as a point to clarify, not a definite grading failure. The dictionary restriction is attached to task 10; using a dictionary in task 12 is not itself a demonstrated violation.

| Day | Paid-only total | All-order total | Bars for paid total, 5,000 per bar |
| --- | ---: | ---: | ---: |
| пн | 20,490 | 20,490 | 4 |
| вт | 870 | 32,870 | 0 |
| ср | 12,500 | 68,500 | 2 |
| чт | 2,300 | 2,300 | 0 |
| пт | 27,900 | 27,900 | 5 |
| сб | 41,000 | 48,400 | 8 |
| вс | 3,300 | 3,300 | 0 |

## Before submission

1. Rename the savings accumulator and restart the kernel.
2. Recheck tasks 6, 7, 8, and 11 using the feedback above.
3. Write your own reflection for task 13.
4. Match the requested rounding and output formats.
5. Run all cells from a fresh kernel, check the outputs, and save.
6. Commit and push the updated notebook; verify the files on GitHub and arrange instructor access.

No replacement solution code or reflection was generated as part of this review.
