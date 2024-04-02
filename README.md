# Spotpy_sceua_hymod_MONICA_Optimisation_Example 
Files and required Scripts for optimizing the simulation of Above-ground biomass (AGB), by the MONICA agroecosystem model using the SPOTPY optimization algorithm.
from the study : DOI: 10.2139/ssrn.4740183

# Steps:
1. Prepare MONICA set-up: sim.json, site.json, crop.json, climate.cv;

2. Prepare the required file for optimising outputs:
   
	2.1. observation.csv: contain the measured values organised based on the key indicator, which for this example is DOY (Days Of Year).
   
   	2.2. calibratethese.csv: contains parameters that we want to optimise and their range, as well as the optimal value for the crop condition.
   
   	2.3.crop_sim_site_MAP.csv: Covers the exact namings of MONICA setup (step 1), and the name of the species and cultivar parameter, along with the crop ID
   
3. Prepare the required files for SPOTPY
   
	3.1. sampler_MONICA.py: (The main routine, control the whole process) read observation for parameter likelihood space calculation, number of reputation, applying the sceua algorithm for sampling, results and figure creation
   
  	3.2. MONICA_adapter.py: (Include functions that are called by the sampler) making env for parameters, MONICA set-up, defining output events
    
   	3.3. spotpy_setup_MONICA.py: This section essentially provides an interface between spotpy and a MONICA model, allowing for calibration and optimization of the model parameters using spotpy's algorithms.


We need to start MONICA in PowerShell in the background to reproduce the result using the port to which the producer (tcp://*:6666) and the consumer (tcp://*:7777) will respond : 

monica-zmq-server -bi -i tcp://*:6666 -bo -o tcp://*:7777


   


   
   
