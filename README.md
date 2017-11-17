# rungen-mn
This script will generate the run.sh files needed to run VASP calculations in MareNostrum 3. 
About MareNostrum: https://www.bsc.es/

# Instructions 

* Create ~/bin/rungen and put the content below 

* Make it executable 
 chmod +x ~/bin/rungen

* To use it in tekla, put the name, the queue (4, 8, 12, or 24), and the number of processors. If you make a mistake in the number of processors the script will tell to you.  
 rungen nanoparticle 12 60 

* You can change the VASP version using an additional fourth input variable: 
 rungen neb 12 48 5.3.5-IB_VTST_GAMMA

* In MareNostrum, use 48a, 48b, 48c, and 48d for class_a, class_b, class_c, and debug queues: 
 rungen neb 48 96 

* If you want to change the VASP version, go to this folder to see what versions do you have available. The default is ''vasp_std'': 
 /apps/VASP/5.4.4/INTEL/IMPI/bin/ 
 rungen neb 48 96 vasp_gam_sol

* If you want to use an exotic flavour that is not yet compiled for the version you are using, you can request MareNostrum people to compile it. Ask your boss before doing the request. Otherwise, you can use an older version of VASP. Feel free to explore into these MareNostrum folders: 
 /apps/VASP/

* Remember to adapt your parallelization to the machine and processors you use each time.[http://aliga.iciq.es/wiki/index.php/The_INCAR_file#Improving_Parallelisation]
