## Missed Trash Pickups

Get the data for this assignment here: https://drive.google.com/file/d/1PvGZkL3v9XkWL1QfiA6TgfCLAWjhfISs/view?usp=sharing. Open the data in Excel and then load Claude for Excel.

This exercise will highlight some of the limitations for Claude in Excel.

Start by simply asking Claude to explain the spreadsheet.

1) Follow the steps below to find what % of complaints are not about missed trash pickups and then to find the top 10 non-missed pickup complaints by count.

- Ask Claude how many complaints were not about missed trash pickups?  Record this answer.
  When asked "how many of non missed trash pickup" Ans: Trash - Curbside/Alley Missed Pickup:15,028 and Non-Missed Pickup requests: 5198 out of 20,226 (Trash- Backdoor:2,629, Trash Collection Complaint:2,312, Damage to Property:257). Claude used Request column to count.
- If it was not already provided, ask for a top 10 non-missed pickup complaints by count.  Do you see any issues?

  When asked Claude to list a top 10 non-missed pickup complaits by count, it used Description column for counting and separated count of Description contained Miss Missed, Miss, Missed. and Missed again separatedly. The Rank is not correct. Clude filtered only by the description in request type: Curbside/Alley Missed Pickup. 
  
- If you noticed any isses with Claude's output, ask about it and have it correct the errors.
  I asked claude to list a top 10 non-missed trash pickup complaints by count in request type that is not Curbside/Alley Missed Pickup, and count only description that are not contained miss.
  
- Repeat these 3 steps until you are satisfied.  It may take several iterations.
- What is the final answer?
  When excluded all miss descriptions, there are 2,487 complaints and only 2,186 unique descriptions.
  Rank
  1. 1 cart (count = 98)
  2. cart still out (count = 58)
  3. still out (count = 31) this should be combined with rank 2
  4. Paid service (count = 15)
  5. Backdoor pick up (count = 5)
  6. Backdoor (count = 5)
- Which types of complaints did Claude miss?
  Since discription are free-text with inconsistent wording, therefore, many complaints mean the same thing but use different phrasing and if claude is not suggested to used common variations and synonyms to group them together by meaning. When Claude grouped complaints by meaning. The result of 2,487 non-missed complaints detected as below:
  Rank
  1. Truck/driver behavior (count = 522)
  2. Need backdoor service (count = 294)
  3. cart not returned/ let out (count = 264)
  4. wrong day/schedule (count = 153)
  5. Yard/lawn damage (count = 114)
- How would you ensure these errors do not slip into your workflow?

I asked claude to explain how it will do to ensure there will not be some errors. This is a step by step instruction.
1. Define "missed" comprehensively
flag synonyms and implied meanings:
Direct: miss, missed, missing
Implied: "still out," "cart still out," "not picked up," "skipped," "passed," "never came," "didn't come," "no pickup," "no show," "forgot," "overlooked," "left behind," "not collected," "not emptied"
2. Exclude by both Request Type AND Description
First exclude Trash - Curbside/Alley Missed Pickup entirely, then filter out any remaining record where the description matches the expanded keyword list above
3. Normalize the descriptions
Lowercase, trim whitespace, remove punctuation. Group similar phrases (e.g., "cart still out" = "still out" = "cart out")
4. Validate with spot checks
Manually review a sample of records in each top complaint to confirm they truly aren't about missed pickups
Flags every record as "Missed" or "Not Missed" using an expanded keyword list (not just "miss" but also "not picked up," "skipped," "still out," "never came," etc.) for manual checking.
With the instruction, 2,012 records of non-missed trash pickup complaints and 18,214 records of missed trash pickup reports were detect and the most
Rank	Complaint Theme	             Count	%
1	    Truck / Driver Behavior	    292	  14.5%
2	    Backdoor Service Request	  232	  11.5%
3	    Cart Not Returned Properly	182	  9.0%
4	    Spilled Trash / Litter	    139	  6.9%
5	    Property Damage (Other)	    108	  5.4%
6	    Mailbox Damaged	             79 	3.9%
7	    Yard / Lawn Damage	         58	  2.9%
8	    Extra Trash / Overflow	     22	  1.1%
9	    Schedule / Wrong Day	       14	  0.7%
10	  Cart Damaged / Broken	       9	  0.5%   
2) Update the spreadsheet with this new information.

- Ask Claude to create a new column between Description and Address name "Missed Pickup" and set the value in this column to TRUE or FALSE.
- Get a % of missed pick ups using this new column and compare it to the value above?  Do they match?
  Total missed pickup complaints is 18,207 counts, 90.0%. It is not matched with the number Claude provided before adding Missed Pickup column.

3) Use the new column for further analysis.

- Which Council District has the greatest number of TRUE values? Double-check Claude by using a pivot table.
  Council DIstrict 25 has the greatest number of TRUE (1,156 reports), using a pivot table, council District 25 still has the greatest number of TRUE and the count no is matched.
- Which Council District has the greatest percent of TRUE values?
  Council DIstrict 25 has the greatest number of TRUE (93.5%)
  
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
