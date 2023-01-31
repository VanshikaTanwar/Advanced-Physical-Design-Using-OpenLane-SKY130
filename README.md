# Advanced-Physical-Design-Using-OpenLane-SKY130


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215343706-7823e1b9-93a4-4fd6-a22e-8f2cf3197330.jpg"></br>
   fig.1: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215343958-2c3ea6f8-b47e-4894-928b-5dc268a1f573.png"></br>
   fig.2: 
</p>

We usually in our daily life calling this thing as a chip but in industrial terms it is known as package.

And package are named as a QFN-48 or QUAD Flat No leads.

The size of this package is 7mm and 7mm.


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344029-f7e05b67-2bb1-456c-810d-da644b70e0c5.png"></br>
   fig.3: 
</p>

There is a chip which is assembled at the centre of the package and the chip is connected in this way as shown below.

And these connectrions are used to send the outside world signals or external signals to the chip

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344053-2ce6bab5-c95c-4627-baec-e7e7957f28f8.png"></br>
   fig.4: 
</p>

Inside this chip there are various components Die,pads,core,etc.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344362-2b689123-76e6-4dd2-9769-8514387247c3.png"></br>
   fig.5: 
</p>

A typical Chip or an idea chip consist of SOC,SRAm,ADC,DAC,PLL,SPI and a couple of components.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344396-dbd9b676-807c-4863-b43a-93cd1fc6bd7b.png"></br>
   fig.6: 
</p>

Foundry IP’s

# Open Source Digital ASIC Design

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344432-6bbbddcb-1bcb-4587-babd-9d3cccd248df.png"></br>
   fig.7: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344481-18fb4d53-2f78-479c-9996-ca91585c71b1.png"></br>
   fig.8: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344507-1f98e2a6-71ac-42ca-ac52-3c482bb5b090.png"></br>
   fig.9: 
</p>

# Openlane

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344549-8040b71c-7584-4bf2-af4a-00145baef992.png"></br>
   fig.10: 
</p>

The main goal of using openlane is “To produce a clean GDSII with no human intervention (no-human-in-the-loop)

Here, clean means:-

    • No LVS Violations

    • No DRC Violations
    
    • No Timing Violations 

    
    • Openlane can also be used for harden macros and chips harden means to generate the GDSII Flow or Final Layout. 
   
    • Openlane has 2 modes of operation :-

    #Autonomous or interactive


# OpenLANE ASIC Flow

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215343706-7823e1b9-93a4-4fd6-a22e-8f2cf3197330.jpg"></br>
   fig.1: 
</p>

OpenLane are based on several OpenSource Projects:-

OpenROAD, Magic VLSI Layout Tool, Fault,Yosys,Qflow, KLayout,etc.

# Day 1:

 •  In day 1 we explore how OpenLane works with Sky130 PDK, its working directory, its initial configurations, how to invoke commands and where to find the generated results.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344659-616fc20c-1912-4598-b76c-a0896d466f40.png"></br>
   fig.12: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344733-3dc65e80-5dff-4846-b080-1b3795151219.png"></br>
   fig.13: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344806-4630d8bb-9d24-4794-af1e-41feec8943b3.png"></br>
   fig.14: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344844-9fc4ce97-06fa-412d-a28d-2a70f742cec9.png"></br>
   fig.15: 
</p>


    • As shown sky130a.tech is the Skywater PDK we are using. It composes of libs.tech and libs.ref.

    • libs.tech  are those files which are specific to the tool.
    
    • libs.refs contains all the technology specific process, specific files which are respective to the timings, length,etc. 

    • These file is dependent on the process technology we are using. In this case, the parameters, tools and technology use in skywater foundry.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344949-1fc4addb-420b-4dbb-932a-1477bab6a444.png"></br>
   fig.16: 
</p>

As, it is seems that all the files which are inside libs.ref are specific to the technology.

Here, as seen below “sky130_fd_sc_hd” so, this nomenclature means :-

Sky130 is the process name , as sky130nm.

fd is the abbreviated foundry name as skywater foundry.

Sc is standard cells which stands for library file.

Hd is stands for high density.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344973-4afcc828-eed7-47f0-97f8-f7d3fb9fc0b8.png"></br>
   fig.17: 
</p>

The files inside sky130_fd_sc_hd are shown in below image:-

These files are used by the EDA tools in the design process.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215345002-e4b24906-17d5-4436-9bb3-25ec4b8f1ec1.png"></br>
   fig.18: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215345031-e2c0434b-9fb8-4fca-b092-77f1a2660c9a.png"></br>
   fig.19: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215345077-12926afe-f82c-49e7-bb9b-3e7d68af1837.png"></br>
   fig.20: 
</p>

As, it is seems that all the files which are inside libs.tech are specific to the tools.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215345106-222e1bf6-19af-4314-a886-8aa1140af255.png"></br>
   fig.21: 
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215447178-125dfdb6-6e55-4131-970c-ec1122d42db1.png"></br>
   fig.22: 
</p>

