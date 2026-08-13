![Uploading Mishika D.jpg…]()
# Light-Up Robotic Arm

My vibrant light-up robotic arm glows different colors for each segment of my robot. Each color lights up in response to the robot's movement. The turntable lights up blue, the arm lights up green, and the claw lights up red. The robot operates using I2C, which allows my Nano board to communicate with my Nano ESP32 board. My Nano ESP32 receives information from my Nano, which tells it to light up LEDs based on the robot's movement.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Mishika D | Cupertino Highschool  | Bio/Biomedical Engineering | Incoming Freshman

<img width="429" height="572" alt="Mishika D (3)" src="https://github.com/user-attachments/assets/eae78f6b-93c8-4616-90a1-24527dfa3412" />


# Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/-RiEY3I1qWA?si=6qZp5qu1kOw35wU6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> 

# Final Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZKKGAXcAkhQ?si=GAgxgriwa98hc6Mu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<img width="318" height="416" alt="Screenshot 2026-07-29 143711" src="https://github.com/user-attachments/assets/7e910cc6-974f-452b-907e-2475c6b17943" />


# Description
I completed my modifications for my third milestone. I successfully added LEDs to my robot, which turn on based on the robot's movement. I also designed a case to house my breadboards.

# Before the Build
In the beginning, I simulated how this modification would go using Tinkercad. I initially wanted my LEDs to light up based on servo movement, so to mimic that, I added a potentiometer (since there was no joystick) and servos along with the LEDs. I also wrote code based on the movement of the servos. During this process, I learned how current flows through breadboards and applied it to my LEDs. Since this was just a simulation, I was able to test how LEDs would react when I changed their resistance and location on the breadboard. During this time, I learned the difference between wiring in series vs parallel.  

# Building my Modification
When I started the actual build of my modification, I realized it would be much easier to have my code read the joystick position rather than the servo position. This is because my original code already reads the position of the joystick, which correlates to movement on my robot. Also, my previous code was written based on the potentiometer, which meant I had to change aspects of my code at some point, which would take time away from my build. Using my original code made debugging and troubleshooting simpler since I knew how it would react alongside my robot. I also changed some of the wiring when attaching my LEDs to my breadboard. For example, due to the amount of wires, I changed the location of some of the LEDs for convenience. Learning how power flows through breadboards was really important too, especially since the top half of the breadboard does not automatically get power even when the bottom half does. 

# I2C
Using I2C, I got my original nano board to communicate with an additional nano esp 32, which currently drives my LEDs. I2C is a common communication protocol that helps transmit data between different devices. I chose to implement I2C because I can easily add more modifications in the future since this mechanism allows for multiple "master" and "slave" devices. Not to mention, this method of communication does not require many wires, which adds to its usefulness. My "master" board was my Nano located on my robot. This microcontroller contained code signaling my robot to move and told the LEDs when to light up. My "slave" board was my Nano ESP32, which lit up my LEDs.

# Programming 
Most of the challenges I faced lay in the program of the robot. As I mentioned before, my LEDs would blink when they were not supposed to. While fixing this issue, I learned how to write debug code and use the serial monitor. This was incredibly helpful since most of the issues I faced weren't directly written in the code. By writing debug code, I was able to read outputs from the serial monitor and fix my issues. 


# Challenges 
This part of my project had many challenges. To start, my code had a dead zone which stated that if the value on the joystick was not 512 (center), then the robot was in motion. When I added my LEDs, I found that the dead zone value had changed. This caused my LEDs to blink rapidly rather than stay still. I overcame this by writing debug code and adding a range of values rather than a specific number. I also found that wiring in series sometimes would not work. While it worked on my simulation, sometimes wiring more than 1 LED in series caused too much resistance, and it wouldn't light up. I faced an issue with the wiring too. When wiring the power line from the top and bottom of the breadboard, I accidentally wired power to ground rather than power to power and ground to ground. I realized this when my robot froze when it was supposed to be in motion. Attaching my LEDs to my robot was a challenge due to the amount of wires I needed. Each LED needed 2 jumper wires, and I had to double the length (the wires had to be long since the LEDs had to reach the robot). In the future, I aim to make a case for my robot so the wires are protected or use Bluetooth to reduce the wire usage. I enjoyed constructing and designing this project, and I am eager to see what projects I will work on in the future. 




# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/FrV4J9Y4CQE?si=83UWknsjZBa5xKt_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


