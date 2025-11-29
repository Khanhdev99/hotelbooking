📌 Detailed Requirements – Hotel Booking System for Travelers
I. Technology Stack
Backend

Node.js (Express or NestJS)

RESTful API architecture

Database

MongoDB using Mongoose ORM

Frontend

Mobile Application

Customer App (Hotel Guests)

Hotel Owner App

Both connect to the backend via REST API

Web Admin Panel

Built with React

Connected to Admin API endpoints

Third-Party Integrations

Payment Gateways

VNPAY (Vietnam)

Stripe (International)

Email OTP Verification

Gmail SMTP or mail server provider

AI Chatbot

Google Gemini API

II. Detailed Features
1. Customer (Mobile App)
1.1. Authentication & User Account

Sign up with email + password, with OTP verification via Gmail

JWT-based login (access token + refresh token)

Multilingual support: Vietnamese / English
→ Backend returns raw data, client handles localization

1.2. Hotel Discovery

Hotel listing filtered by star rating (3★, 4★, 5★)

Search hotels by:

Name

Location

Price

Room type

Provided services

Hotel Details Page:

Image gallery

Description

Room types (Standard, Deluxe, Suite…)

Pricing

Cancellation policies

Included services

1.3. Favorites

Add/remove rooms or hotels to Favorite List

1.4. Room Booking

Select:

Room type

Number of rooms

Check-in & check-out dates

Payment required before confirming booking (VNPAY / Stripe)

Successful booking → send confirmation email via SMTP

1.5. Booking History

View all past and upcoming bookings

Booking statuses:

Pending

Confirmed

Cancelled

Paid

1.6. Chatbot Assistant

AI chatbot (Gemini API) suggests hotels based on system database

1.7. Reviews & Ratings

Customers can:

Rate hotels (1–5 stars)

Post written reviews with images

View hotel average rating and detailed reviews

1.8. Membership Tiers

Based on total spending:

Silver

Gold

Diamond
→ Diamond users receive 5% discount on the total booking fee

2. Hotel Owner (Mobile App)
2.1. Hotel Profile Management

Register a hotel with:

Basic information

Business license

ID/Passport (CMND/CCCD)

Hotel must be approved by Admin before it becomes public

2.2. Room Management

Full CRUD operations for rooms:

Add, edit, delete

Upload images

Set price, description, facilities

2.3. Booking Management

View all bookings from customers

Manage booking statuses:

Pending confirmation

Confirmed

Cancelled

Hotel owner can approve or cancel bookings

2.4. Availability & Room Inventory

Manage room availability for each day

Update “Available / Sold Out” status

2.5. Revenue & Reports

Monthly and quarterly booking reports

Revenue analytics and insights

2.6. Customer Support

Chat with customers through in-app internal messaging

3. Admin (React Web Panel)
3.1. User Management

CRUD users (customers + hotel owners)

Role-based permissions:

Customer

Hotel Owner

Admin

3.2. Hotel Management

Approve newly registered hotels

Manage all hotels (CRUD)

3.3. Room Management

CRUD operations for all rooms across the system

3.4. Booking Management

View statistics for all bookings

Modify booking statuses

3.5. System Reports & Analytics

Total hotels, rooms, and bookings

Revenue reports (monthly, quarterly, yearly)

Membership tier statistics

3.6. Content Management

CRUD hotel reviews and ratings

Manage chatbot dataset:

Import structured hotel data into Gemini
