
[![MCHP](https://cldup.com/U0qhLwBijF.png)](https://www.microchip.com) 
# PIC18F47Q10 Hello World

## Objective
-----

>In this project, an LED (Light Emitting Diode) is turned on by the PIC18F47Q10 microcontroller >using the Curiosity nano (Q10) development board platform. This is a great starting point for getting your Curiosity nano board running.

## Procedure
-----

>The PIC18F47Q10 GPIO pin RE0, connected to LED0 on the Curiosity nano - Q10 board, is setup as an output to control the LED.

>The project uses: [PIC18F47Q10 Microcontoller](https://www.microchip.com/wwwproducts/en/PIC18F47Q10)

>To follow along with these steps, MPLAB� Xpress cloud based IDE should be open. The setup is described in the steps of this training module. You should see a screen similar to the one shown here to start.

![](https://static.transim.com/img/102019/ef2a7b0347504c6ca53b69872bf32b1c-n2mdq.png){width=auto height=auto align=center}

## Task 1
-----

>The Curiosity nano - Q10 board should be connected to an available USB port on the host computer through a USB cable to the micro B connector on the board. Drivers should install successfully the first time the board is connected and may take a minute or so. The connection is shown in the picture. No other components are required.

![](https://static.transim.com/img/102019/058be09e8ba94f45a8051c73a1a4b8d2-vjjys.png){width=auto height=auto align=center}

## Task 2
-----

>Create a new project in MPLAB� Xpress for PIC18F47Q10 using the Curiosity nano - Q10 Board. Instructions are below if this is your first project. Here is a video showing how to Create a Project in MPLAB� Xpress.

>[https://youtu.be/xOrGLKIl8Rs](https://youtu.be/xOrGLKIl8Rs)

### 1. Launch the new project wizard
Launch the New Project Wizard using one of the following methods: From the Toolbar: Click on the New Project icon, or From the Menu: Select File ? New Project
The project wizard will walk you through the process and prompt you for all the required information. Your selections may be changed after the project has been created by modifying the project's properties.

### 2. Choose Project
>* Choose Microchip Embedded from the Categories column (center).
>* Choose Standalone Project from the Projects column (right).
>* Click the Next > button.

>![](https://static.transim.com/img/102019/e2fdb33b4e7f4dc99b790d966000f561-3qvg5.png) {width=auto height=auto align=center}

### 3. Select Device

>* Choose the device family from the Family drop-down box.
>* Choose your device's part number from the Device drop down box. You may also type in the part number directly, and the list will adjust to the characters you enter.
       Or, start typing the part number in the device box using keypad and it will begin search for the matching part number; select the right one from the list
			
>![](https://static.transim.com/img/102019/9db667e25b1f4acc86429d6c282e8154-d4cc6.png){width=auto height=auto align=center}

### 4. Select Project Name and Folder
>Choose a Project Name. This will be your project's name that the IDE will create.

![](https://static.transim.com/img/102019/63f3a33d128c4b06b6f1eb86ef9c9d87-kx459.png){width=auto height=auto align=center}

>>###***Note: The name cannot have any empty spaces!***

## Task 3 
-----

>Open the MPLAB� Code Configurator (MCC) using the MCC icon or under the Tools>Embedded>MPLAB Xpress Code Configurator menu of MPLAB Xpress.

>![](https://static.transim.com/img/102019/e586ea81e16f4b8a89a80717969fd0c9-ysbb8.png){width=auto height=auto align=center}

>A window will appear showing three steps. If you need the latest version of Java you can click on step one, otherwise click on the step two button to open the MPLAB� Xpress Code Configurator.

>![](https://static.transim.com/img/102019/15d63e8d19d245d2b0257816a1e6db31-1wj73.png){width=auto height=auto align=center}

>A file will automatically download in your browser similar to the picture shown. Click on that file to open it. This is a java application that will launch the MCC.

>![](https://static.transim.com/img/102019/903f58c0fe8b4754a22a64cd37b4dc1e-t30s3.png){width=auto height=auto align=center}

>The process can take several seconds depending on your internet connection speed. Several windows may appear asking if you want to run the program. Also for if you are running the MCC tool for the first time it will ask you for a token which you will find in the pop up box in the Xpress IDE, you can copy and paste it to the token box. When the process is complete you will see a new screen appear, separate from the MPLAB Xpress IDE, that is the MCC control screen. In this screen you can select peripherals for your project, system setup for oscillator and other configuration settings, input and output selections for your device. When all of these are completed you can generate project code including a main.c file by clicking on the Generate button near the center top of the screen. All these generated files will be included in your MPLAB Xpress project.

>![](https://static.transim.com/img/102019/fb87e6a45ece469c8da3b231364810f7-66ftp.png){width=auto height=auto align=center}

## Task 4
-----

>There are three default Project Resources associated with any MPLAB� Xpress project as shown here. For this project we only need to setup the System Module and the Pin Manager. The Interrupt Manager will not be used so they can be left in their default state.
Let's start with the System Module settings. When the System Module selection is highlighted in the Project Resources area the System Module settings will appear in the center of the MCC screen.

>![](https://static.transim.com/img/102019/955dc082ead840688aa3af41f0e759fd-nskdk.png){width=auto height=auto align=center}

>For this project select the following:

>>**Internal Oscillator**
>>* Oscillator Select: HFINTOSC (1MHz)
>>* HF Internal Clock: 4MHz
>>* Clock Divider: 4

>###**WWDT**
>>* WDT Disabled
			 
## Task 5
-----

>In the Pin Manager section select the pin RE0 Output by clicking on the blue unlock button, turning it to a green locked symbol.

>![](https://static.transim.com/img/102019/e8c21a0333964b04ba846f24a12c19af-11tcn.png){width=auto height=auto align=center}

>The Curiosity nano - Q10 Board has RE0 connected to the LED0. By making RE0 an output, the pin will control the LED.
Under the Easy Setup tab of the Pin Module section, you will see the output box already properly checked for the RE0 pin. It also allows you to change the name of the pin from RE0 to a custom name such as "led".

>Since LED0 on Curiosity nano - Q10 is active low,  "Start High" box should be kept unchecked. This configuration will drive the RE0 output pin high and light the LED.

>![](https://static.transim.com/img/102019/4546f5ddbcd34825a13979e5d0837aa8-th2r1.png){width=auto height=auto align=center}

## Task 6
-----

>Click the Generate button in MCC to create the appropriate header and source files for this configuration.

>![](https://static.transim.com/img/102019/37e13528f5824e2089cc849e1985b626-qqs32.png){width=auto height=auto align=center}

>Upon successful code generation the �Generation Completed� notification should appear. Select �OK� to close the window.
New MCC Generated header and source files should now be present in the Project window of the MPLAB Xpress IDE including a new main.c source file.

>![](https://static.transim.com/img/102019/97f4333447e94a458ba80f52f31d685e-w1prn.png){width=auto height=auto align=center}

## Task 7
-----

>Click on the main.c source file in the Project pane to open the file and scroll through the code to locate the //Add your application code comment inside of the while(1) loop.

>This is highlighted to show you can modify the code to create a custom application. Here, the MCC already set the pin low in the Pin Manager setup of Step 5. This will keep it LOW to light the LED. The initialization code generated by the MCC is in the pin_manager.c file.

>Alternatively, values can be manually assigned to an LED inside while loop. RE0 is assigned as 0 by default. Assigning RE0 to 1 will turn off an LED since LED on Curiosity nano - Q10 is active low.

>![](https://static.transim.com/img/102019/3c6a0ab7d6f04e028ff39e63c509703b-tnqk7.png){width=auto height=auto align=center}

## Task 8
-----

>Compile and download the project .hex file by clicking on the Make and Program Device button at the top of the MPLAB Xpress IDE.

>![](https://static.transim.com/img/102019/615e490672854d42873ed713fb43c952-xq01p.png){width=auto height=auto align=center}

## Task 9
-----

>The Curiosity Nano board should appear as a Mass Storage Device after enumeration and to program you simply drag the .hex from the downloads section and dropping the file on to the Curiosity drive.

>![](https://static.transim.com/img/102019/85abf885d33c483081c1427baeb2b1db-bq3x3.png){width=auto height=auto align=center}

>The Programmer LED on the Curiosity nano - Q10 board should quickly flash from green to red and then back to green indicating that the .hex file was successfully programmed to the PIC18F47Q10.

## Results
-----

>The LED0 will now be lit on the Curiosity nano - Q10 board.

>![](https://static.transim.com/img/102019/ddaf1c881b2045cc96baa3e4a8232dad-5mz9d.png){width=auto height=auto align=center}

## Analysis
-----

>The example shows how to control an I/O pin as an output to drive an LED on. The code shows how the MCC can generate initialization code so no additional code was required within the main.c file. Additional control of the LED can be performed by adding code to main.c under the while(1) loop. There are many I/O control macros established in the pin_manager.h file to make it easier to create that code.

## Conclusions
-----

>This project can be the basis for building any project that requires an I/O pin to control a digital output signal. This can include various circuits such as transistor controlled relay or LED displays. This will form the basis of just about any microcontroller based project


