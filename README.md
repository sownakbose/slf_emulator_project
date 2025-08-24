# slf_emulator_project
This repository contains data sets used in the work by Bose & Deason (2025, arXiv: XXXX.XXXX). We provide access to the processed (binned) satellite luminosity function (SLF) and mass-metallicity relations (SMZ) from the 2600 Latin hypercube Galform runs,  which act as the starting point for our investigation. 

Each of these data sets is store as a _.npy_ file, and can be loaded into a Numpy array by simply executing:
```
input_data = np.load("filename.npy")
```

* the file _bin_centres.npy_ contains the bin centres (in absolute M_V) used for the SLF and SMZ
* file names with _satlf_*_ contain the binned luminosity function
* file names with _satmz_*_ contain the binned mass-metallicity relation
* file names ending with __mean_ and __std_, respectively, refer to mean or 1-sigma scatter associated with that statistic
* file names with _model_ are of size (23, 2600), where the first dimension refers to the number of bins, and the second to the total number of runs. Each model is therefore stored in one column of this matrix.
* file names with _fiducial_ contain the data for the fiducial Lacey et al. (2016) Galform model.
* the combination of the 11 input parameters corresponding to each of the runs is stored in _inp_params.npy_, which has size (11, 2600). The parameters are stored in the following order: ($z_\mathrm{reion}$, $V_\mathrm{crit}$, $f_\mathrm{burst}$, $f_\mathrm{ellip}$, $\nu_\mathrm{SF}$, $\gamma_\mathrm{SN}$, $V_\mathrm{SN}^\mathrm{disk}$, $V_\mathrm{SN}^\mathrm{burst}$, $\alpha_\mathrm{ret}$, $V_\mathrm{sat}$, $F_\mathrm{stab}$). See Table 1 of the paper for their descriptions.
