# **Kerala IoT Challenge: Level-1**

# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1a7StPJyJS_xLxvAypo7lb9wxHR5HKGno/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int ledPin=10;   // define digital pin 10.

void setup() {
  pinMode(ledPin,OUTPUT); // define pin with LED connected as output.
}

void loop() {
  digitalWrite(ledPin,HIGH);  // set the LED on.
  delay(1000);                // wait for a second.
  digitalWrite(ledPin,LOW);   // set the LED off.
  delay(1000);                // wait for a second.
}

```

## Output

> The LED is blinked with a time interval of 1 second

<iframe src="https://drive.google.com/file/d/1_vFBUMslCSqiNlfPoc9ICI4rU2lpY0wn/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1aOzUVYDMJTpzoL7NUcoNC5oCRviyUSPb/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 10;
int yellowLED = 7;
int greenLED = 4;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(yellowLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
}

void loop() {
  digitalWrite(greenLED, HIGH);
  delay(5000);
  digitalWrite(greenLED, LOW);

  for (int i = 0; i < 3; i++) {
    delay(500);   // wait 5 seconds
    digitalWrite(yellowLED, HIGH);
    delay(500);
    digitalWrite(yellowLED, LOW);
  }
  
  delay(500);
  digitalWrite(redLED, HIGH);
  delay(5000);
  digitalWrite(redLED, LOW);
}
```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe src="https://drive.google.com/file/d/1aNLQ9esjV7VXee6iXbvcMZN3RidI1_2V/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

