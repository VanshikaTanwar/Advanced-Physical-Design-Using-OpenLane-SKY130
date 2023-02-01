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

               • Utilisation Factor =  Area occupied by netlist
   
                                      __________________________
                      
                                          Total area of core

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687478-3fa3bf8c-2905-4d2f-b5f9-efa36007d737.png"></br>
   fig.52
</p>

A utilization Factor of 1 signifies 100% utilization leaving no space for extra cells/logics such as to add buffer. However, practically , we only use utilization factor approximately 50%-60% or 0.5-0.6.

   • Aspect Ratio
   • Aspect ratio = Height/Width

Aspect ratio 1 means that the chip is squared shaped. Any value which is another than 1 means it implies the rectangular shaped. It also means that when anything comes other than  1 then, the core is 50% utilized and the remaining area or extra amount of area is used to place the additional cells.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687571-3995e2cd-4ad3-4ed0-9cd9-3b6cf9a44958.png"></br>
   fig.53
</p>

Core utilization =area of netlist/total area of cell

Here, FP_CORE_UTIL=50 means floorplan core utilization is 50%.

Aspect ratio is 1.


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687667-b56e3d47-187c-438c-8fa1-16a17388f15f.png"></br>
   fig.54
</p>

Steps to run floorplan using OpenLANE

After the synthesis , execute the run_floorplan command

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687770-b2ce4ef6-e8b3-431b-b5f0-4ed869e95f1a.png"></br>
   fig.55
</p>

Now, to review the floorplan files

Post the floorplan , a picorv32a def file is created in the floorplan under results of run within picorv32a folder. Basically, def file describes about the core area.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687844-becf68fe-ad07-4263-8793-db25e4ae6ca9.png"></br>
   fig.56
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215688009-6176d4da-a641-43b8-83f1-41953a9840a1.png"></br>
   fig.57
</p>

After opening Def file it’s showing below:-\

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215688075-ee4f3913-ffd2-48ed-934f-11b3a2006cbc.png"></br>
   fig.58
</p>

To view the floorplan, magic is executed using following command.

 • magic -T /home/vanshikatanwar/desktop/vsdflow/work/tools/openlane_working_dir/OpenLane/pdks/volare/sky130/versions/9f1c2b06d2b5a6708cfe0b55679c7e84d37220cc/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.max.lef lef read ../../tmp/merged.min.lef lef read ../../tmp/merged.nom.lef def read picorv32.def &

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215688164-c135c779-8755-4a65-8f0c-f9fe842ec9d7.png"></br>
   fig.59
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215690921-ba44cce2-2296-47ac-befa-5d44f1b45199.png"></br>
   fig.60
</p>

Press on the keyboard to bring it in the center.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691224-ebb7e512-eabd-41e3-951d-98e6b6f79dac.png"></br>
   fig.61
</p>

Zoom in view

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691379-2a741222-f770-4c6e-8c9b-0cfac9bd207d.png"></br>
   fig.62
</p>

There are decaps which are arranged along the side rows.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691468-a9090933-ae96-49bc-8876-c358fc333d33.png"></br>
   fig.63
</p>

Zoom in provides the view of decaps which are present in picorv32a.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691560-ed498122-27ec-4a9d-8b1e-93cbfca645f2.png"></br>
   fig.64
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691631-0459d6d5-5691-476e-a8d1-d8a6597110cc.png"></br>
   fig.65
</p>

The standard cell is found at the bottom of the left corner. This is buffer basically.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215691711-24c9cc2b-e191-4a66-9a21-a39072e14b5c.png"></br>
   fig.66
</p>

Placement run on openlane and view in magic

In placement we are doing the congestion related placement. We are just ensuring that the transition is left.

Now, for the placement run command in openlane

run_placement

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215694604-bc12c459-dddf-4f54-b0ec-1de8ebd5bdd7.png"></br>
   fig.67
</p>

