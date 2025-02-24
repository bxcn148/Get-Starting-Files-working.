Download link :https://programming.engineering/product/get-starting-files-working/


# Get-Starting-Files-working.
Get Starting Files working.
Overview

As a starting point for this lab a Vivado project file that includes a MicroBlaze soft processor is provided. In addition, a C-code application is provided as a starting point. Using the Vitis IDE an application is developed that outputs a frequency control digital signal to the AMP2 PMOD to create different musical notes. The application code performs the following functions.

Read the push buttons and dip switches on the Basys3 board.

Set the LED outputs and 7 segment display value.

Create a frequency controlled square wave output to the AMP2 Audio Amplifier to generated different musical notes.

Generate a short tune on start up.

Part 1: Get Starting Files working.

Two files have been provided that should be used as a starting point for your own work.

lab4_start.c : Starting point for the C application code. Feel free to modify any of the existing functions and code as you see fit.

lab4_start.zip : Starting point for the Vivado project files.

Lab4_SettingUpVitis.pdf gives instructions on how to use these files.

To use these starter files, you must have Vitis and Vivado 2021.1 Installed on your computer. Refer to the Lab_GettingStarted.pdf file posted in Lab 1 if you need instructions on how to add Vitis or install Vitis and Vivado.

The starting files provide the below functionality

Light the LED corresponding to its switch input.

Output a continual tone at Middle C.

If these functions do not just work, seek assistance before going further.

As part of the sign-off the LED functionality must be demonstrated. So, leave the LED functionality in place.

Part 2: Create 16 different musical notes

For this part of the lab, read the value of the buttons and slider switches and change the toggle rate of the AMP2’s Analog Input to create a musical note corresponding to the settings defined in the table below. The lab4_start.c shows how to use the Hardware Timer to generate a single middle C note. The target_count value needs to be calculated for each of the 16 notes.

ECE3829-A22 Lab 4

Part 3: Show the note information on the 7-segment display

The 7-segment display is used to show the musical note information. On display D (right most display) show the letter of the corresponding musical note. For example, for btn = 3’111, the display would read b.

Part 4: Power-up play a little tune

When the Basys3 board first powers up or after a reset, it should play a little wake up tune with at least 4 notes and long enough for each note to be heard.

Extra Credit

Up to 5 points lab bonus points for any good improvements, enhancements to your design. You must demo on board and describe the additional functionality well in your report. For you could use buttons to cause distortion affects or play additional tunes. You could expand the usage of the unused 7-segment displays (taking care not to interfere with the audio quality).

Sign-Off Procedure

Signoff can be done remotely via zoom or in-person during lab hours. If via zoom, you will need to have the ability to share your screen with the TA and also have video and audio capability to display and hear the Basys-3 board functions clearly.

You may repeat steps 1-4 as many times as needed. But you may only submit your exported Vitis project and pdf of your C code once during your final demonstration. No changes to these submissions are allowed after your final demonstration.

Have project fully compiled and be ready to show to the TA.

Using File->Export select System Projects to generate an archive of your C project and have it ready to submit.

Have all your C code in a single pdf file ready to submit.

Demonstrate the functionality in the Functionality Check List. TA will record results and assign points for all functionality that is correct.

You can demo as many times as needed.

You will always be rewarded points for the functions that are working.

Once you are happy with your demonstration results.

You will submit the single pdf version in canvas immediately.

You will submit the exported zip in canvas immediately.

TA will verify they are submitted and complete the sign-off process.

4

ECE3829-A22 Lab 4

Sign-Off Check List ( 60 points)

Project Status ( 6 points)

Expected files are in place in the Vitis software project. (2 points)

FPGA Hardware Programs successfully (2 points)

Elf file compiles and runs. (2 points)

Functionality Check List (50 points)

LED Operation (10 points)

When a switch is pushed up, the corresponding LED turns on. When switch is pushed down LED turns off.

If no buttons are pushed, no sound come out and displays are off. (5 points)

When no buttons are pushed, no sound comes out and not lights are on.

Creates 7 musical notes corresponding to button values in table. (10 points)

Test each of the 7 notes that correspond to button values 1 through 7.

Show the letter of the note on display D (right most display). (10 points)

Test each of the 7 notes that correspond to button values 1 through 7.

Switches[1:0] changes the note octave. 0 = octave 3, 1 = octave 4, 2 = octave 5. (5 points)

Test sw[1:0] values 0 through 2. Verify notes increase in octave. 0 = octave 3, 1 = octave 4, 2 = octave 5.

Play a startup tune. (10 points)

When first powered on, play a tune with at least 4 notes.

Extra Credit Demonstrated (up to 5 points)

Extra credit must be demonstrated at time of sign-off and documented in report to receive credit.

Canvas Submissions Completed (4 points)

Exported System Project zip file submitted in canvas at time of sign-off

PDF of C code files submitted in canvas at time of sign-off

5

ECE3829-A22 Lab 4

Rubric for C Code in PDF (20 points)

Code implements the requested functions. (10 points)

Code is composed of initialization functions executed once at the beginning of the programmed followed by an infinite polling loop.

The code in the polling loop is non-blocking and the polling loop delay is minimized.

The count value of the timer module is used to determine the toggle rate of the AMP2 Audio input as well as the refresh rates of the 7-segment display.

Code is well commented ( 5 points)

Code is well formatted, organized and written. (5 points)

The code should be well formatted with proper indentations and reasonable line lengths.

Code is readable and organized so it is clear what functionality is being implemented.

Functions are used when appropriate.

Variable names are short but descriptive.

Define statements are used to define constants.

6

ECE3829-A22 Lab 4

Rubric for Report

Brief Introduction / Problem Statement (5 points)

General Overview of solution (5 points)

Write a brief description of your C code including a flow diagram.

If you implemented extra credit, include a description of the extra features.

Detailed Implementation Description (5 points)

Write a detailed description of how each piece of required functionality is implemented and which hardware blocks were used.

Detail any efforts taken to minimize the loop delay of the infinite polling loop.

Conclusion (5 points)

For functions like the 7-segment display, reading switches, writing LED values, compare your designer experience.

o Was implementation in C or Verilog easier?

o Where there advantages or disadvantages to the different approaches?

What problems or challenges were faced in implementation?

What solutions were used to solve them?

What lessons were learned from the project?

Suggestions for further improvements and extensions?

Where there particular things you liked about the lab?

