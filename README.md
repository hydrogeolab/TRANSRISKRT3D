TRANS-RISK-RT3D is a MATLAB/OCTAVE tool for computing transient Tier3 human health risk assessment (HHRA) using time-varying parameters in RT3D. 

When using the code, please cite
Authors: (will be disclosed when the manuscript is accepted) 
Title: "An integrated tool for transient Tier-3 Human Health Risk Assessment using multispecies reactive  transport models with dynamic parameter updates" 
Journal: (the manuscript is currently under review on Environmental Modeling & Software).
DOI/Year/Volume, Issue, Pages: (will be indicated when the manuscript is published).

TRANSRISKRT3D uses MODFLOW-96 and RT3D executables installed in the directory C:\Simcore\PM8,
which is the default installation directory of public domain software PMWIN 8
https://www.simcore.com/wp/archive/ (accessed on 11 October 2025). Although these files
can be obtained from other sources, TRANSRISKRT3D was tested only using the files included in PMWIN 8.

The example provided in this script is based on three sequential phases. If more phases need to be
simulated, add them by defining other initial inputs (e.g., "TRANSRISKRT3D_RTC4", "tottime_4", "PT_phase4",
for phase 4; etc) and adding new phase blocks after Phase 3 (rename the variables
according to the number of phases, e.g., %% Phase 4; "if % skip_phase4~=1", 
"disp('Now computing phase 4...'); "nph=4;", etc)

When loading the zip file, 
(1) COMPUTE TRANSIENT SIMULATIONS USING MULTISPECIES REACTIVE TRANSPORT MODEL
(2) TRANSIENT HUMAN HEALTH RISK ASSESSMENT
When downloaded, the zip file must be unzipped in a folder (e.g., "C:\Users\[Windows username]\TRANSRISKNET"). The user will find the following structure

/TRANSRISKRT3D/

  ├─ project_executed /
  
  ├─ common_functions/
  
  └─ common_data/
  
The common_functions and common_data folders contain MATLAB/OCTAVE .m scripts, functions, text files, and supporting data required for the simulations. These files are temporarily copied into the working directory, where the two main scripts are executed (TRANSRISKRT3D_1_rt3d.m for Step 1; TRANSRISKRT3D_2_risk.m for Step 2). After each step, temporary files are automatically deleted to clean up the working environment. The project_executed subfolder includes a fully executed example corresponding to the “default” scenario analyzed in the manuscript.