After the placement is done, a def file of placement is created within the picrv32a folder/run/result/placement  now the placement can be viewed in magic with the following command :-

magic -T /home/vanshikatanwar/desktop/vsdflow/work/tools/openlane_working_dir/OpenLane/pdks/volare/sky130/versions/9f1c2b06d2b5a6708cfe0b55679c7e84d37220cc/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.max.lef lef read ../../tmp/merged.min.lef lef read ../../tmp/merged.nom.lef def read picorv32.def &

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215694702-af2a6185-a8d0-4db0-8591-7112c49528fd.png"></br>
   fig.68
</p>

The view of placement in magic looks like

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215694779-338dd405-4bab-43f2-81bb-4fe9f398fb44.png"></br>
   fig.69
</p>

Press s


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215694850-919da388-3339-4f3c-a85e-02f1a24c2f5a.png"></br>
   fig.70
</p>

zoom in view  of placement is shown below:-

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215694934-1030200b-4929-4d46-a82e-590ecaea1fe0.png"></br>
   fig.71
</p>

After zoom in it is seen that the placement of all the standard cells in the standard cell rows 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215695003-1bd51aab-4ee0-42a6-a162-38b9cad0c716.png"></br>
   fig.72
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215773056-b0c8359a-c907-4cdf-97ac-f70b0bf949e4.png"></br>
   fig.73
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215773859-69f079a1-184b-4456-b000-26106be1a41a.png"></br>
   fig.74
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215773162-906a2855-ebcc-4b82-af8a-8a801db9e6bb.png"></br>
   fig.75
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215774272-5025e9ca-e0e8-48c3-8862-fb59dc6bcbf6.png"></br>
   fig.76
</p>

### Timing characterization

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215775529-19399c30-c678-46b3-af79-ded54bbbe9a8.png"></br>
   fig.77
</p>



</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215774272-5025e9ca-e0e8-48c3-8862-fb59dc6bcbf6.png"></br>
   fig.78 
</p>



</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215782582-5f58cb82-9115-44ed-991e-e7f34f307323.png"></br>
   fig.79
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215782792-bffef679-8602-4620-835b-6578b454d734.png"></br>
   fig.80
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215783257-8a7ffa60-ac2c-4af0-bf2e-e2d05c2f2a9a.png"></br>
   fig.81
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215783520-237aa288-048c-4dfc-9276-b54585990431.png"></br>
   fig.82
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215784192-2067973c-cbe4-423a-92ad-46926cccdfc8.png"></br>
   fig.83
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215784454-22ce08ad-6008-46f3-8381-e2d9ffd6b620.png"></br>
   fig.84
</p>


# Day 3

OpenLANE allows users to make changes to environment variables . If we want to change the pin placement from equidistant to some other style of placement .

For that first we need to check and verify the value which is already set in the floorplan .tcl file.

For checking it , go to this directory and the follows further steps as mentioned below:-

Go to openlane/configurations/

And open “less floorplan.tcl”


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215786452-4bffa95f-4aa3-4238-b88a-49c1d78aa5f5.png"></br>
   fig.85
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215786781-6709f462-ba0e-4dbc-8ade-4ef52f14b16a.png"></br>
   fig.86
</p>

Now, to change the environment variable , write this command in the OpenLANE:

set ::env(FP_IO_MODE) 2

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215787110-7c9e86fe-abda-4299-b44e-89d9b9cac3fb.png"></br>
   fig.87
</p>

Now, run the floorplan again in OpenLANE 

run_floorplan

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215787332-c5915d49-438b-4ee1-baaf-7a9c2ebd39fd.png"></br>
   fig.88
</p>

Now, post the floorplan the, def file has updated. Now use, that magic -T command which is used earlier to see floorplan in Magic tool to see that what has been updated now.

Lab steps to git clone vsdstdcelldesign

