# XCS_TELO

The attached code provides an XCS, a set of rule compaction algorithms and three visualization techniques. The code is based on Python 3.7. Visual Studio 2017 is the recommended platform. To run the provided code, you need to add numpy (https://numpy.org/install/) and matplotlib (https://pypi.org/project/matplotlib/) libraries to your python environment. 

The version XCSv2 is recommended. In this version, you can produce the TELO paper's visualization results of AFVM by invoking the code in visualization.py:

#title="6-bits Multiplexer"

#env=Environment(0,6,1000,'b')

#Address="RCompacted\\19_38_45_6MultiplexerRCR.txt"

#operator=Compacted_Model()

#R_AFVM=AFVM(Address,operator)

#png_Path="V_Result"

#V=Visualization(png_Path)

#V.Drew_MultiAction3D_Boolean(title,R_AFVM.AFVM_Data,R_AFVM.ActionList,360)

your results are expected in the "V_Result" folder

Furthermore, you can get the results of AFIM or FIM by changing the code:

#R_AFVM=AFVM(Address,operator)

#V.Drew_MultiAction3D_Boolean(title,R_AFVM.AFVM_Data,R_AFVM.ActionList,360)

For example, to produce the AFIM change the code to:

#R_AFIM=AFIM(Address,operator)

#V.Drew_MultiAction3D_Boolean(title,R_AFIM.AFIM_Data,R_AFIM.ActionList,360)

To produce the FIM, change the code to:

#R_FIM=FIM(Address,operator)

#V.Drew_Simple3D_Boolean(title,R_FIM.FIM_Data,360)


