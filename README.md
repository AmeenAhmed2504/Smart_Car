ARDUINO PIN CONNECTION
Pin	Function
13	Trig Pin (Triggers ultrasonic sensor)
12	Echo Pin (Receives echo from ultrasonic sensor)
7	Motor Control Pin (Controls the motor)
6	Buzzer Control Pin (Controls the buzzer)

Export to Sheets
Code Description:
This Arduino code implements an obstacle avoidance system using an ultrasonic sensor, a motor, and a buzzer.

Initialization:

trigPin, echoPin, motor, and buzzer pins are defined.
setup() function initializes the pins as input or output.
Ultrasonic Sensor Reading:

loop() function continuously reads the distance from the ultrasonic sensor.
A pulse is sent on the trigPin and the time taken for the echo to return on the echoPin is measured.
This duration is converted to distance in centimeters.
Obstacle Avoidance:

If the distance is less than 50 cm (adjust as needed), the motor is activated to avoid the obstacle.
A buzzer is also activated to provide an audible warning.
If the distance is greater than 50 cm, the motor and buzzer are deactivated.
Delay:

A delay of 500 milliseconds is introduced between readings to allow for sensor processing and motor/buzzer response.
