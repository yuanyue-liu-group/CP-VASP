![CP-VASP image](https://github.com/yuanyue-liu-group/CP-VASP/blob/main/CP-VASP.jpg?raw=true)

# CP-VASP
<p>Thank you for taking interest in CP-VASP! CP-VASP is a patch to the Vienna Ab-Initio Simulation Package (VASP) to enable DFT calculations under constant electrode potential. This is essential for accurately simulating the electrochemical interface, where the Fermi level is controlled by external electrode potential. CP-VASP enables fixed-structure calculation, structural relaxation, and molecular dynamics (MD) simulations under a given electrode potential. </p>

<p>As shown in the lefthand figure above, the supercell for CP-VASP is made of an explicit region with atoms of interest and an implicit region that models the solution as a dielectric continuum containing point charges (where the dielectric continuum represents the solvent, and the point charges represent the electrolyte ions). The supercell is connected to an “electrode” with potential U<sub>ext</sub>. CP-VASP tunes the number of electrons in the explicit region to change the average Fermi level to a target value set by Uext. These net electronic charges are balanced by the ionic charges in the implicit region to keep the system charge neutral. </p>

<p>CP-VASP has various algorithms to tune the electron number. Particularly, for MD simulations, it can emulate the “true” grand-canonical ensemble of electrons to produce the correct Fermi level fluctuation (see the righthand figure above). Moreover, it implements “flash solvation” technique which avoids the “flying solvent” problem at the explicit-implicit interface (see section 6 in the manual). This technique also significantly accelerates the MD simulation. </p>

<p>We have recently developed version 2 of CP-VASP. This README contains instructions for installing and using version 2. If you would like to use a previous version, navigate to the desired version and consult the manual in the corresponding folder.</p>

# Prerequisites
<p>CP-VASP version 2 is currently compatible with VASP version 6.3.2 and 6.4.2. Please see the VASP manual for download instructions:  
    https://www.vasp.at/wiki/index.php/Installing_VASP.6.X.X</p>

<p>CP-VASP also requires installing either VASPsol++ or VASPsol (VASPsol++ is currently only compatible with VASP 6.3.2). The instructions for installing VASPsol++ and VASPsol can be found at the following links:<br>
    VASPsol++: https://github.com/VASPsol/VASPsol<br>
    VASPsol: https://github.com/henniggroup/VASPsol/tree/master</p>

<p>We note that the developers of VASPsol have released an updated patch file for VASP6 that can be found here:  <br>
    https://github.com/henniggroup/VASPsol/issues/43.</p>

# Installation
<p>Please fill out the request form at the link below. We will subsequently give you access to the patch files. <br>
    https://docs.google.com/forms/d/e/1FAIpQLSdjinABLY26jora50jedL5X6bj5Pc7BTeys5pmclstlWs46Lw/viewform </p>

<p>If you are using VASPsol++, use the cp-vaspol++.patch file. If you are instead using VASPsol, use the cp-vaspsol.patch file. To apply the patch, navigate to the /src directory in your VASP folder and copy the appropriate patch file into it. Then execute the following command (assuming you are using VASPsol++):  
    patch -p0 < cp-vaspsol++.patch </p>

# Instructions
<p>See "CP-VASP Manual.pdf" under the folder for your desired version of CP-VASP for detailed instructions on using CP-VASP. We have also provided a few examples in "CP-VASP Examples.pdf".</p>

# Troubleshooting & Discussion
<p>If you encounter issues using CP-VASP or have questions/comments, please check the issues tab on this GitHub repository. If you don't see your issue or question, please make a post and we will assist you. </p>

# Authorship
<p>CP-VASP was developed by Zachary Levell*, Ruoyu Wang*, Saerom Yu*, Xunhua Zhao, and Yuanyue Liu. (* These authors contributed equally) </p>

# How to Cite
<p>Please cite the following publications when using CP-VASP in your research: <br>
<ul>
    <li>Zhao, X.; Liu, Y. Origin of Selective Production of Hydrogen Peroxide by Electrochemical Oxygen Reduction. <em>Journal of the American Chemical Society</em> <strong>2021</strong>, <em>143</em> (25), 9423-9428.</li>
    <li>Yu, S.; Levell, Z.; Jiang, Z.; Zhao, X.; Liu, Y. What Is the Rate-Limiting Step of Oxygen Reduction Reaction on Fe–N–C Catalysts? <em>Journal of the American Chemical Society</em> <strong>2023</strong>, <em>145</em> (46), 25352-25356.</li>
</ul></p>
