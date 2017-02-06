# KNOCK-LOCK
[![Everything Is AWESOME](https://preview.ibb.co/cAAOFa/IMG_0910.jpg)](https://youtu.be/PgSmZbtFHxg "Servo-knock-block")

<p align="center">
  <h2> For Latest Arduino IDE </h2> <a href="arduino.cc/download">arduino.cc/download</a>  
</p>

<p align="center">
  <h2> Item List </h2> 
  <ul>
    <li>Switch</li> <img src="https://image.ibb.co/g7ZKMF/switch.png" height="50" width="50">
    <li>LED(3- diffrent colors would be great)</li> <img src="https://image.ibb.co/cyvhaa/led.png" height="50" width="20">
    <li>10k ohm Resistor (1)</li> <img src="https://image.ibb.co/ieTDgF/resistor.png" height="50" width="100">
    <li>220 ohm Resistor (3)</li> <img src="https://image.ibb.co/nDhjov/Screen_Shot_2017_02_06_at_11_16_08_AM.png" height="50" width="100">
    <li>1 Mega ohm Resistor(1)</li> <img src="https://image.ibb.co/cONTFa/1mOhm.png" height="50" width="100">
    <li>100 uF capacitor</li><img src="https://image.ibb.co/iJc61F/capacitopr.png" height="80" width="50">
    <li>Servo motor</li><img src="https://image.ibb.co/fNXTFa/servo_motor.png" height="50" width="70">
    <li>Piezo</li><img src="https://image.ibb.co/j2gc8v/piezo.png" height="80" width="120">
  </ul>
</p>

<h3>A Piezo when connected to 5v, can detect vibrations that can be fed in the arduino as analog input, and from there we can process the data to check if the number of knock is within the range we defined </h3>

<p>
 <ul>
  <li>On both ends of the bread board, the vertical strips should be connected to the 5v and GND pin in the arduino</li>
  <li>Put a switch on the board, 1 end goes to the "-" strip of the board, anther end goes to pin 2 (PWM), another end goes to "-" strip of the board through a 10khm resitor</li>
  <li>A peizo has to pins, one end goes to "+" stip of 5v on the board,the other goes to A0 pin on the arduino boaed as well as "-" strip of the bread board through a 220 ohm resistor </li>
  <li>Add leds, the cathode (short-leg) goes in the "-" strip or ground and 220 ohm resistor series with all the anodes</li>
  <li>Connect the resitors to Arduino pin, 3,4 5</li>
  <li>Connect the servo motor's red wire to 5v strip on the bread board and black wire to the "-" strip / ground</li>
  <li>Connect a 100 uF capacitor to handle irregularities in the voltage</li>
  <li>Coonect the middle or white wire of the servo motor to the Arduino pin 9</li>
 </ul>
</p>

<a href="https://gist.github.com/loftywaif002/c4ed06e710eab1a9c3b16d78d807a0a6">See The Code Here</a>
## License

MIT © 