# Description + Challenges 
My second milestone was achieving motion on my robot and completing the wiring. The only wiring required for my robot was for the servos (which I already did to set them to 90 degrees) and the controller. Thus, I finished wiring really fast and decided to finish the programming aspect instead of adding my modifications. Initially, I decided to have my modifications as the second milestone and have the program as the last. As I worked on the wiring for this milestone, the programming came consecutively, which led me to change my plans. I also wanted to apply my modifications by themselves as a separate milestone. The program, which is written in C++, directs the robot to move faster when the joystick moves faster and vice versa. It also goes over the buzzer feature, in which a sound will be made when an action is memorized and when it acts out this recorded action. A problem I faced was that some of the screws holding the servos in place became loose. This was due to the power of the servos, as the screws provided were slightly too short. I decided to replace some of these screws with mini zip ties since I wouldn't have to worry about any screws coming out. To add on, I found that female-female wires can be used to connect the batteries to the robot. This is a much better idea than soldering since it is not permanent and can easily be removed if necessary.  

# What's next?
For milestone 3, I want to add the modifications that I thought of when creating my build plan. The modification I want to focus on involves LEDs. I am hoping to add different colors of LEDs around my robot and have certain colors light up when certain actions are performed. If time permits, I will CAD a case for the controller since it is currently only attached by the wires. 





# First Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/MZYBzXjo5vc?si=ej4jDvrsS-FzDc1A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


# Description + Challenges
Completing the build of my robot was my first milestone. Before starting the assembly of the robot, all servos needed to be set to 90 degrees. This is done by uploading code to the robot that states which pins the servos are located on and sets the servos to 90 degrees. Without setting them, the position of your servos is unknown. This means when you assemble the robot, it won't have its full range of motion. This robot utilizes 1 servo beneath the base of the robot to rotate the arm. This servo is located between the turntable, which is used to support the base that the arm stands on. Two servos are located in the middle of the arm; they control how far forward and backwards the arm moves. The last servo is located at the top of the arm, and it moves one side of the claw up and down. The gear on this side of the claw is in contact with the other gear on the other claw, thus moving both sides while only utilizing one servo. 
I overcame many challenges during this assembly. For example, while building my robot, I didn't set my servos. At this point, I had already attached 3 out of the 4 servos, and I ended up having to deconstruct a lot of my robotic arm. While this was tedious, it got me familiar with the robot. Keeping track of parts was also important. The screws used for the servos were extremely small, so I had to make sure not to accidentally lose any. To add on, I didn't have access to the lithium batteries necessary to power the robot. Instead, I used a single 9V battery as the power source. Also, some of the screws were located in awkward places, and so it was hard to properly attach some parts. An example of this was one side of the claw (the side not attached to the servo). I had to add 2 bearings, my claw, and three washers through the screw before using a nut at the end to secure it. 

# What's next?
For my next milestone, I am aiming to complete my modifications. My main modification is to add LEDs that light up based on the movement of the robot. If I have extra time, I will CAD a case for my controller using Onshape. 

# Schematics + CAD

DISCLAIMER: My LED schematics were a rough draft and my final program may not match the original setup found in this design. 

<img width="822" height="640" alt="Screenshot 2026-07-29 142229" src="https://github.com/user-attachments/assets/dfc0fee4-81ae-4fa1-9e74-b42b6e405eaa" />
<img width="824" height="628" alt="Screenshot 2026-07-29 142514" src="https://github.com/user-attachments/assets/a4f8c52b-b001-40f2-81f6-42cdf8c29703" />

<img width="774" height="599" alt="Screenshot 2026-07-29 142712" src="https://github.com/user-attachments/assets/87233872-78c3-4135-af19-5a14ad4e096c" />

<img width="759" height="518" alt="Screenshot 2026-07-29 150332" src="https://github.com/user-attachments/assets/2f3419ee-c32d-437d-8c19-39643d059ea1" />




# Code

