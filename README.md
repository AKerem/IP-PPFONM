# Indoor Positioning via Prefiltering and Particle Filtering with Obstruction-aware No-signal Multilateration (IP-PPFONM) Using Bluetooth Low Energy 
A wireless indoor positioning system that uses BLE signals.


**********************
1) CODE DESCRIPTION:

"IP-PPFONM.py" is the base code that includes all functionalities of the IP-PPFONM. This script includes whole IP-PPFONM algorithm and the IP-PPFONM simulation tool which simulates this algorithm visually. 

The visuals in the thesis made adjusting some variables and lines of this base code.
Comment out the lines in "IP-PPFONM.py" reading "Comment out" or uncomment the lines where it reads "Uncomment" to open more functionalities as mentioned in the corresponding commented out lines. Please search the code with these keywords ("Comment out" and "Uncomment") to see all the lines that can be commented out or can be added by uncommenting corresponding lines to utilize the algorithm with different parameters/setups.

The "IP-PPFONM.py" code, with the current parameter settings, do not take fingerprinting data into account since "UseFingerPrintingIn_IPPPFONM" is False, simulates a single person walking in an indoor environment with random but valid movements (does not go out of map etc.), generates two blocks randomly on the map and places three places in the most useful positions as possible using k-means algorithm. The other parameters can be checked and modified in the code.

The utility functions used to draw and plot the figures/charts to show IP-PPFONM results can be found under "Utilities" folder. The content of this folder will be updated to reflect the changes made in the plots.
Moreover, in "Utilities/realWorldEnvironment_Experiments" folder; the variation of "IP-PPFONM.py" which is used in a real world environment (an office) where the parameters are pre-set can be found if how the parameters of IP-PPFONM.py should be changed is not clear enough.

There are also automation scripts written in Bash, running the IP-PPFONM algorithm for various different setups by running each setup 20 times and then calculates the mean and standard deviation of all the errors. Afterwards, these scripts produce error line segments on bar charts. These scripts will hopefully be available in a month under "Utilities" folder in the coresponding folders depending on the experiment type. These scripts are only used for visualizing the errors of "IP-PPFONM" algorithm with bar charts for various different setups and has NO OTHER RELATION to the "IP-PPFONM" algorithm (these are separate scripts used locally to produce bar charts using IP-PPFONM and not a part of IP-PPFONM algorithm)

Please read the README files in Utilities and Utilities/realWorldEnvironment_Experiments folders for more clarification.

For any questions related to the code, please reach me out at akeremtaskan@gmail.com.

**********************
2) CODE REQUIREMENTS:

-> Usage of Python2 is required (>=2.7)  
-> Code is confirmed to run on Ubuntu 16.04 and 20.04.1.  
-> The following libraries are required to run the code:   
numpy  
matplotlib.pyplot  
tkinter (python-tk)  
scipy  
filterpy  
sklearn  
shapely  
dvipng  

-> The packages/libraries can be installed by running the commands below in terminal:  
pip install numpy  
python -m pip install -U matplotlib  
sudo apt install python-tk  
python -m pip install -U scipy  
python -m pip install -U filterpy  
python -m pip install -U sklearn  
python -m pip install -U shapely  
sudo apt install dvipng texlive-latex-extra texlive-fonts-recommended  

