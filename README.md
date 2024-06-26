# CP-VASP
Thank you for taking interest in CP-VASP! CP-VASP is a patch to the Vienna Ab-Initio Simulation Package (VASP) to enable DFT calculations under constant electrode potential. Using CP-VASP, the electron number, energy, and forces can be determined for any structure under a given electrode potential. Thus, CP-VASP enables structural relaxation and molecular dynamics (MD) simulation under a fixed electrode potential.

# Prerequisites
CP-VASP is currently compatible with VASP version 6. Please see the VASP manual for download instructions: 
    https://www.vasp.at/wiki/index.php/Installing_VASP.6.X.X

CP-VASP also requires installing VASPsol. The VASPsol documentation can be found here: 
    https://github.com/henniggroup/VASPsol/tree/master. 

We note that the developers have released an updated patch file for VASP6 that can be found here: 
    https://github.com/henniggroup/VASPsol/issues/43.

# Installation
Please visit our group's page (https://sites.utexas.edu/yuanyue-liu/codes/cp-vasp/) and fill out the request form. We will subsequently give you access to the patch files.

If you are using VASP version 6.4 or 6.3, use the vasp6.4_6.3_cpm.patch file. If you are instead using VASP version 6.2 or 6.1, use the vasp6.2_6.1_cpm.patch file. To apply the patch, navigate to the /src directory in your VASP folder and copy the appropriate patch file into it. Then execute the following command (assuming you are using VASP version 6.4):
    patch -p0 < vasp6.4_6.3_cpm.patch

# Instructions
See "CP-VASP Manual.pdf" for detailed instructions on using CP-VASP. We have also provided a few examples in "CP-VASP Examples.pdf".

# Discussions and Feedback
If you encounter challenges with CP-VASP or have comments, please check our discussion board on this GitHub repository. We are happy to answer any questions.

# Authors
Xunhua Zhao
Saerom Yu
Zachary Levell
Yuanyue Liu

# How to Cite
Please cite the following publications when using CP-VASP in your research:
* Zhao, X.; Liu, Y. Origin of Selective Production of Hydrogen Peroxide by Electrochemical Oxygen Reduction. Journal of the American Chemical Society 2021, 143 (25), 9423-9428.
* Yu, S.; Levell, Z.; Jiang, Z.; Zhao, X.; Liu, Y. What Is the Rate-Limiting Step of Oxygen Reduction Reaction on Fe–N–C Catalysts? Journal of the American Chemical Society 2023, 145 (46), 25352-25356.
