# Pacflix Subscription Management

A simple program to manage subscription plans and benefits for a fictional streaming platform called Pacflix. This program allows existing and new users to view plan benefits, check current plans, upgrade plans, and select plans using referral codes.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Study Cases](#study-cases)
- [License](#license)

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/pacflix-subscription.git
Install required dependencies:
bash
Copy code
pip install tabulate
Usage
Run the program using Python:

bash
Copy code
python main.py
The program will execute a series of study cases to demonstrate its features.

Features
The program consists of two main classes:

User:
Attributes:
username: Name of the user.
current_plan: The user's current subscription plan.
duration_plan: Duration of the subscription in months.
Methods:
check_benefit(): Displays available subscription plans and their benefits.
check_plan(): Displays the user's current plan benefits.
upgrade_plan(new_plan): Allows the user to upgrade their plan with a discount if the subscription is over 12 months.
New_User:
Attributes:
username: Name of the new user.
Methods:
check_benefit(): Displays available subscription plans and their benefits.
pick_plan(new_plan, referral_code): Allows a new user to select a plan and get a discount if a valid referral code is provided.
Study Cases
Study Case 1: User Checks All Plan Benefits
In this case, an existing user (Shandy) checks the available plans and their benefits. This showcases the available features of each subscription tier.

python
Copy code
user_1 = User('Shandy', 'basic plan', 12)
user_1.check_benefit()
Study Case 2: User Checks Current Plan Benefits
Here, another user (Cahya) checks their current subscription plan's benefits and details.

python
Copy code
user_2 = User('Cahya', 'standard plan', 24)
user_2.check_plan()
Study Case 3: User Upgrades Their Plan
An existing user (Cahya) decides to upgrade their current subscription from the Standard Plan to the Premium Plan. If the user has been subscribed for over 12 months, they receive a 5% discount.

python
Copy code
user_3 = User('Cahya', 'Standard Plan', 24)
user_3.upgrade_plan('Premium Plan')
Study Case 4: New User Picks a Plan with Referral Code
A new user (Faizal) signs up and chooses a plan using a referral code. The referral code provides a 4% discount if valid.

python
Copy code
faizal = New_User('Faizal_icikiwir')
faizal.pick_plan('basic Plan', 'bagus-9f92')
License
This project is licensed under the MIT License.
