# Architecture report
**last updated: 5 Dec**

---

[TOC]

---

## 1. Class Diagram
### Bank Implementation
The bank model works as real world banks.
So far, bank have two types of money:
   - physical
   - virtual

Whenever bank takes physical money from customer, it extracts that amount money from bank account and transfers it to the customer's account.

---

### Business Users Implementation
In the first meeting, team discussed how the system should work, and the types of users that will use the sytem.

The team decided to divide the system users in to two types:

   - `Customer` - persons who uses the system.
   - `Employee` - persons who operates the system.

And as  there are 2 types of employees:
   - `Admin` 
   - `Manager`

The team defined them by using `UserRoles` model.

#### Enums

To put boundary on models, we used several Enumerations.

---

### Business Sevice Implementation
In second meeting, team discussed to how system service will be implemented.
   1. Each `Customer` can have only one `Account` for payments and transfers. (At first, team didn't know that would they implement the joint account feature or not.)
   2. Each services works with `Transaction` in order to provide tracability of money, and storing all transfers that happened on the account. 

![](/diagrams/class_diagram/SystemModellingProject.png)

[Link to plantuml version](/diagrams/class_diagram/class_diagram.plantuml)

---

## 2. Use Case Diagrams

In these use cases, team together worked on logic of our project through the usage of Use Case Diagrams. For project, we decided each user story will have one use case diagram to make implementation process easier, and to make the easy to grasp the logic of our product.

### Account Logic

As a first thing the team started discussion about the Account part of the project. 

1) The team created the logic where bank employee creates account on behalf of the customer 
   ![](/diagrams/use_cases/4,5,6,7/4._Create_an_account_on_behalf_of_the_customer.png)
2) The team worked on where bank employee edits the account details.
   ![](/diagrams/use_cases/4,5,6,7/5_Modify_Account_Details.png)
3) The team worked on where customer themself edits the account details. 
   ![](/diagrams/use_cases/4,5,6,7/6_Edit_Account_Customer.png)
4) The team worked on where customer closes account.
   ![](/diagrams/use_cases/4,5,6,7/7._close_customer_s_account_usecase.png)

---
### Transaction Logic
1) Use case diagram for Deposit logic
   ![](/diagrams/use_cases/8_9_11_12/8.DepositUseCase.png)
2) Use case diagram for Withdrawl logic
   ![](/diagrams/use_cases/8_9_11_12/9.WithdrawlUseCase.png)
3) Use case diagram for Transfers logic
   ![](/diagrams/use_cases/8_9_11_12/11.Transfer_to_another_account.png)
4) Use case diagram for Mobile bank Transfers
   ![](/diagrams/use_cases/8_9_11_12/12.CustomerToCustomerMobileBankTransfer_Usecase.png)
5) Use case diagram for changing Transfer amount.
   ![](/diagrams/use_cases/13_14_15/13.1.Change_transfer_amount.png)

6) Customer deposits money to the bank 
   ![](/diagrams/use_cases/13_14_15/13.3.Change_deposit_amount_in_bank.png)
7) Customer cancels transaction.
   ![](/diagrams/use_cases/13_14_15/US14UC.png)
8) Admin sees the transaction logs
   ![](/diagrams/use_cases/13_14_15/15.Admin_see_transtion_logs.png)