# XCS_TELO

The attached code provides an XCS, a set of rule compaction algorithms and three visualization techniques. The code is based on Python 3.7. Visual Studio 2017 is the recommended platform. To run the provided code, you need to add numpy (https://numpy.org/install/) and matplotlib (https://pypi.org/project/matplotlib/) libraries to your python environment. 

The version XCSV2 is recommended. In this version, you can produce the TELO paper's visualization results of AFVM by invoking the code in visualization.py:

# title="6-bits Multiplexer"

# env=Environment(0,6,1000,'b')

# Address="RCompacted\\19_38_45_6MultiplexerRCR.txt"

# operator=Compacted_Model()

# R_AFVM=AFVM(Address,operator)

# png_Path="V_Result"

# V=Visualization(png_Path)

# V.Drew_MultiAction3D_Boolean(title,R_AFVM.AFVM_Data,R_AFVM.ActionList,360)

your results are expected in the "V_Result" folder

Furthermore, you can get the results of AFIM or FIM by changing the code:

# R_AFVM=AFVM(Address,operator)

# V.Drew_MultiAction3D_Boolean(title,R_AFVM.AFVM_Data,R_AFVM.ActionList,360)

For example, to produce the AFIM change the code to:

# R_AFIM=AFIM(Address,operator)

# V.Drew_MultiAction3D_Boolean(title,R_AFIM.AFIM_Data,R_AFIM.ActionList,360)

To produce the FIM, change the code to:

# R_FIM=FIM(Address,operator)

# V.Drew_Simple3D_Boolean(title,R_FIM.FIM_Data,360)

You can allow the system to visualize other problems by utilizing the given system to learn other problems. For example, utilizing the given XCS.py to train multiple models for the same problem, and then compacting these models with the given CompactAgent.py (Details please check the instruction). Change the address to the location of your compacted results.

We also provide a simple way to produce the result of the TELO paper, i.e. the version LCS.zip. This is an old version, which is not easy to be extended, but it can produce all the results of the TELO paper. Same as the XCSV2 this version also requires the numpy and matplotlib libraries. The models that can be visualized are stored in the folder ``V_Pop``.

To produce the visualization you need to run the visualization.py with the code (visualization result of 70-bits Multiplexer problem):

# Address="V_Pop\\MUX\\MUX702019_7_22_19_32_7.txt"

# Path="DResult\\"

# action_list=[0,1]

# vvp=Visualize_value_pattern(Address,action_list,Path,1)

Note in the vvp=Visualize_value_pattern(Address,action_list,Path,1), the last parameter determines which type of visualizations you are going to generate, i.e. 0 for the AFVM, and 1 for the AFIM. you are expected to collect your result in the ``DResult`` folder.

Change the address can output the visualization results for different problems. The following are some of the most important results of the TELO paper.

37 bits Multiplexer problem:

# Address="V_Pop\\MUX\\MUX37RCR2019_7_13_6_32_10.txt"

20 bits Multiplexer problem:

# Address="V_Pop\\MUX\\MUX20RCR2019_7_12_15_2_49.txt"

11 bits Multiplexer problem:

# Address="V_Pop\\MUX11RCR2019_7_11_5_58_34.txt"

6 bits Multiplexer problem:

# Address="V_Pop\\MUX6RCR2019_7_10_17_27_20.txt"

10 bits Carry problem:

# Address="V_Pop\\RCR\\Carry10RCR32019_7_13_3_15_47.txt"

11 bits Majority-On problem:

# Address="V_Pop\\RCR\\Majority11RCR32019_8_1_21_28_10.txt"

8 bits Majority-On problem:

# Address="V_Pop\\MOE\\Majority8RCR2019_7_12_4_40_45.txt"

7 bits Majority-On problem:

# Address="V_Pop\\MOO\\Majority7RCR2019_7_11_6_21_52.txt"
