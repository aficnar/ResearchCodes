# ResearchCodes

Some of the Mathematica codes used in my physics research.

* **HolographicIsotropization-GenerateBackgrounds.nb** - code used in the upcoming paper to study how highly anisotropic, (infinitely) strongly coupled plasmas relax to a stationary state and become isotropic. This is done using holography, where the strongly coupled plasma dynamics are represented by dynamical evolution of a gravitational system in a curved spacetime in the presence of a black hole.
  * The code is based on the so-called characteristic formulation of general relativity, which combines the relevant equations of motion into a convenient, "nested" form, which is amenable to numerical evaluation.
  * The code automatically generates random, anisotropic (but homogeneous) initial conditions for the gravitational background, and adapts to make sure that all the necessary conditions for stable solutions are met (such as the existence of the apparent horizon, absence of caustics and so on).
  * The code then solves the PDEs of motion from scratch by using pseudospectral methods with a discretization on a Chebyshev grid to handle the spatial coordinate, and fourth order Runge-Kutta to evolve the results in time.
  * The results of the code are output as numerical data, which is then analyzed and used to compute the time evolution of the pressure anisotropy.

* **HolographicIsotropization-EvolvePerturbations.nb** - code used in the same upcoming paper as the above, with the goal of studying how anisotropic, strongly coupled plasmas isotropize, but in the more realistic setting when the plasma is strongly coupled, but with a finite value of the coupling. This is a more relevant case, closer to the conditions of realistic quark-gluon plasmas created in heavy ion collision experiments.
  * The effect of finite strong coupling can be modeled in holography by studying gravitational systems with higher curvature terms, such as the Gauss-Bonnet gravity. 
  * Since the relevant equations of motions are significantly more complex, we simplify the problem by linearizing them around the numerical solutions produced with the previous code.
  * A nested formulation is then obtained, and the PDEs are solved with similar methods as in the previous notebook, outputting the results as numerical data. 
  * This data is then analyzed and modeled (via regression), and an approximate analytic description is formulated in terms of the so-called quasinormal modes. 
  * Both this and the previous notebook have also been optimized to run on a cluster and generate large amounts of data.

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
  
* **ComparingWithLHCdata.nb** - code used in this [paper](http://arxiv.org/abs/1311.6160) to model the quark-gluon plasma
produced in heavy ion collisions at RHIC and LHC and implement our string theoretic (holographic) model for light quark energy loss 
from this [paper](http://arxiv.org/abs/1306.6648) in that plasma model. 
 * This is done in order to calculate a particular experimental observable (nuclear suppression factor) and compare to the relevant data from LHC and RHIC.
