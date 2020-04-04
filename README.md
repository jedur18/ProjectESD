# ESD project
**Project:** Motion Sensor Alarm (Group 2)
General Description: This project is divided in two groups. Group 1 will work with the motion sensor and will transmit a signal to the cloud when alarm is activated. Group 2 will work with the buzzer, display and keyboard in order to introduce the code to switch the alarm off.

**Group 2 description:** Our system will recive the signal of the activated alarm from the cloud by the LORA module. The idea then is to activate the buzzer to emit the sound. While the alarm is ringing the user will be able to introduce a secret code using the keyboard to switch the alarm off. In the display it will be showed the status of the system (Alarm ON/OFF), the code introduced and if it is correct or not.

**Distribution of the work:**
- EDU:
  - Basic part:
    - Numeric Keyboard: With this part digital I/O will be faced. I will also need to remove the bouncing of the buttons, deal with PCINTs (Pin change interruptions).
  - Individual Goals to reach 4/5 mark:
    - Display: SPI communication. Showing the system state, the code introduced by the user and if the code is correct or not.
    - Software protection--> Encryption. Asymmetric encryption if its possible (need to investigate on it)

- ALI:
  - basic part:
    - Buzzer: sendig out sound by the PWM signals as the LEDs.
    - LEDs control. Green:normal mode. Red:alarm mode. (LED blinking-->PWM)
  - More advansed part for us electronic backgrounded students is software development:
    - We are going to make the keypad unit and the sensor unit works as front end which will communicate to the back end server.
    - We are even going to make it possible for the system to be able to support more than one sensor and make it possibble for the master to identify which unit is detecting motions.


## EQUIPMENT:
- Murata CMWX1ZZABZLoRa Module:
	Datasheet:https://wireless.murata.com/datasheet?/RFM/data/type_abz.pdf
  - STM32L0x2:
		Documentation (Full information about micro): https://www.ece.uvic.ca/~ece355/lab/supplement/stm32f0RefManual.pdf
		With rust: https://docs.rs/stm32f0x2/0.1.0/stm32f0x2/

- Oled Display: SSD1306. 
	Datasheet: https://buildmedia.readthedocs.org/media/pdf/ssd1306/latest/ssd1306.pdf
	Website to order: https://cdon.se/hem-tradgard/oled-display-0-96-tum-med-128x64-vita-pixlar-i2c-ssd1306-p50542494
	Prize: 59kr
- Driver for Oled Display SSD1306
	Datasheet: https://cdn-shop.adafruit.com/datasheets/SSD1306.pdf
- LEDs: (Maybe available at lab)
	Red LED: https://se.rs-online.com/web/p/leds/2285988/
	Green LED: https://se.rs-online.com/web/p/leds/2286004/
- Numeric Keyboard:
	Website to order: https://www.elfa.se/en/3x4-matrix-keypad-adafruit-3845/p/30139179?queryFromSuggest=true
	Prize: 61.90kr
	Documentation: https://www.adafruit.com/product/1824
					https://www.futurlec.com/Keypad3x4.shtml
					Arduino libraries and documentation: https://playground.arduino.cc/Code/Keypad/
- Capacitors:
	6x100nF for decoupling: 
			for power supply:

- Resistors: 
	2x10k for pull Up and pull Down resistors for NRST and BOOT0: https://www.elfa.se/en/thick-film-smd-resistor-0805-10kohm-125mw-rnd-components-rnd-1550805s8f1002t5e/p/30056718?q=10k+resistor+0805&pos=1&origPos=1&origPageSize=10&track=true
	Prize: 0.4972 (ordering 4)
	for power supply: 
	
- Serial Wire Debug (SWD) to program and debug the MCU: 
	Website to oder: https://www.elfa.se/en/ampmodu-mod-ii-straight-male-pcb-header-through-hole-54mm-te-connectivity-826629/p/14371639?q=straight+male+pcb+header&pos=3&origPos=97&origPageSize=10&track=true
	Prize: 5.78SEK
	Datasheet:https://www.elfa.se/Web/Downloads/_t/ds/8266xx_x_eng_tds.pdf?pid=14371639

- Power Supply:

- Buzzer: 
  - piezo buzzer (KMTG1603-1) : https://se.rs-online.com/web/p/piezo-buzzer-components/7675349/?relevancy-data=636F3D3126696E3D4931384E53656172636847656E65726963266C753D7376266D6D3D6D61746368616C6C7061727469616C26706D3D5E5B5C707B4C7D5C707B4E647D2D2C2F255C2E5D2B2426706F3D31333326736E3D592673723D2673743D4B4559574F52445F53494E474C455F414C5048415F4E554D455249432673633D592677633D4E4F4E45267573743D4B4D5447313630332D31267374613D4B4D5447313630332D3126&searchHistory=%7B%22enabled%22%3Atrue%7D
    - Datasheet: https://docs.rs-online.com/aa51/0900766b81113b92.pdf
  - Transistor: (MMBT2222A)
    - Datasheet: https://www.elfa.se/Web/Downloads/_p/df/Diotec-MMBT2222A_eng_ger_tds.pdf?pid=30146837
    
    
 - num-pad:
   - Rectifier Diodes: https://www.elfa.se/en/rectifier-diode-1206-taiwan-semiconductor-ts4148-rxg/p/30139387?q=rectifier+diodes&pos=1&origPos=265&origPageSize=10&track=true
     - Datasheet: https://www.elfa.se/Web/Downloads/_t/ds/TS4148_RXG_eng_tds.pdf?pid=30139387
   - Buttons:
     - RND210-00204: https://www.elfa.se/en/pcb-tactile-switch-210-1no-57n-6mm-rnd-components-rnd-210-00204/p/30090660?q=Tactile+Switch&pos=5&origPos=16&origPageSize=10&track=true
     - Datasheet: https://www.elfa.se/Web/Downloads/_t/ds/RND%20210-00204_eng_tds.pdf?pid=30090660
   
 - Antenn con: https://www.elfa.se/en/micro-coaxial-straight-socket-micro-coaxial-connector-50ohm-6ghz-molex-73412-0110/p/30076410?queryFromSuggest=true
   - datasheet: https://www.elfa.se/Web/Downloads/_t/ds/73412-0110_eng_tds.pdf?pid=30076410
   
 - Micro-USB B connector: https://www.elfa.se/en/socket-micro-usb-smd-wuerth-elektronik-629105150521/p/30009163?q=micro+usb+smd&pos=4&origPos=4&origPageSize=10&track=true
   - Datasheet: https://www.elfa.se/Web/Downloads/40/32/629105150521.pdf?pid=30009163
   
 - Voltage Regulator:
   - LM1117ADJ: https://www.elfa.se/en/ldo-voltage-regulator-800ma-sot-223-texas-instruments-lm1117impx-adj-nopb/p/30019194?queryFromSuggest=true
   
 - LEDs:
   - Red:https://www.elfa.se/en/smd-led-640nm-1206-600mcd-30ma-kingbright-kptd-3216surc/p/17531032?q=*&pos=3&origPos=3&origPageSize=10&track=true
     - Datasheet: https://www.elfa.se/Web/Downloads/6_/en/csKingbright_SMD-LED-rot-KTPD3216_EN.pdf?pid=17531032
   - Green: https://www.elfa.se/en/smd-led-468nm-1206-700mcd-20ma-kingbright-kptd-3216qbc/p/17510753?q=*&pos=1&origPos=1&origPageSize=10&track=true
     - Datasheet: https://www.elfa.se/Web/Downloads/_t/ds/kptd-3216qbc-d_eng_tds.pdf?pid=17510753
   
