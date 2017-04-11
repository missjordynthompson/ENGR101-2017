#include <stdio.h> 
#include <time.h> 
#include "E101.h"
					
int main (){          //This sets up the RPi hardware and ensures everything is working correctly
          init ();   
          
          //We declare an integer variable to store the ADC data int adc_reading;
          int adc_reading;
          int mean;

          for (int count = 0; count < 5; count = count + 1) {				
                  adc_reading = read_analog (0);      //Reads from Analog Pin 0 (A0) through A7
                  mean = mean + adc_reading;
                  printf("%d\n",adc_reading);     // Prints read analog value
          }
	        printf(“Mean reading is %d\n”, mean/5);
          //Waits for 1 seconds (1000000 microseconds)
          sleep1 (1,0); 
          
          //Sets the motor connected to pin 1 & pin 2 to go in one direction at MAX speed.
          set_motor(1, 255);          //Sets the motor connected to pin 1 to 100 % speed straight ahead. 
          set_motor(2, 255);          //Sets the motor connected to pin 2 to 100% speed straight ahead.
          sleep1 (5,0);         // stops motors
          
          //Makes robot turn left
          set_motor(1, 0);      //Sets the motor connected to pin 1 to 0% speed
          set_motor(2, 255);      //Sets the motor connected to pin 2 to 100% speed. 
          sleep1 (2,0);         //stops motors
          
          //Makes robot turn right
          set_motor(1, 255);      //Sets the motor connected to pin 1 to 100% speed
          set_motor(2, 0);      //Sets the motor connected to pin 2 to 0% speed. 
          sleep1 (2,0);         //stops motors
          
          //Sets the motor connected to pin 1 & pin 2 to reverse in one direction at MAX speed.
          set_motor(1, -255);          //Sets the motor connected to pin 1 to 100 % speed reverse. 
          set_motor(2, -255);          //Sets the motor connected to pin 2 to 100% speed reverse.
          sleep1 (5,0);         // stops motors
          
          int adc_reading;
          for (adc_reading > 0) {
                  //Sets the motor connected to pin 1 & pin 2 to reverse in one direction slowly.
                  set_motor(1, -100);          //Sets the motor connected to pin 1 to reverse slowly. 
                  set_motor(2, -100);          //Sets the motor connected to pin 2 to reverse slowly.
                  sleep1 (5,0);         // stops motors
          }
          
          stop (0);
return 0;} 