```c++
// I2C Master


// IMPORTS
#include <Wire.h> // the required Wire Library for I2C
#include "src/CokoinoArm.h" // the required CokoinoArm class


// define booleans to be sent over I2C
bool isRed; // should the red LED be on?
bool isGreen; // should the green LED be on?
bool isBlue; // should the blue LED be on?

// this is where I create my arm class, and I call it arm. 
CokoinoArm arm;

// define input strength variables
// xL is movement of the left joystick along the x-axis
// yL is movement of the left joystick along the y-axis
// xR is movement of the right joystick along the x-axis
// yR is movement of the right joystick along the y-axis
int xL, yL, xR, yR;


void setup() {
  Serial.begin(9600); // begin serial communication at 9600 baud
  // start the I2C Bus as Master
  Wire.begin();
  //arm of servo motor connection pins
  arm.ServoAttach(4,5,6,7);
  //arm of joy stick connection pins : xL,yL,xR,yR
  arm.JoyStickAttach(A0,A1,A2,A3);
}


void loop() {

  // update the input strength variables by reading the joysticks
  xL = arm.JoyStickL.read_x();
  yL = arm.JoyStickL.read_y();
  xR = arm.JoyStickR.read_x();
  yR = arm.JoyStickR.read_y();

  // limit each joystick input to one-axis at a time.
  date_processing(&xL,&yL, 523, 507);
  date_processing(&xL,&xR, 523, 514);
  date_processing(&xR,&yL, 514, 507);

  // move the arm according to the input strength variables,
  // and updates the LED booleans to their intended information
  turnUD();
  turnLR();
  turnCO();

  // send three boolean values to the slave.
  // the slave must call Wire.read() in the exact same order.
  Wire.beginTransmission(9); // transmit to device #9
  Wire.write(isRed);
  Wire.write(isGreen);
  Wire.write(isBlue);
  Wire.endTransmission(); // close transmission
}


////////////////////////////////////////////////////////////////////////////////

// function handles the up and down control of the arm via joystick. 
// additionally, it determines whether the respective (green) LEDs should be on.
// turnUD is short for turn Up-Down

void turnUD(void){

  if ((xL<519) || (xL>529)) { // is there up-down movement of the joystick?

    isGreen = true; // update isGreen: we want the green LEDs to be on.

    //pushing harder on the joystick increases speed of the arm (up and down)
    if(0<=xL && xL<=100){arm.up(10);return;}
    if(900<xL && xL<=1024){arm.down(10);return;}
    if(100<xL && xL<=200){arm.up(20);return;}
    if(800<xL && xL<=900){arm.down(20);return;}
    if(200<xL && xL<=300){arm.up(25);return;}      
    if(700<xL && xL<=800){arm.down(25);return;}
    if(300<xL && xL<=400){arm.up(30);return;}
    if(600<xL && xL<=700){arm.down(30);return;}
    if(400<xL && xL<=480){arm.up(35);return;}
    if(540<xL && xL<=600){arm.down(35);return;}
  } else { // no up-down movement of the joystick
    isGreen = false; // update isGreen:  we want the green LEDs to be off.
  }
}


////////////////////////////////////////////////////////////////////////////////

// function handles the left and right control of the arm via joystick. 
// additionally, it determines whether the respective (blue) LEDs should be on.
// turnLR is short for turn Left-Right

void turnLR(void){
  if ((yL<500) || (yL>513)) { // is there left-right movement of the joystick?
    
    isBlue = true; // update isBlue: we want the blue LEDs to be on.
 
    if(0<=yL && yL<=100){arm.right(0);return;}
    if(900<yL && yL<=1024){arm.left(0);return;}  
    if(100<yL && yL<=200){arm.right(5);return;}
    if(800<yL && yL<=900){arm.left(5);return;}
    if(200<yL && yL<=300){arm.right(10);return;}      // pushing harder on the joystick increases speed of the turn table (left and right)
    if(700<yL && yL<=800){arm.left(10);return;}
    if(300<yL && yL<=400){arm.right(15);return;}
    if(600<yL && yL<=700){arm.left(15);return;}
    if(400<yL && yL<=480){arm.right(20);return;}
    if(540<yL && yL<=600){arm.left(20);return;}
  } else { // no left-right movement of the joystick
    isBlue = false; // update isBlue: we want the blue LEDs to be off.
  }
}

////////////////////////////////////////////////////////////////////////////////

// function handles the open and close control of the arm via joystick. 
// additionally, it determines whether the respective (red) LEDs should be on.
// turnCO is short for turn Close-Open

void turnCO(void){

  if((xR<510) || (xR>518)){

    isRed = true; // update isRed: we want the red LEDs to be on.

    if(0<=xR && xR<=100){arm.close(0);return;}
    if(900<xR && xR<=1024){arm.open(0);return;}
    if(100<xR && xR<=200){arm.close(5);return;}
    if(800<xR && xR<=900){arm.open(5);return;}
    if(200<xR && xR<=300){arm.close(10);return;}      // pushing harder on the joystick increases speed of the claw open and close
    if(700<xR && xR<=800){arm.open(10);return;}
    if(300<xR && xR<=400){arm.close(15);return;}
    if(600<xR && xR<=700){arm.open(15);return;}
    if(400<xR && xR<=480){arm.close(20);return;}
    if(540<xR && xR<=600){arm.open(20);return;}
  } else {
    isRed = false; // update isRed: we want the red LEDs to be off.
  }
}

////////////////////////////////////////////////////////////////////////////////

// function ensures only one arm axis is being controlled at a time.
// Whichever axis is being moved the most is given priority, and the other axis is reset to default pos.

void date_processing(int *x, int *y, int x_avg, int y_avg){
  if(abs(x_avg-*x)>abs(y_avg-*y)) 
  {*y = y_avg;}
  else 
  {*x = x_avg;}
}

```
```c++
// I2C Slave


// include the required Wire library for I2C
#include <Wire.h>`

