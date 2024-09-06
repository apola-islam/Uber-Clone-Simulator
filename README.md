# Simple Uber App Simulator

This was a course assignment that simulates Uber's core functionality; managing users, drivers, and service requests.

## Some Actions (On Command Line)

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

DROPOFF: completes a request using request #.

PICKUP: changes drivers location to pickup location.

DRIVETO: changes drivers location to specified address.

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

### `CityMap.java` 
Represents a 9x9 grid city layout, with:
Streets (east-west) numbered from 1st to 9th.
Avenues (north-south) numbered from 1st to 9th.
It provides methods to handle addresses, calculate distances, and determine zones within the city.

### `TMUberUI.java`

The class allows for users to enter in commands, which it processes according to the defined actions and functions. 

### `TMUberSystemManager.java`
The main logic controller for the simulator. It manages the registration of users and drivers, handles ride and delivery service requests, and tracks their completion. The class includes methods for adding new users and drivers, requesting and canceling services, managing driver assignments, and calculating revenue from completed rides and deliveries. It also provides functionality for sorting and listing users, as well as updating driver locations. Custom exceptions are used throughout to handle errors.

## Installation
Compile on a command line using 'javac TMUberUI.java' and then 'java TMUberUI'
### Prerequisites
- Java JDK 11 or higher

