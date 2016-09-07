# Outline
Inference
Fourier transform
Signal and noise
HRF and 1/f
Design and time
Perfusion

## Follow-ups

Types of experiments where exact knowledge of HRF important
	* Timing - activity in one part of brain happened before anotyher part of brain)
	* Dynamic Causal modelling

## Inference

Basic types of experimental designs
Claims about groups vastly different about a claim about an individual person.

#### Prototypical experiment

Brian Dougall had less of response to emotional faces, therefore psychopath (within the amygdala)
Fearful faces as *compared* to neutral faces.
For every point in the brain (univariate staittical test) compare signal from fearful face to neutral face
Set a threshold to only show points of difference above threshold
Smooth the data in space (done in raw data rather than processed) - improves statitical power
Show on anatomical data, digital reconstruction in 3D for display.
Each step is well justified statistically.

### To look at
Multi-voxel pattern analysis

## Takehomes - Protypical Exp

* Relative signal - within subjects relative change
* Indirect Measure - BOLD fMRI signal has no direct absolute interpretation - no units. Must be comapred between states. A control experiment to account for group differences in blood flow (drug use, age etc). Also an interrated measure so only detectable if there is a bulk change in neural activity, as opposed to change in pattern of firing.
* Bulk activity change
* Subtraction design
* Blocked order

Bonferroni correction (crude way), divide statistical value by number of voxels to reduce false positives. (Not using this comes up with results such as dead salmon showing activation)
Voodoo correlations - By chance a noisy brain has reasonable chance of correlating with separate likelihood (Handwashing vs response to pictures of sink)
Permutation approach for assessing significance of group differences in data.

##Inference

2 basic types of neuroimaging studies (and a third that combines the two).
* **Forward Inference** The brain area for "love". ie a brain area that corresponds to isolated behaviour. Isolate such behaviour by subtracting conditions (ie subtract images of friend from images of wife. Key problem is that all sorts of other things may be included in subtraction. A classic example is working memory - assumes pure insertion, that adding say working memory between perception and response does not change other aspects such as response execution. An alternative is parametric manipulation where the *amount* of cognitive process varies in each condition. Does not completely remove assumption of pure insertion. **Task vs cognitive operation** is a critical thing to think of when designing and evaluating experiments. Lesion inferences and imaging study are largely independent (remove part of brain does not necessarily mean cognitive process is removed).
* **Focal Reverse Inference Study** claims identify cognitive state from brain region activated. Key assumption is that particular region is only activated by one state. So pain activates a region, test every single other possibility stimuli???
* **Multi-voxel pattern analysis** - Step1: What is the difference in pattern across the brain or region for a particular state/stimulus. Step 2: Given a new statement/stimulus, use classifier from step 1 to decode somethin new. Key question is how well this generalises beyond a training set.

## Fourier Transform

* Any signal in time can be represented as a power spectrum using Fourier transform
* Blocked and evet-related designs. HRF favors designs with power at low temporal freqs. Changes in signal < about 4 seconds basically undetectable in fMRI signal.
* However intrinsic noise at low frequencies is high.
* Balancing noise and HRF has a optimal point of ~ 20 seconds.
* Tradeoffs between estimation efficiency and detection power. For some experiments we need stimuli to be randomised - but this is challenging. So event related designs are less statistically powerful.

## Perfusion fMRI

* Instead of oxygenated/deoxygenated blood flow. Tag protons inflowing to brain (in neck), and after delay readout effect of label in brain. Alternating images with/without tagging to get differences. Differencing removes intrinsic noise.
* very good therefore for measuring slow changes in neural signal.
