## Missed Trash Pickups

Get the data for this assignment here: https://drive.google.com/file/d/1PvGZkL3v9XkWL1QfiA6TgfCLAWjhfISs/view?usp=sharing. Open the data in Excel and then load Claude for Excel.

This exercise will highlight some of the limitations for Claude in Excel.

Start by simply asking Claude to explain the spreadsheet.

1) Follow the steps below to find what % of complaints are not about missed trash pickups and then to find the top 10 non-missed pickup complaints by count.

- Ask Claude how many complaints were not about missed trash pickups?  Record this answer.
- If it was not already provided, ask for a top 10 non-missed pickup complaints by count.  Do you see any issues?
- If you noticed any isses with Claude's output, ask about it and have it correct the errors.
- Repeat these 3 steps until you are satisfied.  It may take several iterations.
- What is the final answer?
- Which types of complaints did Claude miss?
- How would you ensure these errors do not slip into your workflow?


2) Update the spreadsheet with this new information.

- Ask Claude to create a new column between Description and Address name "Missed Pickup" and set the value in this column to TRUE or FALSE.
- Get a % of missed pick ups using this new column and compare it to the value above?  Do they match?


3) Use the new column for further analysis.

- Which Council District has the greatest number of TRUE values? Double-check Claude by using a pivot table.
- Which Council District has the greatest percent of TRUE values?
- Did any Council Districts have 100% of their complaints due to missed trash pick ups?
- Do the same with FALSE values.
- Find which trash hauler has the greatest percent of their complaints due to missed trash pick ups?
- Which address has had the greatest number of missed trash pick ups?

4) Fines

- You want Claude to calculate the fines according to the following rules:
  - Every missed trash pick up beyond the 2nd at a given address will result in a fine of $500 for the trash hauler.
- Take these results and create a new sheet in the workbook that contains the trash hauler and the total fine amount.

5) Create a Dashboard

- First, ask Claude how many days are covered in this data?
- Next ask Claude to make a dashboard for you choosing whichever metrics it thinks are more important.
- If Claude provided some rows with a grand total, double check that total.
- What are the good aspects of the final dashboard?
- What are the things that are not good?
- Could this dashboard be a good starting point to improve upon it or would it be better just to create your own from scratch?
