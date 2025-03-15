# Payment Setup Guide

## Overview
This guide explains how to set up automatic bank transfers for payments received through the OAuth Apps Marketplace. We use Stripe as our payment processor for secure handling of financial transactions.

## Prerequisites
- A Stripe account (sign up at https://stripe.com if you don't have one)
- Business bank account details
- OAuth Apps Marketplace admin access

## Steps to Set Up Bank Transfers

### 1. Create a Stripe Account
If you don't already have a Stripe account, create one at https://stripe.com.

### 2. Connect Your Bank Account in Stripe
1. Log in to your Stripe Dashboard
2. Go to Settings → Bank accounts and cards
3. Click "Add a bank account"
4. Enter your bank details:
   - Account holder name
   - Sort code
   - Account number
5. Verify your bank account following Stripe's instructions

### 3. Configure Stripe Payouts
1. In Stripe Dashboard, go to Settings → Payouts
2. Set your preferred payout schedule (daily, weekly, monthly)
3. Confirm the bank account for payouts

### 4. Connect Stripe to OAuth Apps Marketplace
1. In Stripe Dashboard, go to Developers → API keys
2. Copy your Publishable key and Secret key
3. In the OAuth Apps Marketplace admin panel:
   - Go to Settings → Payment Processing
   - Enter your Stripe API keys
   - Save settings

### 5. Automatic Payment Flow
Once configured, the payment process works as follows:
1. Customer makes a purchase (subscription or one-time)
2. Funds are collected through Stripe
3. Stripe applies its processing fee (typically 2.9% + $0.30 per transaction)
4. According to your payout schedule, Stripe automatically transfers funds to your connected bank account

## Important Security Notes
- Never share your Stripe Secret key
- Do not store bank details in application code or repository
- All payment data must be handled through Stripe's secure API

## Testing Payments
Use Stripe's test mode to verify the payment flow without processing real transactions before going live.

## Support
For payment processing issues, contact:
- Stripe Support: https://support.stripe.com
- OAuth Apps Marketplace support: (include support email)
