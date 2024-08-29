# Reinforced Shock Acceleration for Relativistic Electrons - Injection Threshold
In this repository we provide instructions and the code that allow the reproduction of the results found in the manuscript "*Revealing an Unexpectedly Low Electron Injection Threshold via Reinforced Shock Acceleration*" Under Review in Nature Communications journal.

[![Publication: Under Review](https://img.shields.io/badge/Publication-Under_Review-orange?style=flat&logo=openaccess)](/README.md)

### Cite as 
*TBD*

### Corresponding Author
[![Savvas Raptis: 0000-0002-4381-3197](https://img.shields.io/badge/Savvas%20Raptis-0000--0002--4381--3197-green?style=flat&logo=orcid)](https://orcid.org/0000-0002-4381-3197)

## Repository Content
* [`code`](./code): Contains the Pyspedas and IRFU-matlab packages that were used to downloade and process the data respectively. The zipped files contain the version of the library that were used to generate the latest figure and analysis shown in the manuscript.

* [`figures`](./figures): Contains a step-by-step guide on how to fully reproduce the figures of the work. Figures will be uploaded after the publication of the manuscript. 

## Extra information

For fully reproducing the figures the irfu-matlab library can be used, available at [irfu-matlab](https://github.com/irfu/irfu-matlab). After adding the library to MATLAB's path one needs to run:

```matlab
irf
```
At the time of the latest submission of the article, the following software versions and OS were used:

* irfu-matlab version:  v1.16.3 (devel branch)
* Pyspedas version: 1.3 - Python Version  3.11.2
* Spedas version: 6.1 (standalone software)
* Adobe Illustrator 2024  (standalone software)
* MATLAB version: R2023a
* OS: Apple M2 Max Sonoma 14.5