All the files inside the openlane directory are shown below:-

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215447562-7a4c5a5e-2b6f-4e8e-adc7-a528ee03c3f2.png"></br>
   fig.23: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215447911-d9503024-a61c-47b6-8616-9e58e7090577.png"></br>
   fig.24: 
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215448029-dcfbb6c3-0867-468a-89e3-3a2d00732649.png"></br>
   fig.25: 
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215448135-4460af67-7110-48c5-81b8-0a6d4d198627.png"></br>
   fig.26: 
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215448310-d41ce3d0-e013-4224-a192-dabb512d760e.png"></br>
   fig.27: 
</p>


Many of the switches use default values that’s why we have used the less command in less config.tcl

After executing this command this will come, 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215448722-763edb31-7866-4c0a-8700-e1c9c29eeefe.png"></br>
   fig.28: 
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215448931-46af6dda-a885-4f53-b0bd-3dd97d3ddd27.png"></br>
   fig.29: 
</p>

It shows default values and it set file name.

For example , as in this image the highlighted command means it sets the clock from default value to 24nm. It overwrites the default openlane setup.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215449340-a7e0d9e9-21f7-463d-b960-5bb443f75e74.png"></br>
   fig.30: 
</p>


## Design Preparation Steps

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215494909-bb22573e-7194-437a-8319-b0b885f3e7d2.png"></br>
   fig.31 
</p>

To start openlane we invoke the following commands which are mentioned below:-

    1) Go to the vsdflow/work/tools/openlane_working_dir/OpenLane
    
    2) Execute this command after going into the respective directory of OpenLane 

make mount

    3) Then execute this command 

./flow.tcl -interactive
  
  4) package require openlane 0.9
  
  5) prep -design picorv32a

after the execution of last step this is shown :-

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675370-2a89da6f-7c40-4968-8cdb-26bdda31ad09.png"></br>
   fig.32
</p>

Checking the creation of file ,so a run folder is created within picorv32a 

Since, today’s date is 27th January 2023 so a folder created is titled as “RUN_2023.01.27_19.36.16” within the picorv32a Directory.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675497-3960863e-b642-4a41-8d51-bd5fbbefe7b5.png"></br>
   fig.33
</p>

These are the files after reviewing the run folder 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675597-cda1a361-9c1a-4a37-9e53-18b6b42fb8fe.png"></br>
   fig.34
</p>

After opening the tmp folder and see all the list of files , it shows:-

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675679-bc012d3c-f4c8-4f89-8f43-d79f386408b2.png"></br>
   fig.35
</p>

Some merged files are created under tmp folder inside RUN_2023.01.27_19.36.16

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675756-ee80a69b-1996-487d-93a8-e19402c77105.png"></br>
   fig.36
</p>

merged.max.lef file after opening looks like this as shown in the image below. 

merged.max.lef shows all the layers related information,layer vias, etc.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215675835-7a65e737-cc63-4a70-9412-f680a41f8df8.png"></br>
   fig.37
</p>



</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215676145-5ebdd685-5d55-429c-8df0-e297e91dbc1c.png"></br>
   fig.38
</p>

Next, we will run the synthesis of picorv32a design in the openlane interactive terminal

run_synthesis

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215676451-2bb3f8d3-4140-4506-bc97-dde789acecee.png"></br>
   fig.39
</p>

To calculate the Flop Ratio 

we need to see the printing statistics content in synthesis folder within reports.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215680449-2de7696f-bd3a-4d1a-9e33-b04dec3448b9.png"></br>
   fig.40
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215680533-f1ed0288-988d-4eb7-9b0a-aa7f9b657e36.png"></br>
   fig.41
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215680710-5efbc2e4-3acc-4cc1-868f-25d2ede143c7.png"></br>
   fig.42
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215680792-2760a448-f1a7-41ac-9099-df90c98abe0f.png"></br>
   fig.43
</p>

Now, we need total no. of cells and no. of d flip flop Formula for calculating flop ratio is 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215681005-35986bfb-e86c-4fcf-b734-728345fd7ebe.png"></br>
   fig.44
</p>

dfxtp_2= 1596,

Number of cells = 9727,

Flop ratio = 1596/9727 = 0.1640793 = 16.4%

  • Characterization of synthesis results

To confirm the success of synthesis step we need to check the synthesis folder for synthesized netlist file(.v file).

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215681117-e3152aa8-868c-4ac6-ab27-9a3a41b80f4f.png"></br>
   fig.45
</p>

This file is generated by Yosys

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215681205-287c2a95-505c-4f07-8b93-0b540cd3f350.png"></br>
   fig.46
</p>


# Day 2

The synthesis statistics report can be accessed within the reports directory.

So, to view it we need to open  it


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215685396-ae43d1e9-cec6-4275-ae3f-4a0dc0809b93.png"></br>
   fig.47
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215685483-bd577a83-a445-4aab-9943-c8c11d89e94c.png"></br>
   fig.48
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215685561-e278832a-7561-4d0d-9b71-738660349391.png"></br>
   fig.49
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215685643-ff03f18c-231c-42ec-b758-db320ecba2c6.png"></br>
   fig.50
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215685727-30f88514-d543-4ae9-bac7-3c5a09b2e9b6.png"></br>
   fig.51
</p>

Chip area is 99853.267200.


## FloorPlan and Library Cells

2 parameters are important mainly in floorplanning .These are:-

Utilization Factor and Aspect Ratio.

                Utilisation Factor =  Area occupied by netlist
   
                                      __________________________
                      
                                          Total area of core