<iframe src="https://drive.google.com/file/d/1aRU9ASibO_EVZExIgvXuNEPUkLn4vJNc/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int BASE=2;  // the I/O pin for the first LED
int NUM=6;   // number of LEDs
void setup()
{
   for(int i=BASE;i<BASE+NUM;i++)     //for(i=2;i<8;i++){}
   {
     pinMode(i,OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for(int i=BASE;i<BASE+NUM;i++) 
   {
     digitalWrite(i,HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1aRS9UR71ErY2z8gHnOJLQbja9MWDuJ7g/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1b9a3Xh35Hpcn2YSD-GWkLJ5_ezjbtI0Q/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int pushButtonPin=7;
int ledPin=10;

void setup() {
  pinMode(pushButtonPin,INPUT);
  pinMode(ledPin,OUTPUT);
}

void loop() {
  int value=digitalRead(pushButtonPin);
  if(value==HIGH){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);
    }  
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe src="https://drive.google.com/file/d/1b75s8TpWnPmmIaZ2vRndma61RXcgMiC1/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

<iframe src="https://drive.google.com/file/d/1bCYx4HTTnR6r5ofHokuyqMCTUS1FaTIR/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzerPin=8;

void setup() {
  pinMode(buzzerPin,OUTPUT);
}

void loop() {
  digitalWrite(buzzerPin,HIGH);
  delay(5000);
  digitalWrite(buzzerPin,LOW);
  delay(2500);
}

```

## Output

> The Buzzer makes beep sound.

<iframe src="https://drive.google.com/file/d/1b9musasMSkpdPV0hUYHVFDwXQ5Z2pUTT/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bDv9XzsQwxKkAbMQ2d7FdhwT8368cu0T/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int redLED = 11;
int blueLED = 10;
int greenLED = 9;
int val;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(blueLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  for (val = 255; val > 0; val--)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  for (val = 0; val < 255; val++)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe src="https://drive.google.com/file/d/1bDF6kjx_ksgmsZ-uUJKtRNaVgUGCyKvK/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

## LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bYp2eFOM836RWwWW7p76h9Ws8N3Npqee/preview" width="640" height="480" allow="autoplay"></iframe>

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

int ledPin=11;
int LDRPin=A0;
int value=0;

void setup() {
  pinMode(ledPin,OUTPUT);
  //pinMode(LDRPin,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(A0);
  Serial.println(value);
  if (value<50){
    digitalWrite(ledPin,HIGH);
    }
  else{
    digitalWrite(ledPin,LOW);  
    } 
}

```

## Output

<iframe src="https://drive.google.com/file/d/1bWcJMEvDCdi6tGUzNEvNiH0hdSdv85ZH/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 8 : Flame Sensor

> An experiment to understand the working of an Flame sensor.

## Flame Sensor

 **Usage**:These types of sensors are used for short range fire detection and can be used to monitor projects or as a safety precaution to cut devices off / on.

 **Range**:I have found this unit is mostly accurate up to about 3 feet.

 **How it works**:The flame sensor is very sensitive to IR wavelength at 760 nm ~ 1100 nm light.

**Analog output (A0)**: Real-time output voltage signal on the thermal resistance.

**Digital output (D0)**: When the temperature reaches a certain threshold, the output high and low signal threshold adjustable via potentiometer.

**Pins:**

* VCC - Positive voltage input: 5v for analog 3.3v for Digital.

* A0 - Analog output

* D0 - Digital output

* GND -  Ground

## Components Required

* Arduino UNO
* Flame Sensor
* LED
* Buzzer
* BreadBoard
* Jumper

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1cxmamxl2GsNSdq9oZYFPBJLoNjNiGGSX/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int buzzer=9;
int flame=A0;
int value=0;

void setup() {
  pinMode(buzzer,OUTPUT);
  pinMode(flame,INPUT);
  Serial.begin(9600);
}

void loop() {
  value=analogRead(flame);
  Serial.println(value);
  if(value>100){
    digitalWrite(buzzer,HIGH);
    }
  else{
    digitalWrite(buzzer,LOW);
    }  
}

```

## Output

<iframe src="https://drive.google.com/file/d/1crfYcVQjOEZs8XEKlhNs_esmtOyULyZQ/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 9 : LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

## LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor. LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing. LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1bhtQHqxbl2Hrli0SFZcpkpcB68WiRoc-/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor

void setup()
{
  Serial.begin(9600);// set baud rate at”9600”
}

void loop()
{
  int val;// define variable
  int dat;// define variable
  val = analogRead(0); // read the analog value of the sensor and assign it to val
  dat = (125 * val) >> 8; // temperature calculation formula
  Serial.print("Temp: ");// output and display characters beginning with Tep
  Serial.print(dat);// output and display value of dat
  Serial.println("°C");// display “C” characters
  delay(500);// wait for 0.5 second
}

```

## Output

<iframe src="https://drive.google.com/file/d/1bcseeXimEUsC-M9T-TZLl_irFxF7SUrn/preview" width="640" height="480" allow="autoplay"></iframe>       


# Experiment 10:IR Remote Control Using TSOP

> An experiment to understand the working of IR Remote Control using TSOP.

## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1VLwls4a8qDIQT4JF4tfTY3Eyr_G-rSy8/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

#include <IRremote.h>
int RECV_PIN = 13;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
long on1  = 0x40BF30CF;
long off1 = 0x40BF10EF ;
long on2 = 0x40BF18E7;
long off2 = 0x40BF38C7;
long on3 = 0x40BF7A85;
long off3 = 0x40BF5AA5 ;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i%2) == 1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
//  pinMode(LED4, OUTPUT);
//  pinMode(LED5, OUTPUT);
//  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
//       on = !on;
//       digitalWrite(8, on ? HIGH : LOW);
//       digitalWrite(13, on ? HIGH : LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);      
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}



```

## Output

<iframe src="https://drive.google.com/file/d/18r4ElvlKp73HMx_YoQ693pg7zJrsT5Dh/preview" width="640" height="480" allow="autoplay"></iframe>


# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1kyB57-gy38jwMJYV64Le3A7HMszeaK0M/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```

void setup() {
  pinMode(A0,INPUT);
  Serial.begin(9600);
}

void loop() {
  int value=analogRead(A0);
  Serial.println(value);
  delay(1000);
}

```

## Output

<iframe src="https://drive.google.com/file/d/1kvbY5FXLrZJDjJPoV1iAetbvJJHrYI1P/preview" width="640" height="480" allow="autoplay"></iframe>

# Experiment 12 : 7 Segment Display
        
> An experiment to understand the working of 7 Segment Display.

## Components Required

* Arduino Uno Board*1
* digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1

## Circuit Diagrams

<iframe src="https://drive.google.com/file/d/1l7lTHtJwW6tuEQGShJlKGWVZCq8XbVZL/preview" width="640" height="480" allow="autoplay"></iframe>

## Code

```
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 9
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}


```

## Output

<iframe src="https://drive.google.com/file/d/1l13DCYrQZ1uhAb0sOxh2xnbH38Xu9Z1j/preview" width="640" height="480" allow="autoplay"></iframe>

# Assigenments

## Assigenment  1- Night lighting system 


> An experiment to prototype a night ligting system.

### Components
* Arduino Uno
* Breadboard
* RED,GREEN LED
* Jumper wire
* Restsor 220 ohm 10 k
* LDR Sensor

### Circuit

<iframe src="https://drive.google.com/file/d/1lUYA0-UbfrYyGOoQif-xRGF1wISazxC5/preview" width="640" height="480" allow="autoplay"></iframe>

### Video

<iframe src="https://drive.google.com/file/d/1l_4iXTNj2CNAefJXnJpuU4RRh-MPKdhY/preview" width="640" height="480" allow="autoplay"></iframe>

### Code
```

#define LDR A0
#define LED 12

void setup() {
  pinMode(LDR,INPUT);
  Serial.begin(115200);
}

void loop() {
  int value=analogRead(LDR);
  Serial.println(value);
  delay(1000);
  if(value>800){
    digitalWrite(LED,HIGH);
    delay(1000);
    }
  else{
    digitalWrite(LED,LOW);
    delay(1000);
    }  
}


```

## Assigenment 2 - 6 Number Random Dice


> For a dice random numbers from 1-6 is required but I took numbers from 0-9.

### Components
* Arduino Uno
* Breadboard
* pushbuttion
* Jumper wire
* Restsor 220 ohm
* push buttion

### Circuit

<iframe src="https://drive.google.com/file/d/1lUJ8w3sh6rKqiSFNrE_08SyQyH88l8k_/preview" width="640" height="480" allow="autoplay"></iframe>

### Video

<iframe src="https://drive.google.com/file/d/1lSfDRG9heKJsdru7ROcSp8j8h9r82MO9/preview" width="640" height="480" allow="autoplay"></iframe>

### Code
```

//for a dice numbers 1-6 is enough but I took from numbers 0-9.
int readPin = 4;
bool buttonState = 0;
int time = 500;        //can set the time to t=0 sec,but not working efficiently.
int sevenSeg[] = {13, 12, 11, 10, 9, 8, 7, 6};   
/*
a=7
b=6
c=11
d=12
e=13
f=8
g=9
*/

//display number 0
void digital_0() {
  digitalWrite(sevenSeg[0], HIGH);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], LOW);
  digitalWrite(sevenSeg[5], HIGH);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}

