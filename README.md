# Seismic failure mode identification of reinforced concrete shear walls using ANN
<h2>Objective</h2>
<li>To identify failure modes of reinforced concrete shear walls.</li>
<br></br>
<p>A shear wall is a structural element that resists lateral forces such as wind forces in a reinforced concrete framed construction. Shear walls are commonly employed in high-rise buildings that are subjected to lateral wind and earthquake stresses. Wind forces become more significant as a structure's height grows in reinforced concrete framed constructions. The shear wall's shape and plan position have a significant impact on the structure's behavior. The shear walls should be placed in the middle of each half of the building from a structural standpoint. However, because it dictates the use of space, this is rarely practicable, thus they are placed at the ends.Despite advances in the use of machine learning techniques for failure mode and damage monitoring of building systems, no studies on data-driven approaches for shear wall failure mode assessment have yet been conducted. Shear walls are the most prevalent lateral load resisting structure, and there is yet no mechanics- or empirical-based model for shear wall failure mode detection.</p>
<center><h1>Failure modes</h1></center>

<center><img src="images\failure_modes.jpg"></center>
<br>
<center>
<h2>Label Encoding
<table>
  <tr>
    <th> Failure Modes</th>
    <th>Labels</th>
  </tr>
  <tr>
    <td>Flexural failure </td>
    <td>0</td>
  </tr>
  <tr>
    <td>  Flexure-shear failure </td>
    <td>1</td>
    
  </tr>
  <tr>
    <td>Shear failure </td>
    <td>2</td>
  </tr>
  <tr>
    <td>Sliding Shear failure </td>
    <td>3</td>
  </tr>
</table>
</h2>
<br></br>
</center>

<center><h1>Overview</h1></center>
<br></br>
<center><img src="images\Overview.jpg"></center>
<br></br>

<center><h1> Input features</h1></center>
<br></br>
<center><img src="images\Input_features.jpg"></center>
<br></br>
<h2>
<ul>
<li> Aspect ratio</li>
<li> Wall length to wall thickness ratio</li> 
<li> Concrete compressive strength </li>
<li> Vertical and horizontal reinforcement ratio of web</li>
<li> Vertical and horizontal reinforcement ratio of boundary element</li>
<li> Yield strength of vertical & horizontal reinforcement in web </li>
<li> Yield strength of vertical & horizontal reinforcement in boundary element</li>
<li> Gross cross sectional area of wall</li>
<li> Area of boundary element to area of gross sectional area of wall</li>
<li> Axial load ratio  P/fc'Ag </li>
<li>Cross section shape
</ul>
</h2>
<br></br>

<center><h1>Model definition</h1></center>
<br></br>

<center><img src="images\model_definition.jpg"></center>
<br></br>
<h2>
<ul>
<li>Input layer & hidden layer: ReLU</li>          
<li>Output layer : Softmax</li>
</ul>
</h2>
<br></br>

<center><h1>Training process</h1></center>
<h2>
<ul>
<li>Optimizer=Adam</li>
<li>Loss= Sparse Categorical Crossentropy</li>
<li>Metrics=Accuracy</li>
<li>Epochs=100</li>
</h2>
</ul>

<center><h1>Results</h1></center>
<br></br>

<center><img src="images\AccvsEpoch.jpg" width=800 height=500></center>
<br></br>

<h2>
<ul>
<li>Testing accuracy - 83.19%</li>
<li>Macro F1 score - 0.8335</li>
<li>Macro Precision - 0.8182</li>
<li>Macro Recall - 0.8564</li>

</ul>
</h2>
<center><img src="images\confusion_mat.jpg"></center>
<br>
<center>
<h2>F1 scores
<table>
  <tr>
    <th> Failure Modes</th>
    <th>F1 Score</th>
  </tr>
  <tr>
    <td>0 </td>
    <td>0.875</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0.701</td>
    
  </tr>
  <tr>
    <td>2</td>
    <td>0.8684</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0.8889</td>
  </tr>
</table>
</h2>
</center>
<br>

<hr>







