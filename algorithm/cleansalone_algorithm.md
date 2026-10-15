# CleanSalone: Step-by-Step Algorithm

1. Start the system and call InitialiseSystem to set all counters and crew loads to 0.
2. Set running to TRUE.
3. While running is TRUE, display the menu (1 Report, 2 Update, 3 Statistics, 4 Exit) and read the choice.
4. If the choice is 1, perform steps 5 to 14 (Submit Report).
5. Add 1 to totalReports and create a new reportID.
6. Read the location of the dump site.
7. Repeat until the waste type is Household, Plastic, Market or Hazardous; show an error each time it is not.
8. Repeat until the site size is Small, Medium or Large; show an error each time it is not.
9. Ask whether the site is near a drain and near a market or school, and store each answer as TRUE or FALSE.
10. Repeat until daysUnresolved is 0 or more.
11. Determine priority: if the waste is Hazardous, or the site is near a drain or market, or days are 3 or more, the priority is HIGH. Otherwise, if the size is Large or days are 2 or more, it is MEDIUM. Otherwise it is LOW.
12. Search the crews: for each crew with fewer than 3 jobs, calculate its distance to the site and remember the nearest one.
13. If a crew was found, add 1 to its load and set the status to ASSIGNED. If not, set the status to QUEUED.
14. Save the report, update the priority counter and display the confirmation.
15. If the choice is 2, read a reportID. If it is not found, or is already RESOLVED, show a message and return to the menu.
16. Otherwise mark the report RESOLVED, add 1 to totalResolved and reduce the assigned crew's load by 1.
17. Assign queued reports to free crews, HIGH first, then MEDIUM, then LOW.
18. If the choice is 3, count the queued reports, calculate the resolution rate (resolved divided by total, times 100) and display all statistics.
19. If the choice is 4, set running to FALSE. For any other choice, display "Invalid choice".
20. Return to step 3. When running is FALSE, display a goodbye message and stop.
