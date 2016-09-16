# Day 4 fMRI course

## Interaction Effects between measures (confounds)

### Multi-channel and norm based encoding models

* Multi-channel neural coding (aka uniform population code) ideally measured using adaptation. One clear example (Juang et al 2006) modulation of neural respoonse cencodes distance between stimuli.
* Norm based code (aka prototype representation). How far away from *average* face. More firing for more extreme example of stimulus. Can be measured by direct response. Caricature effect. Canonical examples by Loffner et al 2005, amplitude of neural response encodews distance from prototype.

Problem is both these methods are confounded in measurement. What it means to be centre of space means everything is more similar to you.
* Adaptation mistaken for norm based coding or vice versa.
* Can also be examined using ERP (Similarity effect)

Confounds can be measured using the carry-over designs.

## Questions

Topics:
  Motion, F.I.R (basis sets), SOA designs,

* Motion (and other Data preprocessing)
  * Sinc interpolation
    * project timing for each slice back in time when each slice acquired.
  * Motion - 
    * Effects of motion 6 DOF, rotations and translations (pitch roll yaw, up/down, left/right, forward/back)
    * 6DOF does not completely fix problem, each image is not instantaneous (ie slices), movement causes blurs. Also spin history effects, create signal changes that is completely non-linear. Commonly include covariate that models motion to include in data processing
    * Advanced motion detection fiducial markers, and more
  * Spatial Normalisation
    * Take brain and aligning to std rerefence frame
  * Smoothing
    * Commoon when looking for direct effects (not so for MVPA)
    * Reduce multiple comparison
    * Smooth with kernel with size of effect you are trying to measure.

* Analysis of data and experimental design
  * basis Sets, set of covariates that have property that a combination of such model variation of possible responses
    * One such basis set is HDR and first derivative. Model differneces in timing between expected and actual HDR
    * Basis Sets, impulses at time = 0,1,2,3,4... - FIR model (Finite Impulse Response, or shifted set of Dirac functions)
  * SOA (Stimulus Onset Asynchrony). Difference in timing for diff stimuli (rotated E vs vertical E), not different timing for different region.
