# Project Name Here
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Mishika D | Cupertino Highschool  | Bio/Biomedical Engineering | Incoming Freshman

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
  # Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZKKGAXcAkhQ?si=GAgxgriwa98hc6Mu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE

 # Description
I completed my modifications for my third milestone. I successfully added LEDs to my robot, which turn on based on the robot's movement. I also designed a case to house my breadboards.

  # Planning my modification 

In the beginning, I simmulated how this modification would go using tinkercad. I initially wanted my LEDs to light up based on servo movement, so to mimic that I added a potentiometer (since there was no joystick) and servos along with the LEDs. I also wrote code based on the movement of the servos. During this process I learned how current flows through breadboards and applied it to my LEDs. Since this was just a simmulation, I was able to test how LEDs would react when I changed their ressistance and location on the breadboard. During this time I learned the difference between wiring circuts in series vs parallel.  

  # Building my modification

When I started the actual build of my modification, I realized it woud be much easier to have my code read the joystick position rather than the servo positon. This is because my original code already reads the position of the joystick, which correlate to movement on my robot. Also, my previous code was written based on the potentiometer, which meant I had to change aspects of my code at some point, which would take time away from my build. Using my original code made debugging and troubleshooting simpler since I knew how it would react alongside my robot. I also changed some of the wiring when attaching my LEDs to my breadboard. For example, due to the ammount of wires, I changed the location of some of the LEDs for convenience. Learning how power flows through bread boards was really important too, especially since the top half of the breadboard does not automatically get power even when the botton half does. 

# Challenges 

This part of my project had many challenges. To start off, my code had a deadzone which said that if the value on the joystick was not 512 (center), then the robot can move. When I added my LEDs, I found that the deadzone value had changed. This caused my LEDs to blink rapidly rather than stay still. I overcame this by writing debug code and adding a range of values rather than a specific number. I also found that wiring in series sometimes would not work. While it worked on my simmulation, sometimes wiring more than 1 LED in series caused too much ressistance and it wouldn't light up. I faced an issue with the wiring too. When wiring the power line from the top and bottom of the breadboard, I accidentally wired power to ground rather than power to power and ground to ground. I realized this when my robot froze when it was supposed to be in motion. Attaching my LEDs to my robot was a challange due to the amount of wires I needed. Each LED needed 2 jumper wires and I had to double the lenghth (the wires has to be long since the LEDs had to reach the robot). In the future I aim to make a case for my robot so the wires are protected. 

# Key topics I Learned 

  # I2C

Using I2C, I got my original nano board to communicate with an additional nano esp 32, which currently drives my LEDs. I2C is a common communication protocol that helps transmit data between different devices. I chose to implement I2C because I can easily add more modifications in the future since this mechanism allows for multiple "master" and "slave" devices. Not to mention, this method of communication does not require many wires which adds to it's usefulness. My "master" board was my nano located on my robot. This microcontroller contained code signaling my robot to move and told the LEDs when to light up. My "slave" board was my nano esp 32, which light-up my LEDs.

# Programming 

Most of the challenges I faced lied in the program of the robot. Like I mentioned before, my LEDs would blink when they were not supposed to. While fixing this issue I learned how to write debug code and use the serial moniter. This was incredibly helpful since most of the issues I faced weren't directly written in the code. By writing debug code, I was able to read outputs from the serial moniter and fix my issues. 


# Future 

  # Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/FrV4J9Y4CQE?si=83UWknsjZBa5xKt_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone

# Description + Challenges 

My second milestone was achieving motion on my robot and completing the wiring. The only wiring required for my robot was for the servos, which I already did to set them to 90 degrees, and the controller. Thus, I finished wiring really fast and decided finish the programming aspect instead of add my modifications. Initially, I decided to have my modifications as the second milestone and have the program as the last. As I worked on the wiring for this milestone, the programming came consecutively which led me to change my plans. I also wanted to apply my modifications by itself as a seperate milestone. The program, which is written in C++, directs the robot to move faster when the joystick moves faster and vice versa. It also goes over the buzzer feature, in which a sound will be made when an action is memorized and when it acts out this recorded action. A problem I faced was that some of the screws holding the servos in place becme loose. This was due to the power of the servos, as the screws given were slightly short. I decided to replace some of these screws with mini zipties since I wouldn't have to worry about any screws coming out. To add on, I found that female-female wires can be used to connect the batteries to the robot. This is a much better idea than soldering since it is not perminent and can easily be removed if necessary.  

# Whats next?

For milestone 3, I want to add my modifications that I thought of when creating my build plan. The modification I want to focus on involves LEDs. Im hoping to add different colors of LEDs around my robot and have certain colors light up when certain actions are preformed. If time permits, I will CAD a case for the controller since it is currently only attached by the wires. 





  # First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/MZYBzXjo5vc?si=ej4jDvrsS-FzDc1A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Description + Challenges  
Completing the build of my robot was my first milestone. Before starting the assembly of the robot, all servos needed to be set to 90 degrees. This is done by uploading code to the robot which states what pins the servos are located on and sets the servos to 90 degrees. Without setting them, the position of your servos is unknown. This means when you assemble the robot, it won't have its full range of motion. This robot utilizes 1 servo beneath the base of the robot to rotate the arm. This servo is located inbetween the turntable, which is used to support the base which the arm stands on. Two servos are located in the middle of the arm, they control how far forward and backwards the arm moves. The last servo is located at the top of the arm and it moves one side of the claw up and down. The gear of this side of the claw is in contact with the other gear of the other claw, thus moving both sides while only utilizing one servo. 
I overcame many challeges during this assembly. For example, while building my robot I didn't set my servos. At this point I had already attached 3 out of the 4 servos and I ended up having to deconstruct a lot of my robotic arm. While this was tedious, it got me familiar with the robot. Keeping track of parts was also important. The screws used for the servos were extremely small, and so I had to make sure to not accidentally loose any. To add on, I didn't have acess to the lithiumn batteries necessary to power to robot. Instead I used a single 9V battery as the power source. Also, some of the screws were located in awkward places, and so it was hard to properly attach some parts. An example of this was one side of the claw (the side not attached to the servo). I had to add 2 bearings, my claw, and three washers through the screw before using a nut at the end to secure it. 

# Whats next?
For my next milestone, I am aiming to complete my modifications. My main modification is to add LEDs which light up based on the movement of the robot. If I have extra time, I will CAD a case for my controller using Onshape. 

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Starter Project 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ep7Yl2C_bmo?si=GeC7OTY-ftHB_Cp9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Description + Challanges + Next step  

My starter project was a retro arcade console. I mainly developed my soldering skills, which I did by carefully soldering the pins an wires. This device runs the game on a 8 X 16 LED pixel grid, while the score is revealed on grid beside it. This console contains 5 games, including space invaders which I show in my video. After soldering all the components, I screwed in the acrylic case, which provides protection to the board and allows the user to hold the console comfortably. Soldering was new to me, therfore I struggled at first. Before staring my project I practiced and learned how to solder LEDs and resistors. When soldering, my main struggle was making sure the solder went in the exact place I needed. This was partially due to the thickness of the iron I used. I learned how to remove solder too, which was very helpful. While soldering the wires for the battery I encountered an issue where the mini USB was extremly close to where I was supposed to solder. While soldering this part, I had to make sure the hot iron didn't accidentally damage the mini USB. Overall, I found this experience interesting and I really enjoyed it. My next step is to start my intensive project. 

# Bill of Materials

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










# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
