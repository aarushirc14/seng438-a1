# Assignment 1 - Lab Report

Group: 6

---

Jonathan

---

Dongwook (Luke)

---

Aarushi

---

Ahsan

---

[Introduction](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.2sfrssc4u6qg)

[High-level description of the exploratory testing plan](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.uzgmu0yhy6xf)

[Comparison of exploratory and manual functional testing](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.sr28xccmneil)

[Notes and discussion of the peer reviews of defect reports](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.qlbndtp12lpr)

[How the pair testing was managed and team work/effort was divided](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.qcy3f6s1irzd)

[Difficulties encountered, challenges overcome, and lessons learned](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.iy9lfbesuyxo)

[Comments/feedback on the lab and lab document itself](https://docs.google.com/document/d/1jD7jhX0Vvhps-CgdnxYMAjgIhVM6ihr7OKlF0aI-KBY/edit#heading=h.hcs1dknhaqj4)

# Introduction

In this lab, we are given the task of testing an ATM application under exploratory and manual functional testing (MFT) principles. The application has two versions - the initial release and an updated release that incorporates changes based on imaginary defect reports. This models an environment in which we can perform regression tests. MFT involves verifying a predetermined list of test cases to ensure that the basic requirements are functioning properly. In contrast, exploratory testing is a more open-ended approach where testers actively search for bugs and defects without following a rigid testing plan. The goal of this lab is to gain hands-on experience with software testing and gain a high-level understanding of different testing methods.

# High-level description of the exploratory testing plan

Our exploratory testing plan consisted of two pair testing groups. The first group in which one individual would be testing as a typical ATM user where one individual would be testing and the  other is reviewing and analyzing the results. The second pair testing group would act as an ATM thief, where the individual would take unconventional paths to try and exploit the machine. Each individual pair would alternate between testing and note taking to discover new perspectives.

**Typical ATM User Test Plan:**

For this method, we plan to use the basic testing methods, mimicking a normal ATM user. A rough overview of the test plan was as such:

1. Insert given card, typing the correct pin
2. Following that, the withdrawal functionality was tested, and later ejected the card
3. Re-insert and test the Deposit functionality, eject
4. Re-insert and test the Transfer functionality, eject
5. Re-insert and test the Balance Inquiry functionality, eject

**ATM Exploiter Test Plan:**

This individual would do more extensive testing the login and withdraw functionalities of the ATM. That being said, the deposit would still be considered but would not be the primary focus. Thus the following exploratory test cases were done:

1. Inserting a false card (entering non-numerical values or random numbers)
2. Entering an random/incorrect PINs
3. Checking to see if the chosen withdraw amount the same as the actual amount
4. Checking to see if the chosen withdraw amount is the amount deducted from the account
5. Trying to withdraw money from a unavailable account (Money Market for Card 1 and Savings for Card 2)
6. Trying to withdraw more money than you have in the account
7. Checking to see if the chosen deposit amount is accurately reflected in the balance
8. Checking to see what happens if a unrealistic deposit amount is entered
9. Checking to see if the amount transferred from one account to another is accurate
10. Checking to see if you could transfer money from a unavailable account to an available account

# Comparison of exploratory and manual functional testing

Exploratory testing is a process that utilizes a tester’s creativity, intuition and experience rather than well-defined testing scripts to guide the process. Starting with the exploratory tests first allowed the team to freely try different functionalities and become familiar with a system we had not used before. We caught most of the bugs during the exploratory testing phase and it allowed us to understand the requirements of the application before we proceeded to manual function testing (MFT). The manual functional testing was more rigorous and detailed than exploratory. It covered each function/use case and provided pre-defined information on the initial state of the system and expected outcome. MFT was more efficient as the test cases were performed systematically and split up between team members to avoid duplication and wasting time. However, there could be some trade-offs between MFT and exploratory testing. MFT requires testers to follow the scripts provided and this is rigid so some bugs in the application might get overlooked. Whereas exploratory allows the tester to try out more exceptional pathways or edge cases that may not be included in the MFT scripts. But exploratory testing can be inefficient. We noticed during this phase some of the issues in the Jira backlog were duplicates. As well, once a bug was discovered during exploratory testing, sometimes we had to repeat the steps so we could note down exactly what the initial state and inputs were to reach the error.

Since the ATM system was a simple application most of the bugs were discovered during the first phase of exploratory testing. However, for more complex applications, detailed test plans and scripts as provided in manual functional testing are required. Both styles of testing have their benefits and challenges so it's fair to say a good testing approach might be to use them in conjunction like we did in this lab. This would allow the greatest number of bugs to be caught and resolved, which is the ultimate goal of any QA team.

# Notes and Discussion of the Peer Reviews of defect reports

**Individual Feedback and Discussion Points:**

Aarushi:

- Backlog entries from each pair were reviewed by all team members. We noticed some of the entries lacked details regarding the initial state of the system, inputs needed to reproduce the error or had descriptions that needed clarification. We also noticed that sometimes a single test case or bug could be broken down into separate bugs due to overlap with other functionality or complexity.

Luke:

- After performing exploratory tests related to transfer functionalities, I found that a functionality that closely relates to an MFT test that passed was actually invalid. This may be because the MFT has a firm set of outlines which makes it easy to overlook surrounding functionalities. Maybe a future reference for this is to create more thorough MFT tests or to make sure and perform exploratory tests in related areas.

Jonathan:

- I felt our approach of acting as an ATM exploiter proves to be highly effective in identifying issues around the system that would not necessarily be identified through regular or manual testing. For example one of the bugs we managed to find was if you entered a deposit amount over $22 million it completely freezes the ATM making it unable to be used. This issue was not solved in ATM 1.1 and needs to be patched before the ATMs go public. Having the ATM freeze can have an effect on the physical hardware of the ATM machine or potentially leave the machine in a more vulnerable state. It also prevents other clients which may need to use the machine from interacting with it.
- Some backlog entries required further description as to the steps needed to reproduce an error but overall were all fairly original and informative. The added sections in which we could describe if the issue was still present in ATM 1.1 was also a great feature and make things more efficient.

Ahsan:

- Despite using pair testing, we were still able to spot some overlooked defects such as the log of transactions showing the incorrect card number (e.g 1 or 2). We found that because this defect was common across all test cases, it led to a lot of duplicates in the reporting. As future reference, it would be a better idea to review the reported bugs before proceeding to report defects.

## Pair Testing Results:

**Pair 1 (regular ATM Users):**

| Test | Expected Result | Actual Result |
| --- | --- | --- |
| Insert card, type correct pin | Accepted, logged in | Accepted, logged in |
| Attempt to log out of the system (cancel) | Card ejected | Card ejected |
| Withdraw sufficient amount | Withdraws selected amount and deducts from the balance correctly | Withdrawal amount did not match selected amount |
| Deposit acceptable amount | Deposits selected amount and updates balance correctly | Does not update total balance after a deposit |
| Transfer | Transfers entered value from correct account to correct account | Transferred value does not match the entered value. The “Transfer from” and “Transfer to” accounts are switched on the receipt. |
| Balance Inquiry card #1 (display accounts available) | Shows correct accounts available for the card | Does not display the correct accounts available for that card |
| Balance Inquiry card #2 (display accounts available) | Shows correct accounts available for the card | Does not display the correct accounts available for that card |
| Balance Inquiry (specific account selected) | Displays the full balance available for that account | Successfully displays the full balance available in that account |

**Pair 2 (ATM Exploiters) Results:**

| Test | Expected Result | Actual Result |
| --- | --- | --- |
| Inserting a false card (entering non-numerical values or random numbers) | Not Accepted | Not Accepted |
| Entering a random/incorrect PINs | Not Accepted | Not Accepted |
| Withdraw amount the same as the actual amount | Withdraw amount matches actual amount | Withdraw amount did not match actual amount |
| Withdraw amount is the amount deducted from the account | Withdraw amount matches deducted amount | Withdraw amount did not match deducted amount |
| Withdraw money from a unavailable account (Money Market for Card 1 and Savings for Card 2) | Display Error | Displayed “Invalid Account Type” |
| Withdraw more money than you have in the account | Displays error | Displays “Insufficient cash available” |
| Deposit amount is accurately reflected in the balance | Deposit amount is reflected in Balance | Deposit amount was not accurately reflected in Balance |
| Unrealistic deposit amount is entered | Display Error | Freezes ATM |
| Transferred money from one account to another is accurate | Balance in accounts is reflected accurately | Balance in accounts was NOT reflected accurately |
| Transfer money from a unavailable account to an available account | Display Error | Display “Invalid Account Type” |
| Transfer more money money than you have from one account to another | Display Error | Displays “Insufficient cash available” |

# How the pair testing was managed and team work/effort was divided

Following the guidelines of pair testing, the two pairs formed were:

1. Ahsan & Aarushi
2. Luke & Jonathan

Ahsan and Aarushi: The approach of the first pair was to split the features/functionality and go with the divide and conquer method. Aarushi focused on deposits and withdrawals while Ahsan checked the balance inquiry and system logs. They each updated the backlog with any bugs they found and double checked later for duplication.

Luke & Jonathan: Within the second pair, each person alternated between exploratory tests in different areas and note taking. Jonathan tackled the login and deposit based tasks while Luke tested the withdraw and transfer functions. The purpose of this was to distribute the tasks evenly in which we agreed this was fair. While one individual was testing, the other individual was writing down the steps taken, expected results and actual results. Additionally, pair testing allowed us to provide feedback during and after testing about other perspectives and approaches that needed to be considered.

For the manual functional tests, all the test cases were divided evenly between the team members and we each did ten tests. For the regression tests, each team member tested their MFTs and exploratory tests from the previous phases.

# Difficulties encountered, challenges overcome, and lessons learned

Teamwork was crucial to our success as various tasks were distributed among team members. Effective communication was a key factor in our success as we moved through the various phases of testing. After finishing a test, we realized the importance of thoroughly documenting any additional issues that were identified during the process in order to avoid repeated efforts. Another big lesson we learned was the importance of establishing explicit roles before beginning the testing process. We frequently went back and forth to confirm tasks and responsibilities, which stunted our progress. It would have been beneficial to create a shared outline that provides these details in advance.

One of the most important things we learned during the technical portions of the lab is the importance of spending more time to fully comprehend the problem definition and deliverables. In most cases, this can potentially save hours of extra work and decrease the need for iterative improvements. We also discovered how a professional engineering team might perform QA through several stages in order to test a system. The importance of regression testing was emphasized as certain functionalities remained invalid in the newer iteration of the application. We also learned that creating custom fields like: “Program Version: ATM 1.0, ATM 1.1”,  “Testing Type: EXP, MFT, REG”,  “Tested/Feature Function”, “Input”, “Expected Output” and “Faulty Output” in the bug tracking tool should be done prior to adding any entries. As we progressed through our testing, we continuously added new fields that were deemed useful. However, this required us to revisit and update older tickets to keep a consistent format. Making these fields mandatory ensured all backlog entries had the required information.

One significant challenge we encountered was the need to be very descriptive when documenting our testing logs such that bugs can be replicated consistently under the same conditions. Failure to do this could cause regression tests results to be unreliable. We learned that we should document the basic workflow of the application (Ex: from turning it on to inserting the card) as they were redundant in many of the tests we performed. In the future, it may be useful to separate these steps into their own sub-section in order to make the size of our individual bug reports shorter in the future.

# Comments/feedback on the lab and lab document itself

Luke:

It was a very intuitive way of learning how software testing works. I feel that it simulated a testing process in industry on a very high-level, and was very useful as an individual that isn’t well versed with quality assurance practices.

Ahsan:

Overall, the lab was a great introduction to software testing, broken down in simple coherent parts making it easy to understand for beginners. Requiring to use Jira/Azure was a handy upskill, especially for its uses in many real-world applications. Though this lab lacked difficulty, it was a great start, nonetheless, to some more complex testing methods to be later learnt in the course.

Aarushi:

The lab documents provided were detailed and mostly easy to follow. But instructions for the Regression Testing section could have been a bit clearer. The use of GitHub Classroom was a nice touch and in future labs it will provide an opportunity to learn version control for those that don’t know it. The tasks in this lab provided a high-level overview of the different types of testing possible and is a good introduction to testing.

Jonathan:

I especially appreciated the use of GitHub Classroom and real world defect tracking systems during this lab. Using Atlassian Jira was a great experience as I believe it helped me think more about how reporting defects works at a company. However, I found that having the lab report to be formatted via markdown restricted our ability to simultaneously develop and format our report in an appealing way. It would also be nice to have a copy of the rubric somewhere in D2L such as the Dropbox or Assignment 1 content page for easier access.