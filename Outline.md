## It's science baby

* B0 is direction of magnetic field
* M0 is average direction of alignment of protons within b0
* T1, T2, T2\* (fMRI)
  * T2\* is component that does not re-phase after 180 degree pulse (T2 dephase, T2\* is component that does not refocus)
  * Microscopic distortions of magnetic field cause the T2\* component, one source of this is blood
  * BOLD - Blood oxygen level dependant fMRI due to oxygen attached to hemoglobin, as oxygenated and deoxygenated hemoglobin have differnt magnetic properties
  * At each point in fMRI image, it represents amount of distortion
  * Blood vessels increase in size with activity.
  * Activity -> Increase blood vessel size -> more deoxyhemoglobin -> change in magnetic local properties as measured by T2\* -> Image
* Scanner with larger gradient coil strengths that can change configuration quickly are best for fMRI

## Microscopic > Global

* Brain activity -> fMRI Image mostly a linear system
* Stimulation -> Brain activity is non-linear
* Impulse Response Function measured to input in linear system means from measurement can calculate input to system
* In BOLD fMRI this IRF is called the hemodynamic response function (HRF)
* Different people/populations can have different HRF, Different regions/different drugs/hormonal state etc can affect HRF
* BOLD is slow, averaged out response compared to neuron spikes -> 3-4 seconds time resolution
* A point of neural activity evokes a blood flow response about 3mm wide -> 3mm spatial resolution
* These are fundamental limitations of BOLD fMRI, and are biological/physical limitations (blood flow is slow and broad) rather than scanner limitations

## Inferring from Data

* Basic data processing steps: Correct for motion (6DOF + covariates to deal with spin history effects etc), Sinc Interpolation to get each volume in same time, Smnooth data to increase statistical power , ie reduce multiple comparison (Direct effects), Spatial Normalisation - ie align to std reference frame.
* Claims about groups vastly different about a claim about an individual person. fMRI is a Relative signal - within subjects relative change
* Indirect Measure - BOLD fMRI signal has no direct absolute interpretation - no units. Must be compared between states. A control experiment to account for group differences in blood flow (drug use, age etc) is often useful/necessary. Also an integrated measure so only detectable if there is a bulk change in neural activity, as opposed to change in pattern of firing.
* Bonferroni correction (crude way), divide statistical value by number of voxels to reduce false positives. (Not using this comes up with results such as dead salmon showing activation)
* 2 basic types of neuroimaging studies (and a third that combines the two).
  * **Forward Inference** The brain area for "love". ie a brain area that corresponds to isolated behaviour. Isolate such behaviour by subtracting conditions (ie subtract images of friend from images of wife. Key problem is that all sorts of other things may be included in subtraction. A classic example is working memory - assumes pure insertion, that adding say working memory between perception and response does not change other aspects such as response execution. An alternative is parametric manipulation where the *amount* of cognitive process varies in each condition. Does not completely remove assumption of pure insertion. **Task vs cognitive operation** is a critical thing to think of when designing and evaluating experiments. Lesion inferences and imaging study are largely independent (remove part of brain does not necessarily mean cognitive process is removed).
  * **Focal Reverse Inference Study** claims identify cognitive state from brain region activated. Key assumption is that particular region is only activated by one state. So pain activates a region, test every single other possibility stimuli???
  * **Multi-voxel pattern analysis** - Step1: What is the difference in pattern across the brain or region for a particular state/stimulus. Step 2: Given a new statement/stimulus, use classifier from step 1 to decode somethin new. Key question is how well this generalises beyond a training set.
* Blocked and evet-related designs. HRF favors designs with power at low temporal freqs. Changes in signal < about 4 seconds basically undetectable in fMRI signal.
* However intrinsic noise at low frequencies is high.
* Balancing noise and HRF has a optimal point of ~ 20 seconds.
* Tradeoffs between estimation efficiency and detection power. For some experiments we need stimuli to be randomised - but this is challenging. So event related designs are less statistically powerful.

###Carry over designs

3 Types of measures
  * BOLD fMRI amplitude (Increase of amplitude in realtion to contrast, particular object/stimulus) *Average direct effect of stimulus*
  * *Distributed Pattern Analysis* Patterns of voxel activation within group correlated, but between groups not correlated. Pattern of direct effects across voxels (not average)
  * *Within voxel adaptation* Neurons have reduced response to repetition of stimulus. Neural adaptation studies, looking at modulatory effect of one stimulus on the next.

Continuous carry-over designs, a method to silmultaneously and efficiently measure within-voxel adaptation effects and across voxel distributed pattern responses. Order of stimuli serially counter-balanced, continuous presentation, no stimulus pairing.
Neural response to stimulus @ time = sum of mean response, direct effect (distributed pattern analysis) and influence of prior stimulus (within voxel neural adaptation)
Tyoes of modulatory effects:
  * Neural adaptation, linear adaptation, has property that it's symmetric
  * Bias effects, asymmetric

Counterbalancing can be done with de Bruijn cycles.

Must control for different sized sets of stimuli.

### Applications of carry over designs

Integral (Euclidean) dimensions, not automatically seen as different things (colour = hue + brightness)
Separable (city-block) dimensions seen as different things (colour + shape != anything)

Garner Interference is when when two judgement calls are integral and there is cross talk.

Hypothesis, integral spaces are represented by conjointly tuned neurons. separables spcaces represented by independently tuned neurons.

### Multi-channel and norm based encoding models

* Multi-channel neural coding (aka uniform population code) ideally measured using adaptation. One clear example (Juang et al 2006) modulation of neural respoonse cencodes distance between stimuli.
* Norm based code (aka prototype representation). How far away from *average* face. More firing for more extreme example of stimulus. Can be measured by direct response. Caricature effect. Canonical examples by Loffner et al 2005, amplitude of neural response encodews distance from prototype.

Problem is both these methods are confounded in measurement. What it means to be centre of space means everything is more similar to you.
* Adaptation mistaken for norm based coding or vice versa.
* Can also be examined using ERP (Similarity effect)

Confounds can be measured using the carry-over designs.

### Analysis of data and experimental design
  * basis Sets, set of covariates that have property that a combination of such model variation of possible responses
    * One such basis set is HDR and first derivative. Model differneces in timing between expected and actual HDR
    * Basis Sets, impulses at time = 0,1,2,3,4... - FIR model (Finite Impulse Response, or shifted set of Dirac functions)
  * SOA (Stimulus Onset Asynchrony). Difference in timing for diff stimuli (rotated E vs vertical E), not different timing for different region.

## Perfusion fMRI

* Instead of oxygenated/deoxygenated blood flow. Tag protons inflowing to brain (in neck), and after delay readout effect of label in brain. Alternating images with/without tagging to get differences. Differencing removes intrinsic noise.
* very good therefore for measuring slow changes in neural signal.

## Sources of Noise

* Head motion
* Cardio-Pulmanary Fluctuations
* Distortion due to ferro-magnetic substance prescence
* Susceptibility artifact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

## Researcher Questions

* Adding a marker for side of head, neurological/radiological views of head orientation
* Power Analysis: neuropowertools.org To check for a study based on pilot data or similar. Neurovault.org to access previous study data and results.
* Noise from the scanner (gradient coils) interferes with auditory experiments
