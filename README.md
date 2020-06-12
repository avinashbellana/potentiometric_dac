# POTENTIOMETRIC DIGITAL TO ANALOG CONVERTER
The project aims at designig a potentiometric digital-to-analog converter. The key idea is to realize a potentiometric dac with required specifications to be able to get installed in a home automation microcontroller.

# Why digital-to-analog converter?
A computer is designed to work in a digital domain.In today's world, the existence of digital electronics is boundless.Despite such advancement,the world is yet analogous and this seems to be inevitable.Hence,there is a need for a bridge between the digital and analog domains.On that account,there is a need for digital-to-analog and analog-to-digital converters. 

# Quick glance of the IP
With the advent of high performance digital circuits,the need for data converters with high speed and accuracy for a wide range of applications has drawn the attention of scientists and researchers worldwide.In this project we try to design a potentiometric digital-to-analog converter.This repository consists of all the files required to design a potentiometric dac.

To develop an insight into the project, download the 'understanding_pac' word document uploaded in this repository.Go through the document carefully and navigate to the references provided in the same whenever there is a need. The document also provides you with some applications of dac which helps in understanding their practical implications. 

Let us begin with the design of a 2-bit potentiometric dac. All the steps required are mentioned below. Lets start!

# Installing the simulator: NI Multisim
Ni Multisim(student version) software is selected for design and simulation of the software.NI Multisim is one of the best tools available for electronics and circuit design students, teachers and professional workers.Follow the steps given below to install NI Multisim.

## Installation steps for windows 10
Follow the steps given below to install the NI Multisim software.
1) Click on [NI Multisim](https://www.malavida.com/en/soft/ni-multisim/#gref) to download the software.
2) Click on the download button available towards the right.
![show how to download ]()
3) The software gets downloaded in 'downloads'.Now open 'downloads' and then find and open the .exe file.
4) Click 'ok' on the dialogue box opened and extract the file to a preferred destination on your pc. 
5) After the files are extrated, click on install 'NI circuit design suite 14.0' and go ahead with the installation process.This           completes the installation and your are ready to design and simulate.

# Getting started with the design
Now that you are done with the installation, lets get on with the design. Follow the steps given below:

1) Download the 'pdac_schematic.ms14' file uploaded in this repository.This contains the schematic of the 2-bit potentiometric              digital-to-analog converter.
2) Now, open NI Multisim.This can be done by clicking the NI Mlutisim shortcut present on the desktop.
3) Now follow this to open the schematic downloaded earlier '''File -> open -> pdac_schematic'''
4) You can see a schematic of 2-bit dac being displayed on the screen. All the components are annotated. Probes are placed at nodes which we want to be displayed in the output waveforms.The potentiometric dac is desiged using osu180 node.The length and width of each mosfet is clearly displayed on the schematic.You can develop a basic insight into the circuit by going through the 'CMOS design and simulation of 2-bit potentiometric dac' section in the 'undertanding_pdac' document uploaded in this repository.

# Running the simulation
Now that you have developed a basic understanding of the circuit, lets start with the simulation. Follow the below given steps carefully:

1) Click on simulate present at the top in the tool bar. 
2) Now navigate to 'Analysis and simulation' in the drop down box.
3) Now select 'transient' which is displayed to the left of the window popped. 
4) In the 'analysis parameters' tab, enter the start and stop time(for example, 0sec and 8sec).
5) In the 'output' tab, there is a list of variables. Select the variables V(PR3), D(PR1) and D(PR2) and click on add button present at the center after each selection. You can see that the selected variables are added to the analog graph box. Now select D(PR) and D(PR2) from the nalog graph box and move the to the digital graph box using the up and down buttons shown below the analog graph box. You will see that both these variables have moved to the digital graph box. We are doing this beacuse we need a digital graph of 0s and 1s for digital variables(D(PR1) and D(PR2)) and an analog graph for analog variables(V(PR)).
6) In 'Analysis options' tab, set the digital high threshold to 5 an digital low threshld to 0.
7) Now we are ready to simulate. Click on the run button to get the output. The output thus obtained is similar to the one shown below.
![output waveform ]()

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
