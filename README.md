# Pacflix Membership System

A Python-based application that manages user memberships and plan benefits for the Pacflix streaming service.

## Features

- Display available Pacflix membership plans and their benefits
- Check a user's current plan and plan details
- Upgrade a user's membership plan with applicable discounts
- Handle new user sign-ups with referral code validations

## Membership Plans

Pacflix offers three membership plans:

1. **Basic Plan**
   - Services: Stream, Download, SD Quality
   - Number of Devices: 1
   - Content Variety: 3rd party Movie Only
   - Price: Rp 120,000

2. **Standard Plan**
   - Services: Stream, Download, SD Quality, HD Quality
   - Number of Devices: 2
   - Content Variety: Basic Plan + Sports (F1, Football, Basketball)
   - Price: Rp 160,000

3. **Premium Plan**
   - Services: Stream, Download, SD Quality, HD Quality, UHD Quality
   - Number of Devices: 4
   - Content Variety: Basic Plan + Standard Plan + Pacflix Original Series
   - Price: Rp 200,000

## Study Cases

### Case Study 1: User Checks All Plan Benefits

```python
user_1 = User('Shandy', 'basic plan', 12)
user_1.check_benefit()
```

This case demonstrates how a user can view the details of all available Pacflix membership plans.

### Case Study 2: User Checks Current Plan Benefits

```python
user_2 = User('Cahya', 'standard plan', 24)
user_2.check_plan()
```

This case shows how a user can view the details of their current membership plan, including the plan name, duration, and the specific benefits included.

### Case Study 3: User Upgrades Membership Plan

```python
user_3 = User('Cahya', 'Standard Plan', 24)
user_3.upgrade_plan('Premium Plan')
```

This case illustrates how a user can upgrade their membership plan. The system calculates the discounted price based on the user's current plan and the duration of their subscription.

### Case Study 4: New User Signs Up with Referral Code

```python
faizal = New_User('Faizal_icikiwir')
faizal.pick_plan('basic Plan', 'bagus-9f92')
```

This case demonstrates how a new user can sign up for a Pacflix membership plan and receive a discount if they use a valid referral code.

## How It Works

The application is built using the `User` and `New_User` classes, which handle different aspects of the Pacflix membership system.

### `User` Class

The `User` class is responsible for managing existing user accounts. It has the following key features:

1. **Accessing User Information**: Users can check their current plan, plan duration, and plan benefits.
2. **Upgrading Plans**: Users can upgrade to a higher plan, with applicable discounts based on their current plan and subscription duration.
3. **Error Handling**: The class raises appropriate exceptions for invalid usernames and plan names.

### `New_User` Class

The `New_User` class is used for handling sign-ups of new users. It has the following key features:

1. **Viewing Plan Benefits**: New users can view the details of all available Pacflix membership plans.
2. **Signing Up with Referral Code**: New users can sign up for a plan and receive a discount if they provide a valid referral code.
3. **Error Handling**: The class raises exceptions for invalid plan names and referral codes.

## Dependencies

- `tabulate` library for displaying data in a formatted table

## Error Handling

The application includes error handling for the following cases:

- **Invalid Username**: Raised when the provided username does not exist in the system.
- **Invalid Plan**: Raised when the requested plan does not exist in the system.
- **Invalid Referral Code**: Raised when the provided referral code is not found in the system.

## Future Improvements

- Implement a more dynamic and extensible plan structure to easily add or modify plan details
- Introduce a database or file-based storage to persist user and plan data
- Add more advanced features like multi-user support, payment processing, and subscription management

## Contributing

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.