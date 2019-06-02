# CONTROL BLDC MOTOR WITH STM3F746

# AUTHER:
	 JAGADISH JADHAV
# REQUIREMENT :-
	1) STM32 CUBE MX SOFTWARE.
	2) KAIL uVISION 5 IDE.
# Execuation:
	1)  download zip file and extract the file.
	2)  open the MDK-ARM folder. and double click on uvision file it name same as your project name. 
	3)  then your ide is open with project then open application / user folder from project tab.
	4)  open the main.c file and compile it by pressing F7. after compiling succesfully 
	5)  Plug-in STM32f controller via usb to pc.
	6)  pres load tab.
	7)  after load succesfully just reset board once and your board is ready
# explanation and calculation for pwm frequency:
	To run the esc we need to generate the pwm with 50Hz to 250Hz  frequency and ON period of duty cuyle is 5% to 10%
	esc one udersatnd the 1000us to 2000us pwm pulse as input that mean 1000us is zero RPM and 2000us is full RPM
	
	PWM FREWUENCY CALCULTION:
	pwm freq = (main frequency of timer bus / prrescaller) / Total peroid of duty cycle 
	in my case i used timer 2 which is connected to APB bus 2 that if of 72MHz and i set prescaller to 10
	
	pwm freq = (72MHz / 10 )/ 120000 = 60Hz
	
         
	
	
