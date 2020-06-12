# POTENTIOMETRIC DIGITAL TO ANALOG CONVERTER
The project aims at designig a `potentiometric digital-to-analog converter`. The key idea is to realize a potentiometric dac with required specifications to be able to get installed in a home automation microcontroller.

# Why digital-to-analog converter?
A computer is designed to work in a digital domain.In today's world, the existence of digital electronics is boundless.Despite such advancement,the world is yet analogous and this seems to be inevitable.Hence,there is a need for a bridge between the digital and analog domains.On that account,there comes a need for digital-to-analog and analog-to-digital converters. 

# Quick glance of the IP
With the advent of high performance digital circuits,the need for data converters with high speed and accuracy for a wide range of applications has drawn the attention of scientists and researchers worldwide.In this project we try to design a potentiometric digital-to-analog converter.This repository consists of all the files required to design a potentiometric dac.

To develop an insight into the project, download the `understanding_pac` pdf document uploaded in this repository.Go through the document carefully and navigate to the references provided in the same whenever there is a need. The document also provides you with some `applications` of dac which helps in understanding their practical implications. 

Let us begin with the design of a `2-bit` potentiometric dac. All the steps required are mentioned below. Lets start!

# Installing the simulator: NI Multisim
Ni Multisim(student version) software is selected for design and simulation of the software.NI Multisim is one of the best tools available for electronics and circuit design students, teachers and professional workers.Follow the steps given below to install NI Multisim.

## Installation steps for windows 10
Follow the steps given below to install the NI Multisim software.
1) Click on [NI Multisim](https://www.malavida.com/en/soft/ni-multisim/#gref) to download the software.
2) Click on the `download` button available towards the right.

![download pic](https://user-images.githubusercontent.com/58501983/84499390-21e43380-acd0-11ea-8319-370363cf0a89.JPG)

3) The software gets downloaded in 'downloads'.Now open 'downloads' and then find and open the `.exe` file.
4) Click `'ok'` on the dialogue box opened and `extract` the file to a preferred destination on your pc. 
5) After the files are extrated, click on install `'NI circuit design suite 14.0'` and go ahead with the installation process.
![cricuitsuit](https://user-images.githubusercontent.com/58501983/84499791-e5650780-acd0-11ea-8845-275337e34bf6.png)
6) We are now done with installation and ready to design and simulate.

# Getting started with the design
Now that you are done with the installation, lets get on with the design. Follow the steps given below:

1) Download the `pdac_schematic.ms14` file uploaded in this repository.This contains the schematic of the 2-bit potentiometric              digital-to-analog converter.
2) Now, open NI Multisim.This can be done by clicking the NI Mlutisim shortcut present on the desktop.
3) Now follow this to open the schematic downloaded earlier `File -> open -> pdac_schematic -> open`
The steps are clearly shown in the images below.

   ![file](https://user-images.githubusercontent.com/58501983/84501150-9ec4dc80-acd3-11ea-823a-a25be9967e3c.png)


   ![open](https://user-images.githubusercontent.com/58501983/84500430-2578ba00-acd2-11ea-946d-2fc6f455ecff.png)


   ![scheme](https://user-images.githubusercontent.com/58501983/84500483-450fe280-acd2-11ea-8dc0-33fee8f6e287.png)

4) You can see a schematic of 2-bit dac being displayed on the screen. All the components are annotated. Probes are placed at nodes which we want to be displayed in the output waveforms.The potentiometric dac is desiged using `osu180` node.The length and width of each mosfet is clearly displayed on the schematic.You can develop a basic insight into the circuit by going through the `CMOS design and simulation of 2-bit potentiometric dac` section in the `undertanding_pdac` pdf document uploaded in this repository.

   ![schematicpic](https://user-images.githubusercontent.com/58501983/84500619-8a341480-acd2-11ea-96cc-d94290eaa3dc.png)

# Running the simulation
Now that you have developed a basic understanding of the circuit, lets start with the simulation. Follow the below given steps carefully:

1) Click on `simulate` present at the top in the tool bar. 

   ![simulate](https://user-images.githubusercontent.com/58501983/84515791-8dd39580-acea-11ea-9915-3c352caccc63.png)
   
2) Now navigate to `Analysis and simulation` in the drop down box. 

   ![analysis](https://user-images.githubusercontent.com/58501983/84515822-99bf5780-acea-11ea-8980-8a9ec7d7471f.png)
   
3) Now select `transient` which is displayed to the left of the window popped. 

4) In the `analysis parameters` tab, enter the start and stop time(for example, 0sec and 8sec).

   ![transient](https://user-images.githubusercontent.com/58501983/84515839-9deb7500-acea-11ea-9cc4-46229dc11980.png)
   
5) In the `output` tab, there is a list of variables. Select the variables `V(PR3), D(PR1) and D(PR2)` and click on `add` button present at the center after each selection. You can see that the selected variables are added to the analog graph box. Now select D(PR) and D(PR2) from the analog graph box and move the to the digital graph box using the up and down buttons shown below the analog graph box. You will see that both these variables have moved to the digital graph box. We are doing this beacuse we need a digital graph of 0s and 1s for digital variables(D(PR1) and D(PR2)) and an analog graph for analog variables(V(PR)).

   ![variables](https://user-images.githubusercontent.com/58501983/84515860-a5ab1980-acea-11ea-80a7-5440bbae612d.png)
   
6) In `Analysis options` tab, set the digital high threshold to `5` an digital low threshld to `0`.

   ![threshold](https://user-images.githubusercontent.com/58501983/84515868-a9d73700-acea-11ea-8805-2b7915206d98.png)
   
7) Now we are ready to simulate. Click on the `run` button to get the output. The output thus obtained is similar to the one shown below. A detailed explanation of the output waveform is given in `understanding_pdac` pdf document uploaded in this repository.

   ![output](https://user-images.githubusercontent.com/58501983/84516158-04709300-aceb-11ea-8f3c-3324e8ebffb5.png)

# Export SPICE netlist
Follow the below given steps to export the SPICE netlist.
`Transfer -> export SPICEnetlist -> select destination on your pc -> save`
It is saved as a `.cir` file.All the steps are clearly shown in the images below.

   ![transfer](https://user-images.githubusercontent.com/58501983/84517827-6b8f4700-aced-11ea-9ec0-e07dd0d16b5a.png)
   
   
   ![export](https://user-images.githubusercontent.com/58501983/84517844-721dbe80-aced-11ea-809d-2c5a7cf6d4e1.png)
   
   
   ![cir](https://user-images.githubusercontent.com/58501983/84518113-d771af80-aced-11ea-93c6-f1c69cb22161.png)
   
The `pdac_spicenetlist.cir` file in this repository is the SPICE netlist for the design.

You have finally designed and simulated a 2-bit potentiometric digital-to-aalog converter.

# Contact information
- BELLANA AVINASH NAIDU
 B.tech Electronics and Instrumentation, NIT Rourkela
 avinashbellana@gmail.com
- KUNAL GHOSH 
 Director, VSD Corp. Pvt. Ltd. 
 kunalpghosh@gmail.com
- PHILIPP GÜHRING 
 Software Architect at LibreSilicon Association
 pg@futureware.at
- Dr. GAURAV TRIVEDI 
 Co-Principal Investigator, EICT Academy,   
 and Associative Professor, EEE Department, IIT Guwahati
 trivedi@iitg.ac.in