=Inverter Standard cell Layout & SPICE extraction
 
    • The magic layout of a CMOS Inverter is used to integrate it with picorv32a design.
    
    • For  that , the inverter magic file is sourced from vsdstdcelldesign by cloning it within 
    openlane directory 

That is(i.e., cd vsdflow/work/tools/openlane_working_dir/OpenLane 

Using this command :-

 git clone https://github.com/nickson-jose/vsdstdcelldesign.git


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215787905-f2489ebe-304c-4c83-ba44-e7c8335328b2.png"></br>
   fig.89
</p>


This creates a folder of name vsdstdcelldesign in the OpenLane directory.

Now, write ls-ltr 

To check the created folder

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215789110-c15569c8-e3b0-4095-8ed7-bbe7a8e316ba.png"></br>
   fig.90
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215789215-10733960-ba9e-48eb-b010-10bc19c4aac7.png"></br>
   fig.91
</p>

All the contents are displayed after cloning in the image given below:

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215789347-91c49c67-04a3-4072-8794-978009537478.png"></br>
   fig.92
</p>

Now, let’s open up the mag file to see all different layers which are used to create the inverter layout  but to open the mag file we need to have tech file first means the magic tech file to open it.It means that we need booth .mag file and .tech file in same folder.

So, first copy the sky130_inv.mag file from vsdstdcelldesign to vsdstdcelldesign/libs using this command:

cp sky130_inv.mag   /Desktop/vsdflow/work/tools/openlane_working_dir/OpenLane/vsdstdcelldesign/libs


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215789661-7bf35ef5-f1e5-4ead-9ca5-617295e4488e.png"></br>
   fig.93
</p>


Now, look sky130_inv.mag file has been copied in vsdstdcelldesign/libs

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215790111-16846e3d-dd26-4571-b5dc-64afe11a9ed7.png"></br>
   fig.94
</p>


Now, this sky130A.tech file is used to open the mag file in Magic.To execute the sky130_inv.mag file use this command:-

magic -T sky130A.tech sky130_inv.mag & 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215790261-c1d8f7eb-e1d5-4473-9947-3e283f92270c.png"></br>
   fig.95
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215952753-a32e8a61-ea96-41c5-aae4-3bbd42e737d4.png"></br>
   fig.96
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215952916-91a80dc3-3245-4397-97f9-312a2cc65578.png"></br>
   fig.97
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215953031-21caa148-034a-46ee-8b89-e9c35483994b.png"></br>
   fig.98
</p>

To see which metal layer is which so, for that write 

“what” command in tkcon window but before that drag and drop this white square on that part which you want to know that which metal layer it is 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215953118-45cb2c9f-473b-435e-8e64-cde969af1406.png"></br>
   fig.99
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215953594-f458b8aa-8e88-4371-b216-195ec61e8394.png"></br>
   fig.100
</p>

In SKY130 the first layer is known as local interconnect layer it’s metal 1 or locali as shown below:

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215953765-5ece648f-5cc3-4eb2-9f81-5db88a3fac36.png"></br>
   fig.101
</p>

The pink layer is metal 2

To verify whether this layout is actually a of CMOS inverter or not, so, for that, we need to verify the p-diffusion,n-diffusion, and polysilicon region. Verification of these regions with polysilicon can be observed:

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954162-0698b6bb-1817-406b-aad7-d342e87bb863.png"></br>
   fig.102
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954455-8cc6db1b-d3df-49e7-b1fe-425fb112e36d.png"></br>
   fig.103
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954766-7ab2e93d-c7a9-4736-88a8-db3c0967fe17.png"></br>
   fig.104
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954808-6d0d0534-9ec4-4eff-887a-f2e4754f3589.png"></br>
   fig.105
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954859-3a4aac9b-8515-4726-8d5a-8d59dcff8dde.png"></br>
   fig.106
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215954938-34def755-1ac0-4ec1-bcfa-f89360b8b7e5.png"></br>
   fig.107
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955040-d02c7176-acc2-4269-b118-f14c44e976e6.png"></br>
   fig.108
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955065-d5768fcb-ed09-411f-8871-544ea765db4c.png"></br>
   fig.109
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955163-a2213c93-3039-41e7-b0b7-fb632ce79ed6.png"></br>
   fig.110
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955198-70fe6c4a-3622-4645-8a24-8b20546196c4.png"></br>
   fig.111
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955269-620aafbe-96cc-4f1b-9eee-fc5c0a8d9488.png"></br>
   fig.112
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955297-cd1d0adb-b00b-455a-b582-c139e1429ae3.png"></br>
   fig.113
</p>

The full form of LEF is Library Exchange Format .LEF has only metal layers it does not contain/have all the information of logic part.Because we don’t need for a PnR placement of any cell/any macros we don’t need information of the logic because we only need to know where are the pnR boundries  , if I need to place a cell , I just need to know where are the pins of the cell and where are the boundries where is VDD and where is Gnd.

LEF is also showing the protecting IP.

In commercial tools, LEF is also called the Frame view it basically shows the physical Layout Of an IP.


SpiceExtraction

Within Magic , the following commands are used in the tkcon window to achieve the .mag to .spice extraction:

pwd

extract all

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955559-31bfea57-f425-4cd2-9f35-875b187233ad.png"></br>
   fig.114
</p>

This extract is extracting our design “sky130_inv” into “sky130_inv.ext”.

Now, let’s check that .ext spice file is created or not in vsdstdcelldesign folder

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955720-1fcb509a-5aa4-4a6c-b0b7-cc98574ed752.png"></br>
   fig.115
</p>

Now we are going to use this .ext file to create the spice file

For that write these commands in tkcon window after the extract all command

ext2spice cthresh 0 rthresh 0

ext2spice 

these above commands means ext2spice- extracting to spice file 

cthresh 0 rthresh 0 means we are extracting all the parasitic capacitances after extracting the above commands the result is look like this :-


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215955904-e0f0045b-35d2-4e4c-8dff-bbfe3a2fd2f7.png"></br>
   fig.116
</p>

Now, let’s check that either the spice file is created or not ?

So, the spice file is created 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215956512-54565acf-45c3-4bf5-8aa3-8528ba35ddb4.png"></br>
   fig.117
</p>

Now, let’s see what is inside this spice file 

To open spice file use this command

vim sky130_inv.spice

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215956623-fa40aed5-442a-432a-8683-061df6898814.png"></br>
   fig.118
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215956683-67dfeed2-6f92-4ceb-ac08-d682ded9b1b8.png"></br>
   fig.119
</p>

Now , we edit this SPICE File

By pressing s

Now you can change the SPICE file in the terminal itself Changed spice file looks like this

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215956890-04091514-0fa6-43f3-9752-cae3ca6fc13a.png"></br>
   fig.120
</p>



```sh
SPICE3 file created from sky130_inv.ext - technology: sky130A

"
  .option scale=0.01u
  .include ./libs/pshort.lib
  .include ./libs/nshort.lib

//.subckt sky130_inv A Y VPWR VGND
M1000 Y A VPWR VPWR pshort_model.0 w=37 l=23
+  ad=1443 pd=152 as=1517 ps=156
M1001 Y A VGND VGND nshort_model.0 w=35 l=23
+  ad=1435 pd=152 as=1365 ps=148
VDD VPWR 0 3.3V
VSS VGND 0 0V
Va A VGND PULSE(0V 3.3V 0.01ns 0.1ns 2ns 4ns)
C0 Y A 0.05fF
C1 A VPWR 0.07fF
C2 Y VPWR 0.11fF
C3 Y 0 0.24fF
C4 VPWR 0 0.59fF
//.ends
.tran 1n 20n

.control
run
.endc
.end




Now, to save this changes 
Press esc
Then write “
:wq
Hit enter


For simulation ,ngspice is invoked in the terminal with following command:
 
ngspice sky130_inv.spice

```

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215957698-a8494a15-7412-4fac-a694-5a31ee25e7b5.png"></br>
   fig.121
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215957765-7d9145be-ade7-4908-bc4e-ea81ca3e5edd.png"></br>
   fig.122
</p>

To plot the waveform between y and time 

So, for that we need to write this command in ngSpice:-

The waveform obtained after executing this command is


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215957930-538882b8-d5a8-4778-a3c0-2887f0208f6d.png"></br>
   fig.123
</p>

NOTE:- The spike which is coming in the output at switching point is due to the low load capacitance. It can be changed by editing the spice to increase the load capacitance value.

#### Inverter standard cell characterization 
 There are total 4 timing parameters that are used to characterize the inverter standard cells. These are:-
  
  1 Rise Transition – It is the time taken for the output to rise from 20% of the maximum value  to 80% of the maximum value.
 
 2 Fall transition - It is the time taken for the output to fall from 80% of the maximum value  to 20% of the maximum value.
 
 3 Cell rise delay = time(50% output rise)- time(50% input fall).
 
 4 Cell fall delay = time(50% output fall)- time(50% input rise).

All these above parameters can be calculated by observing and noting down various values grom the generated ngspice waveform.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958206-ca9ce1df-9f94-4aa7-aaa1-cbf468132539.png"></br>
   fig.124
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958266-f8db1b83-b4b9-43ae-a2b1-01a4c96c95e5.png"></br>
   fig.125
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958335-27d45898-bc72-4ec9-86f1-5e3c2d41c88d.png"></br>
   fig.126
</p>

```sh

Rise transition =( 5.47009 - 5.18462 ) = 0.28547=28.5ps
```
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958522-23ca0e51-913b-4508-91a6-b135d06fc19e.png"></br>
   fig.127
</p>

```sh

Fall Transition = ( 5.7121 – 4.5082 ) = 1.2039= 1.20ps
```

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958663-9e079ea3-7d38-43e4-9940-3aa8739831d2.png"></br>
   fig.128
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958796-89b4fe74-76ef-4d66-b28c-99a3adf04dda.png"></br>
   fig.129
</p>


```sh

Cell Rise Delay = ( 5.32564 – 5.11026 ) = 0.21538=0.215ps
```

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215958992-4da47209-7035-44fa-bf48-461a29a1f91a.png"></br>
   fig.130
</p>

```sh

Cell fall delay = ( 5.32564 – 5.11154 ) = 0.2141=0.214ps 
```

### MAGIC FEATURES & DRC Rules

The technology  file is a setup file that declares layer types,colors,patterns,electrical connectivity,DRC,device extraction rules and the rules to read LEF and DEF files.

Magic layout can be sourced from this link 

opencircuitdesign.com using this command:

wget https://opencircuitdesign.com/openpdks/archive/drc_tests.tgz

Lab 3 left in between due to some error 


# Day 4

The input and output ports is that there should be an intersection between vertical and horizontal tracks as shown in the tracks.info file. The CMOS Inverter input and output ports A and Y are on li 1 Layer.

To see the tracks.info file follow the given steps below:-
    
    1 First, go to the directory where your sky130A pdk file is stored. In my UBUNTU it is stored in this directory which is mentioned below:-

```sh

/Desktop/vsdflow/work/tools/openlane_working_dir/OpenLane/pdks/volare/sky130/versions/9f1c2b06d2b5a6708cfe0b55679c7e84d37220cc/sky130A/libs.tech/openlane/sky130_fd_sc_hd
```

    2 After this command do ls -ltr and see all the file content 

    3 Then, open the track.info file using this command: less tracks.info
    
    
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215959906-065e6094-ea0d-4d45-8296-f52e572f67ed.png"></br>
   fig.131
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215960000-10190494-bcd7-4cdb-8898-11124f6db5c2.png"></br>
   fig.132
</p>

These all are metal traces
