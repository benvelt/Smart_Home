# Smart_Home
project of creating a Smart Home

SmartBuilding is a next generation platform for managing IoT enhanced smart building. The platform serves as the controller and integration hub for modules, devices, controllers and sensors that will enable efficient and comfortable operation of the building.

Example 1:
Suppose we have a sensor for ambient noise and a controller that controls a noise cancelation device. The controller will subscribe to receive events of type NOISE_LEVEL in the specific location of interest. The sensor will send an event of type NOISE_LEVEL with additional data indicating noise level measured in dB(A).
The system will route the event to the controller who will act according to the event’s dB(A) value.

Example 2:
• A badge sensor will read and authenticate an employee identification badge. Sensor will then send an event of type ENTRANCE_REQUEST with
payload data specifying employee ID, sensor ID, Lock ID to be unlocked and a secure signature identifying the badge.
• A security controller subscribing to this specific event will receive the event, validate the secure signature to make sure it’s a legitimate badge for the given employee and then will decide if the a door should be unlocked to allow entrance.
• Security Controller will send an UNLOCK_ENTRANCE event with payload data containing lock id to be unlocked

OS used for developement is Linux. The project is also working in a multithreaded environment.
