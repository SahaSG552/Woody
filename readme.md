#  <div align="center"> 🦗 Sudden CNC Post 🦗 </div>  
###  <div align="left">3-Axis CNC Postprocessor in Grasshopper3D
###  Rhinoceros curves to G-Code</div>  
###  <div align="left">*Profiles, pockets, engravings, re-machining, drilling operations. I use it mostly for furniture facade millings and drillings*</div>

<div align="left">
<img src="blob\main\images\CNC2.gif" alt="Sudden CNC Post"  width="80%"/>
</div> 

*Testing trajectories in NC Corrector ☢️
<br>

## Demo

 <div align="center">
|<img src="images\CNC1.gif" alt="Sudden CNC Post"  width="100%"/>
</div> 
First of all you need to choose cutting material from database, or from referenced geometry and set LCS (Local Coordinate System). In this demo i chose 19mm MDF, rectangled shape from curve.<br>
You can select multiple pieces of material and place them wherever you need, machining will be carried out relative to the established initial coordinate system.<br>
Then you need to create geometry in specially named layer. Operation will be created according layer name. There are some layer naming rules, i didn't implement documentation yet 😏<br>
In this example layer named D10_19MM_SN means that cutting instrument would be D10 (cylinder 10mm diameter bit), cutting depth will be 19MM and SN means that bit will be cutting outside profile.
You can combine curves and nest them within each other.

## Operations
- General<br>
    Inclined plunge cutting<br>
    Conventional/climb/mixed cutting direction<br>
    Optional nested geometry detection<br>
    Circular interpolation (G2/G3 codes)<br>
    Different types of sorting including sorting by selection<br>


- Profile machining operation<br>
    Inside, outside, along profile<br>

- Pocketing operation<br>
    Effective clean of leftovers<br>

- Re-Machining<br>
    Cleaning corners after pocketing operation using smaller bit diameter<br>

- V-Carving operation<br>
    Corner sharpening movement<br>

- Drilling operation<br>


## Example project
 <div align="left">
|<img src="images\CNC1.jpg" alt="Plugins Used"  width="100%"/>
</div> 
Several instruments, each instrument could do several operations (one layer - one operation)

## Testing in NC Corrector
 <div align="left">
<img src="images\CNC2.jpg" alt="Plugins Used"  width="100%"/>
</div> 

## Worklist image generator
 <div align="left">
<img src="images\CNC3.jpg" alt="Plugins Used"  width="100%"/>
</div> 

This image is needed for the machine operator to give them a task. The image shows the geometry for processing, a list and order of the required operations, and automatically calculated processing time for each operation.

## 3rd Party Plugins Used
 <div align="left">
|<img src="images\CNC4.jpg" alt="Plugins Used"  width="50%"/>
</div> 


## In progress...
