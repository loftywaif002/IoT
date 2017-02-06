# CrystalBall

<img src="https://image.ibb.co/iZsdFa/setup.jpg" height="350" width="200">
<img src="https://image.ibb.co/g6Z8Fa/schematic.jpg" height="300" width="400">

<p align="center">
  <h2> For Latest Arduino IDE </h2> <a href="arduino.cc/download">arduino.cc/download</a>  
</p>

<p align="center">
  <h2> Item List </h2> 
  <ul>
    <li>Switch</li> <img src="https://image.ibb.co/g7ZKMF/switch.png" height="50" width="50">
    <li>10k ohm Resistor</li> <img src="https://image.ibb.co/ieTDgF/resistor.png" height="50" width="100">
    <li>220 ohm Resistor</li> <img src="https://image.ibb.co/nDhjov/Screen_Shot_2017_02_06_at_11_16_08_AM.png" height="50" width="100">
    <li>Potentiometer</li><img src="https://image.ibb.co/cpPava/potentiometer.png" height="80" width="50">
    <li>LCD Screen</li><img src="https://image.ibb.co/c5u8Fa/lcd.png" height="80" width="150">
    <li>BreadBoard</li><img src="https://image.ibb.co/h2NpMF/breadboard.png" height="80" width="120">
    <li>JumperWires</li><img src="https://image.ibb.co/b3okva/jumper.png" height="50" width="50">
    <li>Arduino Uno</li><img src="https://image.ibb.co/etKEov/arduino.png" height="80" width="100">
  </ul>
</p>

<p align="center">
  <h2> Follow the schematic Design </h2>
  <ul>
     <li>Connect power</li>
     <li>Connect + vertical strip of the breadboard to the +5v in the arduino</li>
     <li>Connect - vertical strip of the breadboard to the GND in the arduino</li>
     <li>Wire the swtich as a digital input in the arduino, one end goes to +, another end goes to - in the breadboard as        well as to the pin 6 of the arduino for digital input</li>
     <li>In the schematic diagram RS(Register Select pin) in LCD controls where the characters should be displayed on the screen</li>
     <li> In the schematic, the read/write pin puts the lcd screen in read and write mode</li>
     <li>In the schematic the E pin will decide that the lcd will receive the commands </li>
     <li>The data pins in the schematic (D0-D7) is used to send characters to the screen </li>
     <li>The data pins in the schematic (D0-D7) is used to send characters to the screen </li>
      <li>To adjust the contrast of the lcd, we use a potetio meter where the center pin connects to V0 of the LCD and one end to the power and another to the ground </li>
      <li>according to the schematic, VSS and LED pins on both end of the LCD- connects to the ground</li>
      <li>However the LED+ shoudl connect to the 5v/ the + strip in the breadboard through a 220ohm resistor</li>
      <li>Also, the R/W pin should connect to the ground to enable wrtie mode</li>
      <li>Also, the R/W pin should connect to the ground to enable wrtie mode</li>
      <li>Then we connect arduino pin 2,3,4,5 to D7,D6,D5,D4 to send data from arduino to LCD</li>
      <li>The EN pin on the lcd connects to pin 11 on arduino board, this pin enables writing on the lcd</li>
      <li>Then we write the code below and send it to the arduino using the IDE</li>
  </ul>
</p>

<h1>Code Used</h1>
<code>
#include <LiquidCrystal.h>
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

const int switchPin = 6;
      int switchState = 0;
      int prevSwitchState = 0 ;
      int reply;
      
void setup(){
     lcd.begin(16,2);
     pinMode(switchPin,INPUT);
     lcd.print("Ask the,");
     lcd.setCursor(0,1);
     lcd.print("Crystal Ball!");
}

void loop(){

  switchState = digitalRead(switchPin);
  if(switchState != prevSwitchState){
    if(switchState==LOW){
      reply = random(8);
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("The Ball Says: ");
      lcd.setCursor(0,1);
      switch(reply){
      
        case 0:
        lcd.print("Tommorrow never dies");
        break;
        case 1:
        lcd.print("Its your Lucky Day!");
        break;
        case 2:
        lcd.print("Green is your color");
        break;
        case 3:
        lcd.print("Dont eat duck today");
        break;
        case 4:
        lcd.print("Go vegetarian");
        break;
        case 5:
        lcd.print("Think before you do!");
        break;
        case 6:
        lcd.print("Doubtful");
        break;
        case 7:
        lcd.print("Hi");
        break; 
      }
    }
  }
  prevSwitchState = switchState;
}

</code>

## License

MIT © 
