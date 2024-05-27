# financial-calculator-extension

As per this given table, I want you to create a Google Chrome extension application 
which is basically calculator a financial functional calculator

where the User is only able to add loan amount, Loan tenure, and loan processing fees.
once this data is updated in the field the rest results will come automatically.

so below are the exact details as mentioned in the table attached to the screenshot

I will also tell you the formula behind it 
you just have to give me the code which is required for an extension app.


1. Loan Amount =  ex 5000 This is the amount that the user can change as per requirement from the client. it can be anything.

2. Loan Tenure = 12 weeks, as this is a weekly Equated installment "EWI" it can be changed ex 8 weeks or 10 weeks, or 12 weeks

3. Processing fees = 12% with 18% GST on it, this also may change from 10% to 12% and 14%


these fields user can update these manually and the rest will show the results 
as I mentioned below with the formula 

next comes is Disbusral amount after entering the above fields 
=C2-C2*C8*1.18
C2 is a 5000 loan amount 
C8 is a 12% processing fee with *1.18 GST on it

processing fees in amount as below 
=C8*C2/1
C8 is processing fees here ex 12% which may change as per the clients profile 
C2 is Loan amount / 1

next is GST 
=C11*C9/1
C11 is 18% GST on processing fees which is 12%
C9 is processing fees / 1

next comes weekly ewi "Equated Weekly Installment"
=PMT(F8/52,F5,-C2)+((7*C2*F8/365)/F5)

PMT is the formula used here for calculating financial product
F8 is the Rate of Interest which is 36% Per Annum / 52
F5 is Loan tenure which is 12 Weeks
C2 is the Loan amount which is 5000

next is the Rate of Interest is 36% which is fixed and it should be in read-only mode

next is the total repayable amount in EWI as mentioned below 
=F2*F5
F2 is the EWI amount for every week
F5 is Loan tenure which is 12 weeks 


Next is Total charges with PF+GST 
=SUM(C12+C9)
C12 is GST in amount
C9 is processing fees in the amount 

Next is total amount with charges 
=F2*F5+C14
F2 is EWI amount weekly 
F5 is loan tenure 
C14 is total charges PF+GST


here is the complete formula and everythis i have given you 

but make sure user can only change Loan amount, Loan tenure, Processing fees.
still rest things will be same as it is 
and in read-only mode
when the user updates the loan amount, processing fees, and loan tenure
then he needs to click on Calculate button 
once he clicks on calculate button 
all the rest blank field get filled automatically as per the formula basis and show the exact details to the user.


hope you understood what I am looking for 

## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with React and Chakra UI.

- Vite
- React
- Chakra UI

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/financial-calculator-extension.git
cd financial-calculator-extension
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
