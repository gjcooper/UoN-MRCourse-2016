name: centred
layout: true
class: center, middle, inverse
---
# fMRI
---
## Who Am I

### GAVIN COOPER

Research Academic with the CBMHR at UoN

Been working with MRI data for > 10 years

---
## Outline
### BOLD fMRI
### Limitations and Considerations
### fMRI Paradigms
### Complimentary sequences and clinical uses
---
layout: true
name: columns
class: inverse, middle
---
.left-column[
## BOLD fMRI
]
.right-column[
### The physics

T2\* relaxation is used in functional MRI. It is a measure of the component that does not re-phase after a 180 degree RF pulse.

.center[<img src="resources/rotateproton.gif" width=500, height=400>]
.center[.imlabel[Proton rotating in magnetic field]]
]
???
* Protons rotate on their axis in the magnetic field.
---
.left-column[
## BOLD fMRI
]
.right-column[
### The physics

T2\* relaxation is used in functional MRI. It is a measure of the component that does not re-phase after a 180 degree RF pulse.

.center[<img src="resources/rf90.gif" width=500, height=400>]
.center[.imlabel[T2 relaxation]]
]
???
* First 90 degree RF pulse puts all proton spins in phase.
---
.left-column[
## BOLD fMRI
]
.right-column[
### The physics

T2\* relaxation is used in functional MRI. It is a measure of the component that does not re-phase after a 180 degree RF pulse.

.center[<img src="resources/rf180.gif" width=500, height=400>]
.center[.imlabel[T2\* relaxation]]
]
???
* As they de-phase (relax) they are hit with a second RF pulse at 180 degrees.
* This flips the fields over and causes them to begin to re-phase.
* The portion that does not re-phase due to microscopic distortions of the magnetic field creates our T2\* signal
---
.left-column[
## BOLD fMRI
]
.right-column[
### The biology

* One source of these microscopic distortions is blood, which gives gives us BOLD fMRI.
* The BOLD response is due to oxygen attached to haemoglobin.
* The brain efficiently delivers oxygenated blood to parts of the brain with a higher energy budget (i.e. activity)
* This quickly results in blood vessels increasing in size.

.center[<img src="resources/arteries.png" width=353, height=325>]
.center[.imlabel[A view of the main arteries from below the brain]]
]

???

* Blood Oxygenation Level Dependent
* Oxygenated and de-oxygenated haemoglobin have different magnetic properties.
* So we have:
  * Activity (Neurons Spiking)
  * Increased blood vessel size
  * More de-oxygenated haemoglobin
  * Change in magnetic local properties as measured by T2\*
  * Image
---
.left-column[
## BOLD fMRI
]
.right-column[
### The HRF

* The transforms that take us from brain activity to an image create an approximately linear system.
* If we measure the output from a linear system when we introduce a brief large signal we can calculate an IRF.
* For a known IRF, give a pattern of output we can determine the input that produced it.
* In BOLD fMRI this IRF is called the hemodynamic response function (HRF).

.center[<img src="resources/hrf.png" width=315, height=325>]
.center[.imlabel[The canonical HRF]]
]
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.

* Different populations can have different HRF's.
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.

* Different populations can have different HRF's.

* Different regions in the brain can have different HRF's
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.

* Different populations can have different HRF's.

* Different regions in the brain can have different HRF's

* Some drugs can affect the HRF
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.

* Different populations can have different HRF's.

* Different regions in the brain can have different HRF's

* Some drugs can affect the HRF

* Hormonal state can affect the HRF
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the HRF)

* Different people can have different HRF's.

* Different populations can have different HRF's.

* Different regions in the brain can have different HRF's

* Some drugs can affect the HRF

* Hormonal state can affect the HRF

* ...
]
???
* Differences are often subtle.

* Have to be careful with claims about an individuals person

* Have to do everything possible to match populations with appropriate controls.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Limitations (the BOLD response)

* BOLD is a slow averaged out response compared to neuron spikes. 3-4 seconds of time resolution.

* A point of neural activity in the brain evokes a blood flow response about 3mm wide.

* These are fundamental limitations of BOLD fMRI and are biological in nature rather than scanner limitations.

]
???
* 3-4 second time resolution
* ~3mm spatial resolution

---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear

* Many sources of noise:
  * Head motion
  * Cardiopulmonary Fluctuations
  * Distortion due to ferro-magnetic substance presence
  * Susceptibility artefact
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear

