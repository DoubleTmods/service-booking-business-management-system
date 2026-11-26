Service Booking and Business Management System

A Django web app where customers book appointments with a service business, such as a salon or barbershop, and the administrator approves, rejects or cancels them from a dashboard.

Learner: Tatenda Sean Mafigo · Student number: [] · Supervisor: MrJeff

Problem

Small service businesses often take bookings by phone or message, which leads to double bookings, missed requests and no clear record of customers. This system moves bookings online. Customers see the services and prices and request a time, and the administrator manages every request and monitors the business in one place.

Features
Customers register, log in and manage their contact details
Public services page showing each service with its duration and price
Customers request an appointment by choosing a service, date and time
Requests are blocked for times that are already taken or outside opening hours
Administrator approves, rejects or cancels bookings, and customers can cancel their own requests
Booking statuses: pending, approved, rejected, cancelled and completed
Administrator dashboard with today's and upcoming bookings, pending request count, and booking summaries
Administrator manages services, bookings (filtered by status and date) and customer records
Customer "My bookings" page showing their requests and statuses
User Roles
Role	What they can do
Customer	Register and log in, view services and prices, request appointments, view their own bookings and cancel their own requests
Administrator	Approve, reject or cancel bookings, create, edit and deactivate services, view customer records and booking history, use the dashboard and booking summaries
Tech Stack
Part	Technology
Language	Python 3.14
Framework	Django 6.1
Database	SQLite during development (may change before deployment)
Frontend	Django templates, HTML and CSS
Testing	Django test framework
Setup
Requirements
Python 3.14
Git
Installation
bash
git clone https://github.com/DoubleTmods/service-booking-business-management-system.git
cd service-booking-business-management-system
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
pip install -r requirements.txt
Environment variables

Copy the example file and fill in your own values:

bash
cp .env.example .env
Variable	Purpose
DJANGO_SECRET_KEY	Django secret key
DJANGO_DEBUG	True for development, False for production
DJANGO_ALLOWED_HOSTS	Comma-separated host names
DB_ENGINE, DB_NAME, DB_USER, DB_PASSWORD, DB_HOST, DB_PORT	Database connection
Database and demo data
bash
python manage.py migrate
python manage.py createsuperuser
python manage.py loaddata demo_data.json   # added with the demo data work package
Run the application
bash
python manage.py runserver

Open http://127.0.0.1:8000/

Running the Tests
bash
python manage.py test
Demo Accounts

Demo accounts are created by the demo data. Ask your supervisor for the login details; do not publish passwords in this file.

Project Documents
Document	Location
Proposal	docs/
Requirements (SRS)	docs/
Work Breakdown Structure	docs/
Design (ERD, URL map, wireframes)	docs/
Test plan	docs/
Screenshots

Screenshots of the main pages will be added once they are built.