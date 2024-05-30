# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

[Bookstore Diagram.drawio.pdf](https://github.com/datatoinsights/sql/files/15500037/Bookstore.Diagram.drawio.pdf)


## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

The employee shift table has been added to the ERD above.

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
```


Type 1 stores no historical data, Type 2 stores all historical data. The two address tables have been added to the ERD above.

[Address Diagram.drawio.pdf](https://github.com/datatoinsights/sql/files/15500039/Address.Diagram.drawio.pdf)

Regarding privacy, there are two considerations:
1. Customer consent:
To keep customer's address data, the company should gain customer consent first. The address records should not be sold or given to third parties.
2. Regulations:
PIPIDA have regulations in regards to how long the cusotmer personal information can be kept by businesses. There should be a time limit on how long the address record can be kept for existing customers that have made purchases in the last few years. To decide what customers are considered current or elapsed, there shoud be discussions on the range of last purchase date. In case that the customer is elapsed, the historical record for the customer should not be kept.

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Your answer...
```
1. I would add special_order_id and unit_price_discount to the Sales table. This should be more applicable to real cases. It would be incomplete if there is no discount information available to the sales transaction.
   
2. For the address table, I would also add forgien key for province and country, then connects the Foreign Key fields to province table and country table respectively. This would make the province and country fields data cleaner.



# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `June 1, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-3-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
