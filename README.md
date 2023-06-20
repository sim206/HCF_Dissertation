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

<br/>
<br />
<br />
</p>


