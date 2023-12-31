#  <div align="center"> 🦗 Woody 🦗 </div>  
###  <div align="left">3-Axis Milling CNC Postprocessor in Grasshopper3D
###  Rhinoceros curves to G-Code</div>  
###  <div align="left">*Profiles, pockets, engravings, re-machining, drilling operations. I use it mostly for furniture facade millings and drillings*</div>


<a href="https://www.youtube.com/watch?v=JxVLw4sx4c4&list=PLpTK_OZMfm1qI5HoSyZqZ8NEA13gcOjpX">
  <img src="https://100tails.ru/wp-content/uploads/2022/06/red-youtube-logo-png-xl.png" alt="YouTube playlist" width="30">
</a>

<div align="left">
<img src="Images\CNC2.gif" alt="Woody PREVIEW"  width="80%"/>
</div> 

*Testing trajectories in [NC Corrector](http://www.nc-corrector.inf.ua/index_EN.htm)☢️
<br>

> **⚠️Warning**<br>
> This is a work-in-progress and not the finished product.<br>
><br>
> Feel free to leave suggestions or report bugs in<br>
> the [issues](https://github.com/SahaSG552/Woody/issues) section.<br>

# Demo
<div align="center">
<img src="Images\CNC1.gif" alt="Woody PREVIEW"  width="100%"/>
</div> 


First of all you need to choose cutting material from database, or from referenced geometry and set LCS (Local Coordinate System). In this demo i chose 19mm MDF, rectangled shape from curve.<br>
You can select multiple pieces of material and place them wherever you need, machining will be carried out relative to the established initial coordinate system.<br>
Then you need to create geometry in specially named layer. Operation will be performed according layer name. There are some layer naming rules, but i didn't implement documentation yet 😏 Hope it will be soon<br>
In this example layer named `D10_19MM_SN` means that cutting instrument would be `D10` (cylinder 10mm diameter bit), cutting depth will be `19MM` and `SN` means that bit will be cutting outside profile.
You can combine curves and nest them within each other.

# Operations
- General<br>
    Inclined plunge cutting (engage in material under the certain angle)<br>
    Conventional/climb/mixed cutting direction<br>
    Optional nested geometry detection (geometry in geometry)<br>
    Circular interpolation (G2/G3 codes)<br>
    Different types of sorting including sorting by selection<br>

- Profile machining operation<br>
    Inside, outside, along profile<br>

- Pocketing operation<br>
    Effective cleaning of leftovers<br>

- Re-Machining<br>
    Cleaning corners after pocketing operation using smaller diameter bit<br>

- V-Carving operation<br>
    Corner sharpening movement using cone bit<br>

- Drilling operation<br>


## Example project
<div align="left">
<img src="Images\CNC1.jpg" alt="Plugins Used"  width="100%"/>
</div> 
In this project using several instruments, each instrument could do several operations (one layer - one operation)

## Testing in NC Corrector
 <div align="left">
<img src="Images\CNC2.jpg" alt="Simulation"  width="100%"/>
</div> 

## Worklist image generator
 <div align="left">
<img src="Images\CNC3.jpg" alt="Worklist image generator"  width="100%"/>
</div> 

This image is needed for the machine operator to give them a task. The image shows the geometry for processing, a list and order of the required operations, and automatically calculated processing time for each operation.

## 3rd Party Plugins Used
 <div align="left">
|<img src="Images/CNC4.jpg" alt="Plugins Used"  width="50%"/>
</div> 

- NEW! Some sort of simulation using slider
 <div align="left">
|<img src="https://global.discourse-cdn.com/mcneel/uploads/default/original/4X/2/5/7/2572ccaf2bdaa92afc846970217339d37dc68439.gif" alt="Plugins Used"  width="100%"/>
</div> 

## In progress...
