_Please stick to the headings and their order. Don't modify the words in bold. Your input is required at each occurrence of "e.g." and "..."._<br>
_You may use https://tex-image-link-generator.herokuapp.com/ to render math formulas in Markdown, see the examples below._

## Physics

### PDEs

One mass balance per component water and CO2.

### Constitutive relations

#### Fluid-matrix interaction

* **Capillary pressure:** Brooks-Corey
  ![p_c(S_{l}) = p_\text{entry}S_{le}^{-1/\lambda}](https://render.githubusercontent.com/render/math?math=%5Cdisplaystyle+p_c%28S_%7Bl%7D%29+%3D+p_%5Ctext%7Bentry%7DS_%7Ble%7D%5E%7B-1%2F%5Clambda%7D%0A)

* **Relative permeability:** Brooks-Corey

#### Phase composition: Applied equations of state

* **CO2 in liquid phase:** Peng-Robinson equation of state

* **Water in gas phase:** Not allowed.



#### Density

* **Liquid phase:** 

* **Gas phase:** 


#### Solubility limit

1.48 kg/m<sup>3</sup>.

### Temperature

20°C.

### Domain volume

0.105 m<sup>3</sup>.

### Spatial parameters

_Please provide the relevant facies parameters as a csv file._<br>
_E.g._ The parameters ![p_\text{entry}, \lambda, S_{lr}, S_{gr}](https://render.githubusercontent.com/render/math?math=%5Cdisplaystyle+p_%5Ctext%7Bentry%7D%2C+%5Clambda%2C+S_%7Blr%7D%2C+S_%7Bgr%7D%0A) for the different facies are given in [spatial_parameters.csv](spatial_parameters.csv).<br>
_Obviously, the number and type of parameters for your model might differ from the ones in the provided template._

## Numerics

### Coupling of flow and transport, temporal and spatial discretization

Fully coupled, fully implicit, enhanced velocity mixed finite element method.

### Linearization and Solvers

GMRES with AMG preconditioner.

### Primary Variables

_E.g._ Dependent on local phase composition:
* Both phases present:
  ![p_l, S_g](https://render.githubusercontent.com/render/math?math=%5Ctextstyle+p_l%2C+S_g%0A)...

### Computational Grid

140x75 Rectangular grids.

### Performance

| Indicator                            |  Average |      Min |      Max |
|:-------------------------------------|---------:|---------:|---------:|
| time step size [s]                   | 1.23e+56 | 1.23e+56 | 1.23e+56 |
| # nonlinear iterations per time step |      123 |      123 |      123 |
| # linear iterations per solve        |      123 |      123 |      123 |
