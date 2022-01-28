# Architecture Report

### Contributors: 

- Adil
- Anneli
- Ashfaq
- Bill
- Boomika
- Enrih
- Jason
- Kamil
- Masud
- Matin
- Pabasara
- Rauno
- Sammar
- Sarp

#### Our open bank is called KaiBank.

Kai means "open" in Mandarin, and KaiBank is truly an open source bank. It is the world's first no-fee bank. Deposits, withdrawals, transfers--all transactions are free for our customers.

#### This document summarizes the architecture of KaiBank.

Our first task toward defining the architecture of KaiBank was to hold an event storming session. 

![event storming diagram](resources/event-storming-diagram.jpg)

The entire diagram can be found [here](https://miro.com/app/board/o9J_ljct2SI=/)

Our next task was to begin writing user stories for KaiBank. This was very much an iterative process where we would envision the features of KaiBank, write user stories to capture those features, create a backlog to begin developing those features, and then go back and modify our user stories to fit our refined and enhanced vision.

A full list of user stories is located [here](user-stories.md).

Our main users are:

- Johan Johansson, KaiBank admin
- Mike Russell, KaiBank customer service representative
- Jesse Smalls, KaiBank customer

Full user personas can be found [here](architecture_report/user-personas.md).

The architecture of KaiBank became clearer after the event storming session and our initial set of user stories were written. Our architecture owners then began working on the class diagram for KaiBank before any development took place.

![KaiBank class diagram](diagrams/class_diagram/SystemModellingProject.png)

# note for architecture report authors: must somehow tie in the fact that KaiBank utilizes a model-view-controller architecture. 

# note for architecture report authors: must also mention bi-directional referential integrity 

The next step was to create use case diagrams and sequence diagrams are based on our user stories. For the sake of convenience, we list the user story followed by the use case diagram and sequence diagram representing that user story. Some user stories have multiple permutations. See [this list](user-stories.md) for a detailed view.

### 4. As a bank employee, I want to create an account on behalf of the customer.

![Create an account on behalf of the customer use case diagram](/diagrams/use_cases/4,5,6,7/4._Create_an_account_on_behalf_of_the_customer.png)

![Create an account on behalf of the customer sequence diagram](diagrams/sequence_diagrams/4-7/4.Create_an_account_on_behalf_of_the_customer.png)

### 5. As a bank employee, I want to modify customer's account details.

![Bank employee modifies profile online banking on customer's behalf use case diagram](/diagrams/use_cases/4,5,6,7/5_Modify_Account_Details.png)

![Bank employee modifies profile online banking on customer's behalf sequence diagram](diagrams/sequence_diagrams/4-7/5.modifying_customers_account_details.drawio.png)

![Customer modifies profile online banking sequence diagram](diagrams/sequence_diagrams/4-7/5.BankEmployeeModifies_Customer_Details.drawio.png)

### 6. As a customer, I want to modify my account details with online banking.

![Bank employee closes customer's account use case diagram](/diagrams/use_cases/4,5,6,7/6_Edit_Account_Customer.png)

![Bank employee closes customer's account sequence diagram](diagrams/sequence_diagrams/4-7/6.user_modifying_theirs_account_details.png)

### 7. As a bank employee, I want to close customer's account.

![Bank employee deposits money on customer's behalf use case diagram](/diagrams/use_cases/4,5,6,7/7._close_customer_s_account_usecase.png)

![Bank employee deposits money on customer's behalf sequence diagram](diagrams/sequence_diagrams/4-7/7._Close_customer_s_account.png)

### 8. As a bank employee, I want to deposit money into a customer's account

![Bank employee withdraws money on customer's behalf use case diagram](/diagrams/use_cases/8_9_11_12/8.DepositUseCase.png)

![Bank employee withdraws money on customer's behalf sequence diagram](diagrams/sequence_diagrams/8-12/8_Deposit.drawio.png)

### 9. As a bank employee, I want to withdraw money from customer's account on request

![Customer ATM withdrawal use case diagram](/diagrams/use_cases/8_9_11_12/9.WithdrawlUseCase.png)

![Customer ATM withdrawal sequence diagram](diagrams/sequence_diagrams/8-12/9_Withdrawal.drawio.png)

### 11. As a customer, I want to transfer money in a branch.

![Customer in-branch transfer use case diagram](/diagrams/use_cases/8_9_11_12/11.Transfer_to_another_account.png)

![Customer in-branch transfer sequence diagram](diagrams/sequence_diagrams/8-12/11_Transfer_to_another_account.png)

### 12. As a customer, I want to transfer money via mobile banking.

![Customer mobile bank transfer use case diagram](/diagrams/use_cases/8_9_11_12/12.CustomerToCustomerMobileBankTransfer_Usecase.png)

![Customer mobile bank transfer sequence diagram](diagrams/sequence_diagrams/8-12/12_Mobile_Bank_Transfer.png)

### 13. As a bank employee, I want to modify a transaction so that I can handle transaction requests.

![Bank employee modifies customer's transaction use case diagram](/diagrams/use_cases/13_14_15/13.1.Change_transfer_amount.png)

![Bank employee modifies customer's transaction use case diagram](/diagrams/use_cases/13_14_15/13.3.Change_deposit_amount_in_bank.png)

![Bank employee modifies customer's transaction sequence diagram](diagrams/sequence_diagrams/13-15/13.ModifyTransaction.png)

### 14. As a Bank Employee, I want to cancel a customer’s transaction on his behalf

![Bank employee cancels transaction on customer's behalf use case diagram](/diagrams/use_cases/13_14_15/US14UC.png)

![Bank employee cancels transaction on customer's behalf sequence diagram](diagrams/sequence_diagrams/13-15/US14SD.png)

### 15. As an admin I want to see transaction logs so that I can know by whom and when the transaction modification request is processed. 

![Admin views transaction logs use case diagram](/diagrams/use_cases/13_14_15/15.Admin_see_transtion_logs.png)

![Admin views transaction logs sequence diagram](diagrams/sequence_diagrams/13-15/15.Admin_see_transactions.png)




# Front end wireframes:

![GUI wireframes](diagrams/wireframes/gui_wireframes_v1.jpg)

![GUI wireframes](diagrams/wireframes/gui_wireframes_v2.png)
