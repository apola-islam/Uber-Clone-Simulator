# Simple Uber App Simulator

This was a course assignment that simulates Uber's core functionality; managing users, drivers, and service requests.

## Actions (On Command Line)

LOADUSERS: loads in pre-existing users from users.txt.

LOADDRIVERS: loads in pre-existing drivers from drivers.txt.

USERS: lists all users.

DRIVERS: lists all drivers.

REGUSER: adds a new user to the system.

REGDRIVER: adds a new driver to the system.

REQRIDE: requests a new ride request.

REQDLVY: requests a new delivery request.

REQUESTS: prints all existing requests.

CANCELREQ: cancels a request using request #.

DROPOFF:

PICKUP:

DRIVETO:

## Files

### `TMUberService.java`
Defines the base class `TMUberService`, which includes common functionality and attributes for different types of Uber services.

### `TMUberDelivery.java`
Inherits from `TMUberService` and adds functionality specific to food delivery requests. Includes:
- Attributes for restaurant and food order ID
- Methods for getting and setting restaurant and food order ID
- Overridden `equals` method to compare delivery requests
- `printInfo` method to print delivery details

### `TMUberRegistered.java`
Handles user and driver registration. Includes:
- Methods to generate unique user and driver IDs
- Methods to load users and drivers from files (`loadPreregisteredUsers` and `loadPreregisteredDrivers`)

### `User.java`
Defines the `User` class, which represents a user of the service. It includes attributes for user ID, name, address, and wallet balance.

### `Driver.java`
Defines the `Driver` class, which represents a driver. It includes attributes for driver ID, name, car model, car license, and address.

## Installation
Compile on a command line using 'javac TMUberUI.java' and then 'java TMUberUI'
### Prerequisites
- Java JDK 11 or higher

