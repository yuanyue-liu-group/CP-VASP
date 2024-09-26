![CP-VASP image](https://github.com/yuanyue-liu-group/CP-VASP/blob/main/CP-VASP.jpg?raw=true)

# CP-VASP
<p>Thank you for taking interest in CP-VASP! CP-VASP is a patch to the Vienna Ab-Initio Simulation Package (VASP) to enable DFT calculations under constant electrode potential. Using CP-VASP, the electron number, energy, and forces can be determined for any structure under a given electrode potential. Thus, CP-VASP enables structural relaxation and molecular dynamics (MD) simulation under a fixed electrode potential.</p>

<p> We have recently developed version 2 of CP-VASP. This README contains instructions for installing and using version 2. If you would like to use a previous version, navigate to the desired version and consult the README in the corresponding folder.</p>

# Prerequisites
<p>CP-VASP is currently compatible with VASP version 6.3.2 and 6.4.2. Please see the VASP manual for download instructions:  
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
<p> If you encounter issues using CP-VASP or have questions/comments, please check the issues tab on this GitHub repository. If you don't see your issue or question, please make a post and we will assist you. </p>

# Authors
<p>Xunhua Zhao<br>
    Saerom Yu<br>
    Zachary Levell<br>
    Ruoyu Wang<br>
    Yuanyue Liu</p>

# How to Cite
<p>Please cite the following publications when using CP-VASP in your research: <br>
<ul>
    <li>Zhao, X.; Liu, Y. Origin of Selective Production of Hydrogen Peroxide by Electrochemical Oxygen Reduction. <em>Journal of the American Chemical Society</em> <strong>2021</strong>, <em>143</em> (25), 9423-9428.</li>
    <li>Yu, S.; Levell, Z.; Jiang, Z.; Zhao, X.; Liu, Y. What Is the Rate-Limiting Step of Oxygen Reduction Reaction on Fe–N–C Catalysts? <em>Journal of the American Chemical Society</em> <strong>2023</strong>, <em>145</em> (46), 25352-25356.</li>
</ul></p>
