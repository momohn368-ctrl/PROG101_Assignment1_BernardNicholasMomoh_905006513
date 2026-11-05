# WasteWatch SL – Community Waste Reporting and Collection Priority System

PROG101 – Principles of Programming Logic and Design | Individual Assignment 1
Limkokwing University of Creative Technology, Sierra Leone – Semester 01 (September 2026 – January 2027)

Student: Bernard Nicholas Momoh  Student ID: `905003449`  

---

 1. **The problem**

Only about 21% of Freetown's waste is properly collected and disposed of. The rest is burned or dumped in streets, drains and waterways (Concern Worldwide, 2019). Waste in drains causes flooding in the rainy season and helps spread malaria and cholera. Trucks and crews are limited, and there is no simple, fair way to decide 'which waste piles to collect first'.

 2. **The solution**

WasteWatch SL is a 'logical design' for a system that takes community reports of waste piles and:

1. scores each report from 0 to 13 based on how long it has been left, its size, whether it is near a drain or a school, market or health centre, whether it is hazardous, and whether it is the rainy season;
2. classifies it as 'URGENT', 'HIGH' or 'ROUTINE' (hazardous waste is always URGENT);
3. recommends an action (collect within 24 hours or within 3 days, or add to the weekly round, plus recycling or composting advice);
4. produces a daily summary for the council showing counts, percentages, average days uncollected and the number of truck trips needed.


4. Programming logic used
- Decision structures: IF / ELSE IF / ELSE, SELECT CASE, nested IF
- Boolean logic: `rainySeason AND nearDrain`, `month >= 5 AND month <= 10`, `value < min OR value > max`
- Repetition: a FOR loop over all reports, and WHILE loops for input validation
- Modular design: `Main`, `GetValidInteger`, `GetYesNo`, `IsRainySeason`, `CalculatePriorityScore`, `ClassifyPriority`, `RecommendAction`, `GetLoadUnits`, `DisplayReport`, `GenerateDailySummary`
- Constants: `URGENT_SCORE = 8`, `HIGH_SCORE = 4`, `TRUCK_CAPACITY = 10`, and others

 5. Sustainable Development Goals

- SDG 11 (Sustainable Cities, target 11.6 on municipal waste) is the main goal.
- The design also supports SDG 3 (health), SDG 6 (clean water and sanitation) and SDG 12 (recycling and composting).

 6. Open source and Digital Public Good

The design is released under the 'MIT licence' so councils, NGOs and students can reuse and adapt it at no cost. It is designed to meet the Digital Public Goods Alliance standard: it is relevant to the SDGs, uses an open licence, is documented, protects privacy (no personal data about reporters) and is platform-independent.

 7. Licence
MIT – see `LICENSE`.