* Many sources of noise:
  * Head motion
  * Cardiopulmonary Fluctuations
  * Distortion due to ferro-magnetic substance presence
  * Susceptibility artefact

* BOLD is an **indirect** measure and has no direct interpretation or units.
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear

* Many sources of noise:
  * Head motion
  * Cardiopulmonary Fluctuations
  * Distortion due to ferro-magnetic substance presence
  * Susceptibility artefact

* BOLD is an **indirect** measure and has no direct interpretation or units.

* BOLD is also an integrated measure, so it is only detectable if there is a bulk change in neural activity.
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear

* Many sources of noise:
  * Head motion
  * Cardiopulmonary Fluctuations
  * Distortion due to ferro-magnetic substance presence
  * Susceptibility artefact

* BOLD is an **indirect** measure and has no direct interpretation or units.

* BOLD is also an integrated measure, so it is only detectable if there is a bulk change in neural activity.

* fMRI scanner paradigms are noisy and care needs to be taken with auditory based studies.
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
]
.right-column[
### Other considerations

* The relationship between stimulation of the participant and brain activity is non-linear

* Many sources of noise:
  * Head motion
  * Cardiopulmonary Fluctuations
  * Distortion due to ferro-magnetic substance presence
  * Susceptibility artefact

* BOLD is an **indirect** measure and has no direct interpretation or units.

* BOLD is also an integrated measure, so it is only detectable if there is a bulk change in neural activity.

* fMRI scanner paradigms are noisy and care needs to be taken with auditory based studies.

* Hardware for MR room needs to be specially designed and is often expensive.
]
???
* Twice as many words does not -> twice as much brain activation

* Susceptibility artefact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

* BOLD is a relative signal and must be compared between states.

* It is possible to work on a shoestring though. First visual system I used was a std projector outside the MRI room through the window onto a screen made of PVC pipe and large sheet tracing paper.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Types of Neuroimaging Studies

#### Forward Inference

* The brain area that corresponds to an isolated behaviour

* Isolate the behaviour by subtracting conditions.

* Key problem is that all sorts of other things may be included in the subtraction.

* An alternative is parametric manipulation.

]
???

* i.e. Brain area for angry faces

* Subtract images of neutral face from images of angry face

* A classic example is working memory, which assumes pure insertion. That is that the addition of a working memory component to a task between perception and response does not change other aspects such as response execution.

* Parametric manipulation where the amount of cognitive process varies in each condition. But this does not completely remove the assumption of pure insertion.

---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Types of Neuroimaging Studies

#### Reverse Inference

* Claims to identify cognitive state from an activated brain region.

* Key assumption is that a particular region is only activated by one state.
]
???

* Participant is feeling pain as this region lights up

* Test every other single possible stimuli?
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Types of Neuroimaging Studies

#### Reverse Inference

* Claims to identify cognitive state from an activated brain region.

* Key assumption is that a particular region is only activated by one state.

#### Multi-voxel pattern analysis

1. What is the difference in pattern across the brain or a region for a particular stimulus.
2. Given a new stimulus use the classifier from Step 1 to decode something new.

* Key question is how well this generalises beyond the training set.
]
???

* Participant is feeling pain as this region lights up

* Test every other single possible stimuli?

* Multi-level is both forward + reverse combined

* Train participant on pictures of dogs and cats

* Show them new pictures and based on brain pattern determine what they are looking at.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Experimental Designs

#### Block Designs

* The HRF favours designs with power at low temporal frequencies.
* However intrinsic noise at low frequencies is high.
* Balancing noise and HRF has an optimal point of ~ 20 seconds.
* This gives us a block design

.center[<img src="resources/block.png" height=300>]
.center[.imlabel[An event-related design]]
]
???
* Changes in signal < about 4 seconds are basically undetectable in fMRI signal
* Block design is optimal in terms of signal to noise ratio.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Experimental Designs

#### Event-related Designs

* Some experimental question do not lend themselves to a block related design, especially those that need some randomisation
* Timing between stimuli would ideally be varied. If this is not possible because of the research question then the timing should be different to TR so that events are out of phase with scans.

.center[<img src="resources/event-related.png" width=450, height=300>]
.center[.imlabel[A traditional block design]]
]
???
* MMN as an example of suited to event-design and not possible to have varying SOA.
* Rare events can be measured.
* More trials are needed as MR signal is small.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Experimental Designs

