# Smart-Crop-Customizable-Gardening-System-A-Grid-Layout-Approach-and-a-CNC-based-Design
Major project developed by Naga abhilash reddy, Katakam Ram Gopal Srikar and myself (Thakur Rishabh Singh)

Abstract:The ever-increasing population demands a higher yield of crops from the farmers. But the current yield rate might not be sufficient in the future and the quality of it may be compromised as well. However, this can be prevented if every household produces their own limited range of crops. Thus, we have written a paper which proposes an automated gardening system, which enables the user to produce a wide range of crops in a grid fashion, which is cost-effective and energy-efficient with minimum human interaction. The system consists of 3 axes controlled by Nema 17 stepper motors which helps it to navigate to each grid location to plant seeds, check moisture and water the crops. The type of seed to be planted at a particular grid location is determined by the user through an android mobile app which also allows the user to check the various parameters recorded by the sensors which are stored on the database. The seed planting is done using linear actuator mechanism, seed selection is achieved using servo motor and the watering of plants is controlled by relay and dc water pump. The Arduino mega serves as the controller to coordinate all the functions and real time clock module is used to enable automatic and regular watering of plants. The system has been implemented and tested for a 5x2 grid and the results are discussed in our paper.

My contribution:
 Developed Bluetooth reception function to get seed information from app (bluetooth_callback()) and integrated real
time clock (RTC) function for initiating moisture checking task at fixed intervals (reg_moisture_callback())
 Designed functions to help the bot navigate on a 5x2 grid and plant the appropriate seeds (seeding_start(int loc[])) with
the help of a servo based mechanism (plantSeed(int loc1)) 
 Developed a linked list using First-In-First-Out (FIFO) algorithm to schedule seeding based
on Bluetooth data (Classes Scheduler, Node) & parallelized the functions using Arduino thread library (callback functions main_callback(),  bluetooth_callback(), reg_moisture_callback())
 Achieved reliability rate of 80% in the bot’s operation tested for 50 trials, with limitations of
power cut, improper harvesting and calibration of the RTC.

This repository has the code which we implemented for the project.

Credits:
Naga abhilash reddy - for developing the android app Cultivating_bot.apk in MIT App Inventor and designing the mechanical structure and programming the steppers.
Katakam Ram Gopal Srikar - for developing the php server and implementing Esp_callback(), httppost() and reset() functions in the main program.
