<h1>Development of a Fatigue Life Methodology for High Cycle Fatigue using ANSYS Finite Element Analysis
</h1>


<h2>Description</h2>

This project aims to develop a methodology to complete high cycle fatigue (HCF) life analysis of components utilizing ANSYS Workbench. A cost-effective alternative method through Finite Element Analysis in evaluating fatigue life. Ultimately the methodology was applied to mechanical components from the (Self Mobility Improvement in the Elderly by Counteracting Falls) SMILING project. The components' lives were previously analysed in the FEA software ABAQUS. The components all surpassed the design life except for the bathtub and track components.

The results gathered were predominantly as expected based on the research acquired from the SMILING paper. Further mesh refinement was conducted, in addition to a contact study as fatigue life is sensitive to mean stresses, however, this is corrected through Goodman’s theory. The next stage was implementing Miner’s rule on the bathtub and track, as the connecting rod and crank have a large fatigue life and due to limitations of Miner's rule, a cumulative damage model could not be assessed for the two components. The results produced were compared to the fatigue tool available in ANSYS and a further damage model was assessed in ANSYS employing the fatigue combination tool. The results achieved and assessed by each model were compared and analysed.
<br />


<h2>Languages and Utilities Used</h2>

- <b>SolidWorks</b> 
- <b>Excel (Bill of Materials)</b>
- <b>Matlab</b>
- <b>ANSYS</b>
- <b>ABAQUS</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Project walk-through:</h2>

**Fatigue Analysis of SMILING Components**

The use of the Finite Element Method for fatigue analysis is an analytical method and simulation that has been widely explored, with a significant approach based on the stress-life method (S-N), a model used in HCF which provides a correlation between stress ranges and cycles to failure (Basquin)

**Notched and Unnotched S-N Curve**

The next step was to determine possible cycles of stress changes, based on which fatigue calculations were performed both analytically and with FEM. The S-N curve utilises the UTS of material to construct an approximate stress life curve for zero-based loading

</b>
<p align="center">
Un-notched and Notched Curves for Al 7075-T651: <br/>
<img src="https://i.imgur.com/10dNws9.png" height="80%" width="80%" alt="HCF"/>
<br />
<p align="center">
Un-notched and Notched Curves for 316 Stainless Steel: <br/>
<img src="https://i.imgur.com/Yfq9zcn.png" height="80%" width="80%" alt="HCF"/>  
<br />

**Finite Element Method and Fatigue Analysis**

The unit cell's fatigue study is conducted using the Finite Element (FE)programme ANSYS. The fatigue tool in ANSYS Workbench demands that fatigue material attributes be defined in terms of the S-N graph's alternating stress versus life graph. The S-N curve obtained above was utilized as the material input for the fatigue analysis for the SMILING components.

A contact study was conducted for each component to determine the effects between non-contact and contact modules, and if there was a significant difference that may account for the differences in fatigue life achieved by each component between ANSYS and ABAQUS

**Connecting Rod Analysis**

In the analysis of the connecting rod, a pin geometry was modelled in SolidWorks, and appropriate mates were added to ensure the rod's stability while assuming the pin was rigid. To reduce computational demand, a 1/8th geometry of the rod was created, and face splits were applied to the internal edges of the pin's cylindrical hole to account for stress concentrations at areas of abrupt cross-sectional changes. 

Frictionless supports were applied to symmetry faces, while fixed support was added to the pins, and a quartered horizontal load was applied to the centre of the pin to replicate the load from the upper crank. 

<p align="center">
Boundary Conditions applied to con-rod: <br/>
<img src="https://i.imgur.com/PhbfFuS.png" height="80%" width="80%" alt="HCF"/>  
<br />

<p align="center">
Refined mesh for the con-rod: <br/>
<img src="https://i.imgur.com/MH6OqYx.png" height="80%" width="80%" alt="HCF"/>  
<br />

**Results**

A plot of the von Mises stress in the model is shown below (a) and (b), with a maximum of 216.15 MPa at node 3440. The pins have been removed from the plots for clarity.
<p align="center">
(a) Maximum Principal Stress (b) Equivalent von-Mises stress: <br/><img src="https://i.imgur.com/sIpqXTR.png" height="80%" width="80%" alt="HCF"/>  
<br />

**Bathtub and Track Analysis**

In the analysis of the track and bathtub components, the geometry was created in Solidworks based on engineering drawings from the SMILING Project with the bathtub made of 7075 Aluminium and the track made of 316 Stainless Steel (cold drawn). To reduce computational demand, only half of the track and bathtub were modelled. An additional component, a baseplate, was designed as a rigid surface to support the slider and bathtub. The components were imported to ANSYS Workbench as a STEP file and further modified in the Design Modeller tab using face splits to create surfaces for applying boundary conditions. Stress concentration areas, such as fillets on the bathtub and internal fillets of the slider, were identified and face splits were generated accordingly.

Boundary conditions were applied, including a load and moment on the top surface of the bathtub, frictionless supports on planes of symmetry, and specific contact areas on the track due to resistive couple provided by steel bolts. The analysis utilized 10-node tetrahedral elements to account for quadratic displacement behaviour and irregular meshes.

<p align="center">
Boundary Condition applied to the Bathtub and track: <br/><img src="https://i.imgur.com/M1BoybP.png" height="80%" width="80%" alt="HCF"/>  
<br />

<p align="center">
Refined mesh for the bathtub and track components: <br/><img src="https://i.imgur.com/5keLNaj.png" height="80%" width="80%" alt="HCF"/>  
<br />

<p align="center">
Maximum Von-Mises stress contour plot for the bathtub: <br/><img src="https://i.imgur.com/vNZIZ1H.png" height="80%" width="80%" alt="HCF"/>  
<br />

<p align="center">
Cropped view of the bathtub indicating the max Von-Mises stress: <br/><img src="https://i.imgur.com/lC95Cqi.png" height="80%" width="80%" alt="HCF"/>  
<br />

<h2>Conclusions and Results</h2>

The damage done during the fatigue process is cumulative and generally unrecoverable as it is difficult to detect progressive changes in a material during fatigue, thus often occurring without warning. The analytical solution presented in this study allows for evaluating the number of cycles based on material data, following a similar approach to the SAE Handbook. This method serves as an alternative for conducting fatigue analysis and generating S-N curves when commercially available Finite Element Method programs are limited in their capabilities. The operational fatigue life of the components showed promising results, although discrepancies in the number of cycles to failure were observed due to assumptions and element distribution. The models could be enhanced by increasing mesh density in high-stress areas. Miner's rule was implemented for the bathtub component, as the connecting rod and crank had a large fatigue life. However, limitations of Miner's rule prevented assessing a cumulative damage model for these components. Despite some sources of error, the fatigue life prediction methods yielded similar results, though differing by a factor of 10. The track's fatigue life differed the most among the methods used compared to the results obtained in ABAQUS, potentially due to capturing results in ANSYS or the application of methodology. Life prediction modelling has contributed to improving component lives, including the use of surface enhancement procedures. Geometric optimization for fatigue can be performed before final product production, and compressive residual stress benefits are currently employed as an additional safety measure rather than incorporated into life prediction calculations.

**_Please contact me for more information on this project_**







<br/>
<br />
<br />
</p>


