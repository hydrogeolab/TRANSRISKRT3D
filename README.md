TRANSRISKRT3D is a MATLAB/OCTAVE tool for computing transient Tier3 human health risk assessment (HHRA) using time-varying parameters in RT3D. 

When using the code, please cite

$${\color{red}D.Pedretti, \ M.Masetti, \ L.Cavalca \ (2026) \ J. \ Hazardous \ Materials \}$$
**An integrated tool for transient Tier-3 Human Health Risk Assessment using multispecies reactive  transport models with dynamic parameter updates** (Volume 507, 141725, https://doi.org/10.1016/j.jhazmat.2026.141725) $${\color{red}Open \ access}$$

TRANSRISKRT3D uses MODFLOW-96 and RT3D executables installed in the directory C:\Simcore\PM8,
which is the default installation directory of public domain software PMWIN 8
https://www.simcore.com/wp/archive/ (accessed on 4 Feburary 2026). Although these files
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

TRANSRISKRT3D is free and open-source software under the GNU GPLv3 license. https://www.gnu.org/licenses/gpl-3.0.html. No warranty, expressed or implied, is made by the authors or corresponding affiliations as to the correct functionality of the software and related material, nor shall the fact of release constitute any such warranty. 


![alt text](https://github.com/hydrogeolab/TRANSRISKRT3D/blob/main/web.png)
