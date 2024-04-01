# Spotpy_MONICA_Optimisation
Files and required Scripts for optimizing the simulation of Above-ground biomass (AGB), by the MONICA agroecosystem model using the SPOTPY optimization algorithm.
Study : DOI: 10.2139/ssrn.4740183

# Steps:
1. Prepare MONICA set-up: sim.json, site.json, crop.json, climate.cv;

2. Prepare the required file for optimising outputs:
		2.1. observation.csv: contain the measured values organised based on the key indicator, which for this example is DOY (Days Of Year).
   	2.2. calibratethese.csv: contains parameter names and their range, as well as the optimal value for the crop condition.
   	2.3.crop_sim_site_MAP.csv: Covers the exact namings of MONICA set up (step 1), and the name of the species and cultivar parameter, along with the crop ID
   
3. Prepare the required files for SPOTPY
   	3.1. MONICA_adapter.py: making env for parameters, MONICA set-up, defining output events
   	3.2. sampler_MONICA.py: read observation for parameter likelihood space calculation, number of reputation, applying the sceua algorithm for sampling, results and figure creation
   	3.3. spotpy_setup_MONICA.py: This section essentially provides an interface between spotpy and a MONICA model, allowing for calibration and optimization of the model parameters using spotpy's algorithms.
    




   
   
