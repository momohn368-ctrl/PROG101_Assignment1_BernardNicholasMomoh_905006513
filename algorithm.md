# WasteWatch SL – Step-by-Step Algorithm

**Problem:** Waste piles up in Freetown's streets, drains and markets because collection capacity is limited and there is no simple way to decide which sites to clear first.

**Goal:** Take reports of waste piles from the community, give each one a priority (URGENT, HIGH or ROUTINE), recommend an action, and give the council a daily summary showing how many truck trips are needed.

## Main algorithm

1. Start.
2. Set the constants: rainy season is May (5) to October (10); warning = 3 days; critical = 7 days; URGENT score = 8; HIGH score = 4; truck capacity = 10 load units.
3. Ask for the current month. If it is not between 1 and 12, show an error and ask again.
4. Decide whether it is the rainy season (month is from 5 to 10).
5. Ask how many reports there are today. Repeat the question until the number is valid.
6. Set all counters (urgent, high, routine, total load units, total days) to 0.
7. **For each report**, do steps 8–15:
8. Enter the report ID and community name.
9. Enter the waste type (1 Household, 2 Plastic, 3 Market/Organic, 4 Hazardous). Repeat until it is valid.
10. Enter the pile size (1 Small, 2 Medium, 3 Large). Repeat until it is valid.
11. Enter the number of days the pile has been left uncollected (0–60). Repeat until it is valid.
12. Answer Y/N: Is it near a drain or stream? Is it near a school, market or health centre?
13. Calculate the priority score:
    - 7 or more days uncollected → +3 points; 3–6 days → +2 points
    - Large pile → +2; Medium pile → +1
    - Near a drain → +2
    - Near a public place → +2
    - Hazardous waste → +3
    - Rainy season **and** near a drain → +1
14. Classify the report:
    - Hazardous waste → URGENT, whatever the score
    - Otherwise: score 8 or more → URGENT; score 4–7 → HIGH; score 0–3 → ROUTINE
15. Recommend an action, display the report, add 1 to the matching counter, and add the pile's load units (Small 1, Medium 3, Large 8) and its days uncollected to the totals.
16. After all reports are done, work out:
    - truck trips needed = total load units ÷ 10, **rounded up**
    - average days uncollected = total days ÷ number of reports
    - the percentage of reports in each priority level
17. Display the daily summary. If any report is URGENT, display a warning.
18. Stop.