#### 3 Types of measures

* BOLD fMRI amplitude - **Average direct effect of stimulus**
* **Distributed Pattern Analysis**
* **Within voxel adaptation**

.center[<img src="resources/carry-measures.png" width=534, height=300>]
.center[.imlabel[The three types of measures]]
]
???
* Increase of amplitude in relation to contrast, particular object/stimulus
* Patterns of voxel activation within group correlated, but between groups not correlated. Pattern of direct effects across voxels (not average)
* Neurons have reduced response to repetition of stimulus. Neural adaptation studies, looking at modulatory effect of one stimulus on the next.
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
]
.right-column[
### Experimental Designs

#### Carry over designs

* Both block and naive event-related designs only show direct effects of a stimulus.

* Continuous carry-over designs offer a method to simultaneously and efficiently measure within-voxel adaptation effects and across voxel distributed pattern responses.

* The neural response to a stimulus @ time = sum of mean response, direct effect and influence of prior stimuli
]
???
* Direct effect corresponds to distributed pattern analysis and influence of prior stimulus is within voxel neural adaptation

* Types of modulatory effects:
  * Neural adaptation, linear adaptation, has property that it's symmetric (A colour that is one shade darker effects brain same way as one shade lighter.)
  * Bias effects, asymmetric (Influence of neutral face in subsequent angry face is different to the effect of an angry face on a subsequent neutral face)
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
## Complimentary sequences and clinical uses
]
.right-column[
### Complimentary Sequences and Technologies

* T1, high resolution structural

* DTI, fMRI can be used to assist with DTI analysis

* EEG can be acquired to increase time resolution

* Plus eyetracking, physiological measures, transcranial magnetic stimulation and more
]
???
* Structural image enables you to overlay results on high resolution image to more easily locate regions activated by the task. It also makes normalisation between subjects much more accurate.

* DIFFUSION TENSOR IMAGING - Tractography seed regions can be created in a subject specific way using the results of fMRI data analysis.

* Electroencephalogram can be either acquired separately (harder to correlate data) or silmultaneously (noise from MR in EEG and vice versa)
---
.left-column[
## BOLD fMRI
## Limitations and Considerations
## fMRI Paradigms
## Complimentary sequences and clinical uses
]
.right-column[
### Clinical Uses

* The primary use in a clinical setting is to help assess how risky a particular brain surgery may be.

* Idea is to map the brain for critical functions like verbal, motor , sensory and executive function.

* Assessment of the effects of stroke, tumors etc can also be performed.

]
???
---
template: centred
## Final Discussion

.uncentre[
* Other fMRI techniques and paradigms exist such as Perfusion fMRI and resting state fMRI.
]
???
* Perfusion fMRI - Instead of oxygenated/deoxygenated blood flow. Tag protons inflowing to brain (in neck), and after delay readout effect of label in brain. Alternating images with/without tagging to get differences. Differencing removes intrinsic noise. Very good at measuring slow changes in neural signal.

* Resting State fMRI - Used to look at regional interactions in the brain when the subject is not performing an explicit task. Particularly sensitive to physiological noise. 
---
template: centred
## Final Discussion

.uncentre[
* Other fMRI techniques and paradigms exist such as Perfusion fMRI and resting state fMRI.

* Things the radiographer can do for researchers
]
???
* Know the capabilities of the scanner you are operating, what is possible and what is not.

* Scanner with larger gradient coil strengths that can change configuration quickly are best for fMRI

* Adding a marker for side of head, neurological/radiological views of head orientation. Will help the researcher validate file conversion steps later on in analysis.

* Keep researchers in the loop for any high priority clinical cases that take precedence.
---
template: centred
## Final Discussion

.uncentre[
* Other fMRI techniques and paradigms exist such as Perfusion fMRI and resting state fMRI.

* Things the radiographer can do for researchers

* Things researchers can do for radiographers.
]
???
* Have a clear idea of what you want to achieve with your sequence, but involve the radiographers early in the piece so that you aer working with the capabilities of the scanner.

* Have participants arrive with plenty of time and if possible backup plans for no-shows.

* Test, retest and test again any other equipment or software that will be needed to ensure a minimum of interruptions and delays.
---
template: centred
## Thank You

.uncentre[
You can find me @ ...

* www.gavincooper.net

* @GavinJCooper on twitter

* https://github.com/gjcooper

]
