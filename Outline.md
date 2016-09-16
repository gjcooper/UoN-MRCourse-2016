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
* BOLD is slow, averaged out response compared to neuron spikes
* Impulse Response Function measured to input in linear system means from measurement can calculate input to system
* In BOLD fMRI this IRF is called the hemodynamic response function (HRF)
* Different people/populations can have different HRF
* A point of neural activity evokes a blood flow response about 3mm wide
* Different regions/different drugs/hormonal state etc can affect HRF
* 3-4 seconds time resolution
* 3mm spatial resolution
* These are fundamental limitations of BOLD fMRI, and are biological/physical limitations (blood flow is slow and broad) rather than scanner limitations

## Sources of Noise

* Head motion
* Cardio-Pulmanary Fluctuations
* Distortion due to ferro-magnetic substance prescence
* Susceptibility artifact - distortion due to air/fluid/flesh boundaries (sinuses, ear canals - important for auditory lobes)

## Researcher Questions

* Adding a marker for side of head, neurological/radiological views of head orientation
* Power Analysis: neuropowertools.org To check for a study based on pilot data or similar. Neurovault.org to access previous study data and results.
* Noise from the scanner (gradient coils) interferes with auditory experiments