//display number 1
void digital_1() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], LOW);
  digitalWrite(sevenSeg[5], LOW);
  digitalWrite(sevenSeg[6], LOW);
  digitalWrite(sevenSeg[7], LOW);
}

//display number 2
void digital_2() {
  digitalWrite(sevenSeg[0], HIGH);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], LOW);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], LOW);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}

//display number 3
void digital_3() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], LOW);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}


//display number 4
void digital_4() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], LOW);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], HIGH);
  digitalWrite(sevenSeg[6], LOW);
  digitalWrite(sevenSeg[7], HIGH);
}


//display number 5
void digital_5() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], HIGH);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], LOW);
}


//display number 6
void digital_6() {
  digitalWrite(sevenSeg[0], HIGH);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], LOW);
  digitalWrite(sevenSeg[5], HIGH);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], LOW);
}


//display number 7
void digital_7() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], LOW);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], LOW);
  digitalWrite(sevenSeg[5], LOW);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}


//display number 8
void digital_8() {
  digitalWrite(sevenSeg[0], HIGH);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], HIGH);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], HIGH);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}


//display number 9
void digital_9() {
  digitalWrite(sevenSeg[0], LOW);
  digitalWrite(sevenSeg[1], HIGH);
  digitalWrite(sevenSeg[2], HIGH);
  digitalWrite(sevenSeg[3], LOW);
  digitalWrite(sevenSeg[4], HIGH);
  digitalWrite(sevenSeg[5], LOW);
  digitalWrite(sevenSeg[6], HIGH);
  digitalWrite(sevenSeg[7], HIGH);
}


void setup() {
  Serial.begin(9600);

  for (int i = 0; i < 8; i++) {
    pinMode(sevenSeg[i], OUTPUT);
    digitalWrite(sevenSeg[i], HIGH);
  }
}

void loop() {
  buttonState = digitalRead(readPin);
  if (buttonState == HIGH) {
    int ran = random(0, 10);
    if (ran == 0) {
      digital_0();// display number 2
      delay(time);// wait for 2s
    }
    if (ran == 1) {
      digital_1();// display number 1
      delay(time);// wait for 2s
    }
    if (ran == 2) {
      digital_2();// display number 2
      delay(time);// wait for 2s
    }
    if (ran == 3) {
      digital_3();// display number 3
      delay(time);// wait for 2s
    }
    if (ran == 4) {
      digital_4();// display number 4
      delay(time);// wait for 2s
    }
    if (ran == 5) {
      digital_5();// display number 5
      delay(time);// wait for 2s
    }
    if (ran == 6) {
      digital_6();// display number 6
      delay(time);// wait for 2s
    }
    if (ran == 7) {
      digital_7();// display number 2
      delay(time);// wait for 2s
    }
    if (ran == 8) {
      digital_8();// display number 2
      delay(time);// wait for 2s
    }
    if (ran == 9) {
      digital_9();// display number 2
      delay(time);// wait for 2s
    }
  }
  /*else
  {
    digitalWrite(sevenSeg[0], LOW);
    digitalWrite(sevenSeg[1], LOW);
    digitalWrite(sevenSeg[2], LOW);
    digitalWrite(sevenSeg[3], LOW);
    digitalWrite(sevenSeg[4], LOW);
    digitalWrite(sevenSeg[5], LOW);
    digitalWrite(sevenSeg[6], LOW);
    digitalWrite(sevenSeg[7], LOW);
  }*/
  
}
```