// define booleans, which are received via I2C.
// these booleans will determine whether to turn on the respective color of LEDs
bool openRed; 
bool openGreen;
bool openBlue;

const int LED_PIN = 13;


void setup () {
  // define the LED pin as Output
  pinMode (LED_PIN, OUTPUT);
  // start the I2C Bus as Slave on address 9
  Wire.begin(9);
  Serial.begin(9600); 
  // attach a function to trigger when something is received.
  Wire.onReceive(receiveEvent);

  // deifne pins
  pinMode(11, OUTPUT); // green
  pinMode(8, OUTPUT); // blue
  pinMode(2, OUTPUT);  // green
  pinMode(7, OUTPUT);  // red
  pinMode(10, OUTPUT); // green
  pinMode(12, OUTPUT); // blue
  pinMode(3, OUTPUT); // red
}

// updates the RGB variables based on the received data.
// assumes the triplet is sent in the same RGB format.
void receiveEvent(int bytes) {
  if (bytes >= 3) { // ensures we recieved 3 or more data bytes so there is enough to assign to the bools.
    openRed = Wire.read();
    openGreen = Wire.read();
    openBlue = Wire.read();
  }
}

void loop() {
  // openRed is a bool, so it is already either true or false.
  if (openRed) { // does the red LEDs need to be on?
    digitalWrite(3, HIGH);
    digitalWrite(7, HIGH);
  } else { // otherwise, turn them off.
    digitalWrite(3, LOW);
    digitalWrite(7, LOW);
  }

  if (openGreen) { // does the green LEDs need to be on?
    digitalWrite(11, HIGH);
    digitalWrite(10, HIGH);
    digitalWrite(2, HIGH);
  } else { // otherwise, turn them off.
    digitalWrite(11, LOW);
    digitalWrite(10, LOW);
    digitalWrite(2, LOW);
  }

  if (openBlue) { // do the blue LEDs need to be on?
    digitalWrite(8, HIGH);
    digitalWrite(12, HIGH);
  } else { // otherwise, turn them off.
    digitalWrite(8, LOW);
    digitalWrite(12, LOW);
  }

 
}



```


# Starter Project 

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ep7Yl2C_bmo?si=GeC7OTY-ftHB_Cp9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Description + Challenges + Next step  

My starter project was a retro arcade console. I mainly developed my soldering skills, which I did by carefully soldering the pins and wires. This device runs the game on an 8 X 16 LED pixel grid, while the score is revealed on a grid beside it. This console contains 5 games, including Space Invaders, which I show in my video. After soldering all the components, I screwed in the acrylic case, which provides protection to the board and allows the user to hold the console comfortably. Soldering was new to me, and I struggled at first. Before starting my project, I practiced and learned how to solder LEDs and resistors. When soldering, my main struggle was making sure the solder went in the exact place I needed. This was partially due to the thickness of the iron I used. I learned how to remove solder too, which was very helpful. While soldering the wires for the battery, I encountered an issue where the mini USB was extremely close to where I was supposed to solder. While soldering this part, I had to make sure the hot iron didn't accidentally damage the mini USB. Overall, I found this experience interesting, and I really enjoyed it. My next step is to start my intensive project. My intensive project is a joystick-controlled robotic arm. I chose this project because it has a good mix of hardware and software components, and it also allows me to learn more about servo dynamics and motion kinematics.  

# Starter Project Bill of Materials

| Item | Amount | Use |
| --- | ------- |-----
| Circut Board | 1 | contains code for games |
| Buttons | 6 | allows user to control console|
| 8x8 LED pixel grid  | 2 | game display |
| 3 digit display | 1 | score display |
| Passive buzzer | 1 | used for sound |
| Capacitor | 1 | stores electric energy |
| Power swtich + its button cap | 1 | controls when power is turned on or off |
| AAA battery | 3 | power source |
| AAA battery case | 1 | directs power to board and contains batteries |
| Screws | 10 | helps attach acrylic case to board |
| Isolation pillars (copper) | 4 | spaces out acrylic plate from board |
| Isolation pillars (isolation) | 4 | spaces out acrylic plate from board |
| Acrylic main panels | 2 | protects components |
| Acrylic side panels | 4 | protects components + joins main panels |
