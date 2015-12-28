# ResearchCodes

Some of the Mathematica codes used in my physics research.

* **ComparingWithLHCdata.nb** - code used in this [paper](http://arxiv.org/abs/1311.6160) to model the quark-gluon plasma
produced in heavy ion collisions at RHIC and LHC and implement our string theoretic (holographic) model for light quark energy loss 
from this [paper](http://arxiv.org/abs/1306.6648) in that plasma model. 
 * This is done in order to calculate a particular experimental
observable (nuclear suppression factor) and compare to the relevant data from LHC and RHIC.

* **Holographic3JetEvents.nb** - code used in this [paper](http://arxiv.org/abs/1512.00371) to simulate and analyze first 
string theoretical (holographic) models of three-jet events (emission of a gluon from a back-to-back pair of jets). 
  * In the first part of the code, a numerical simulation of a holographic 3-jet is performed using classical strings, and 
this is compared to the analytical prediction for the evolution of these strings described in the paper. 
  * In the second part, 
an automated code loops over many relevant 3-jets initial conditions, simulates the holographic jets and extracts the relevant data
from the simulations,
which is later analyzed in order to discover and confirm an important relationship between the energy of the jets and 
their angle, as described in the paper.

* **QNMinGRDWbackgrounds.nb** - code used in this [paper](http://arxiv.org/abs/1507.06556) to simulate a string theoretical (holographic)
model of a dense quark-gluon plasma and calculate the quasinormal modes in it, which govern the response of the system to small 
perturbations. 
  * The spacetime backgrounds representing the plasma are found by constructing a weighted 2-to-2 numerical 
interpolation between the space of initial conditions and the relevant physical parameters. 
  * Quasinormal modes are then found by the shooting method, in which one numerically solves the relevant equation of motion 
in these backgrounds using a range of initial conditions, and then, using clustering, finds the initial conditions regions
that give the right boundary conditions.
  * The results are also compared to the analytical estimates from this [paper](http://arxiv.org/abs/1503.07149), 
with numerical derivatives obtained using pseudospectral methods. 

* **ShootingStrings&PseudospectralMethods.nb** - the code used in this [paper](http://arxiv.org/abs/1306.6648) to numerically 
simulate classical strings with our novel boundary conditions, potentially relevant for describing energy loss of light quarks
in quark-gluon plasma.
  * Due to the complexity of the new boundary conditions and the kind of strings relevant for our work, a pseudospectral code, 
  written from scratch, was used to numerically solve the relevant PDE equations of motion.
