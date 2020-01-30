ESD project
Project: Motion Sensor Alarm (Group 2)
General Description: This project is divided in two groups. Group 1 will work with the motion sensor and will transmit a signal to the cloud when alarm is activated. Group 2 will work with the buzzer, display and keyboard in order to introduce the code to switch the alarm off.

Group 2 description: Our system will recive the signal of the activated alarm from the cloud by the LORA module. The idea then is to activate the buzzer to emit the sound. While the alarm is ringing the user will be able to introduce a secret code using the keyboard to switch the alarm off. In the display it will be showed the status of the system (Alarm ON/OFF), the code introduced and if it is correct or not.

Distribution of the work:
-EDU:
	Basic part:
		- Numeric Keyboard: With this part digital I/O will be faced. I will also need to remove the bouncing of the buttons, deal with PCINTs (Pin change interruptions).
		-LEDs control. Green:normal mode. Red:alarm mode. (LED blinking-->PWM)
	Individual Goals to reach 4/5 mark:
		-Display: I2C communication. Showing the system state, the code introduced by the user and if the code is correct or not.
		-Software protection--> Encryption. Asymmetric encryption if its possible (need to investigate on it)

-ALI:

EQUIPMENT: 