# ds5500-hw4

## Overview

This homework assignment continues to use school data from the previous assignment.

Download the 2015-16 district-level fiscal data from the National Center for Education Statistics’ Common Core of Data:
• https://nces.ed.gov/ccd/f33agency.asp

The 2015-16 performance statistics on graduation rate and state assessments on mathematics and reading/language arts are available from the EDFacts website:
• https://www2.ed.gov/about/inits/ed/edfacts/data-files/index.html

Additionally, the 2015-16 district-level “universe” survey data provides statistics about enrollment disaggregated by demographics like gender, race, disability status, etc:
• https://nces.ed.gov/ccd/pubagency.asp

These datasets can be linked based on the LEA IDs.

### Problem 1

For the districts you selected for budget cuts in HW 3 Problem 4, calculate and visualize the proportion of
each district’s total funding that will be lost.

Which districts will be affected by your budget cuts the most?

Philadelphia City SD, CLARK COUNTY SCHOOL DISTRICT & Los Angeles Unified will have the highest percentage of budget cuts in amount. 

But if take the proportions, for all the schools which has budget cuts it will have the same proportion because of the solution proposed.

To explain on that, to do the budget cut after we filtered schools on a particular criteria,
1. Calculate the 15% of the total budget amount -> fifteen_percent_fed_budget
2. For each potential case, we take the ('TFEDREV' of a case)/Sum of all ('TFEDREV' of a case) -> percentage_cut
3. percentage_cut * fifteen_percent_fed_budget to get value for each potential case -> budget_cut_for_a_case
4. If we put all in one formula:
   (('TFEDREV' of a case)/Sum of all ('TFEDREV' of a case)) * fifteen_percent_fed_budget =  budget_cut_for_a_case
5. To calculate proportion, we have to calculate budget_cut_for_a_case/('TFEDREV' of a case) which will be equal to fifteen_percent_fed_budget/Sum of all ('TFEDREV' of a case)) which is a constant


### Problem 2

A common problem with purely data-driven solutions is that they can inadvertently perpetuate hidden pre-existing biases in the data, and further disadvantage groups that are already disadvantaged. Calculate the proportion of enrolled students by race for each district, then visualize the distributions of these for districts that received budget cuts versus districts that did not receive budget cuts. Comment on whether the the distributions appear to be the same or different. Did your selection include any hidden biases, or manage to avoid them?

![alt text][logo_2]

[logo_2]: https://github.com/karangm-dev/ds5500-hw4/blob/master/output/2.png "Fig: Race Proportions for Budget vs No Budget Cut"

You can clearly observe race - BL_Proportion proportion budget cut is significantly higher in the districts that received budget cuts and for other races like WH - there are observable differences.


### Problem 3

Calculate the proportion of enrolled students by disability status (students with an IEP under IDEA) for each district, then visualize the distributions of these proportions for districts that received budget cuts versus districts that did not receive budget cuts.

Comment on whether the the distributions appear to be the same or different. Did your selection include any
hidden biases, or manage to avoid them?

![alt text][logo_3]

[logo_3]: https://github.com/karangm-dev/ds5500-hw4/blob/master/output/3.png "Fig: Distribution of Disability for Budget Cut vs No Budget cut"

The proportion distribution for budget cut districts and no budget cut districts seems to be very close to each other.

### Problem 4

Choose and critique one of your fellow classmates’ selection of schools for budget cuts in HW 3 Problem 4 and Problem 5. What was the justification of their selection? Discuss any advantages or disadvantages of their approach.

I chose https://github.com/manvitamarkala/DS-5500-HW3

The solution presented did not consider any performance related criteria to identify which of them should have budget cuts. However a surplus was calculated from the total budget a school has and the corresponding expenditure. Sort the districts descending on the surplus budget. If the surplus amount is greater than the federal budget for that particular district, a value equal to a federal amount of that district is substracted from the 15 percent federal budget amount. 

In a way the solution is appreciable for a fact that only those will be chosen where fedral budget wouldn't matter. However it that could have been combined with a powerful selection critieria, it may have been more effective.

### Problem 5
Summarize and comment on what you learned from one the special topics lectures (MapReduce + Hadoop, Visualization, Causal Inference, or the Industry Panel) of your choice.

I would like to talk about the MapReduce + Hadoop lecture. The lecturer started off with clear explanation of why we need Map Reduce kind of environment to process Big Data. The explanation was in simpler terms and even a student with no prior knowledge can get a clear understanding. He also threw in some important facts about how Map Reduce was originally started by a professor in Northeastern University. Overall a nice lecture.
