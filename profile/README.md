# EX-DATA WORLD

EX-DATA WORLD is a real Nigerian VTU and digital services platform for Data, Airtime, Cable TV, Electricity, Exam PIN and other digital services.

## 🚀 Features

- User Registration
- User Login
- User Dashboard
- Wallet
- Fund Wallet
- Data Purchase
- Airtime Purchase
- Cable TV Payment
- Electricity Payment
- Exam PIN
- Transaction History
- Referral System
- User Profile
- English / Hausa Language Support
- OPay Payment Integration
- PostgreSQL Database
- JWT Authentication
- Secure Password Hashing

## 📱 Data Services

Supported networks:

- MTN
- Airtel
- Glo
- 9mobile

Example plans:

- 500MB — ₦150
- 1GB — ₦300
- 2GB — ₦600
- 5GB — ₦1,500
- 10GB — ₦3,000

Prices can be changed from the backend/provider configuration.

## 💳 Wallet

Every registered user has a wallet.

Wallet features:

- Current Balance
- Fund Wallet
- Wallet Credit
- Wallet Debit
- Pending Transactions
- Successful Transactions
- Failed Transactions
- Transaction History

The frontend must never be allowed to directly increase a user's balance.

Wallet balance must only be changed by the secure backend after a verified transaction.

## 💰 OPay Payment

EX-DATA WORLD is designed to integrate with the official OPay API.

Official OPay Developer Documentation:

https://documentation.opayweb.com/

Payment flow:

Customer
↓
EX-DATA WORLD
↓
OPay
↓
Payment
↓
OPay Verification
↓
Webhook
↓
Backend Verification
↓
Wallet Credit
↓
Transaction History

Never trust a frontend payment-success message.

The backend must verify the payment before crediting the user's wallet.

Duplicate payment references must not be processed twice.

## 🔐 Security

The application uses:

- JWT Authentication
- bcrypt Password Hashing
- Protected API Routes
- PostgreSQL
- Environment Variables
- Backend Authorization
- Webhook Verification
- Duplicate Transaction Protection
- Input Validation

Never put secret keys inside:

- index.html
- style.css
- app.js
- GitHub frontend files

Never publish:

- OPay Secret Key
- JWT Secret
- Database Password
- API Credentials
- User Passwords
- OTP
- PIN

## 🗄️ Database

The production database uses PostgreSQL.

Main tables include:

- users
- wallets
- wallet_transactions
- provider_transactions
- virtual_accounts
- data_orders
- airtime_orders
- cable_orders
- electricity_orders
- exam_orders
- referrals
- webhook_events

## 👤 Registration

Users register with:

- Full Name
- Username
- Email Address
- Phone Number
- NIN
- Password
- Referral Code (Optional)
- Terms and Conditions

Passwords are hashed before being stored.

Sensitive identity information must be protected.

## 🔑 Login

Users can log in using:

- Username
- Email
- Phone Number

Authentication is handled by the backend using JWT.

## 👥 Referral System

Every user can have a unique referral code.

Example: just used username as it

Example Abus3355

Referral links can be generated automatically.

Referral rewards must be controlled by the backend and must not be manipulated from the frontend.

## 📺 Cable TV

Supported services:

- DSTV
- GOtv
- Startimes

The application should verify customer information before completing payment where the provider supports verification.

## ⚡ Electricity

The application supports:

- Prepaid Electricity
- Postpaid Electricity

Users provide:

- Distribution Company
- Meter Number
- Meter Type
- Amount

Customer/meter verification should be performed through the real provider API.

## 🎓 Exam PIN

Supported exam services may include:

- WAEC
- NECO
- NABTEB
- JAMB

Exam PINs must only be delivered after successful provider confirmation.

Never generate fake PINs.

## 🧾 Transactions

Every transaction should contain:

- Transaction ID
- User ID
- Type
- Amount
- Status
- Provider
- Provider Reference
- Description
- Date
- Created At

Transaction statuses:

- pending
- successful
- failed
- cancelled

Users can only access their own transactions.

## 🌐 Language

The application supports:

- English
- Hausa

Users can switch languages from the application interface.

## 🎨 Design

EX-DATA WORLD uses a premium fintech design.

Primary style:

- Black
- White
- Gold

The interface is:

- Mobile-first
- Responsive
- Clean
- Modern
- Professional
- Easy to use

## 📂 Project Structure

```text
EX-DATA-WORLD/
│
├── index.html
├── style.css
├── app.js
├── server.js
├── package.json
└── README.md
