# Reproduce figures
Data for reproducing the analysis of the manuscript and the figures are accessible freely online. Magnetospheric Multiscale (MMS) are available through the [MMS repository](https://lasp.colorado.edu/mms/sdc/public/). For the solar wind measurements, one can access the [OMNI dataset](https://themis.ssl.berkeley.edu/data\_products/index.php) repository, while for THEMIS/ARTEMIS data can also be accessed via their [Repository](https://themis.ssl.berkeley.edu/data\_products/index.php).

Below we give instructions on how to reproduce each figure and table of the analysis.

## General instructions

In the irfu-package there are examples of all the plots that are included in the manuscript with documentation and extensive descriptions.
MMS examples are located here: https://github.com/irfu/irfu-matlab/tree/master/plots/mms

In all the figures, the special notation was done by editing vector graphic files exported from MATLAB with Adobe Illustrator 2024. While the majority of the plots were made in MATLAB, similarly open access functions such as Python's [Matplotlib](https://matplotlib.org) can be used to generate the same figures with minor visual differences. Furthermore, by installing the [Pyspedas](https://github.com/spedas/pyspedas/) package that was used to download the data, the requirement packages to do all operations and plots in Python become also available.

More information regarding the derivation of each product that is plotted on all figures can be found in the Methods section of the article. The information below should be used complementary to the information found in the text regarding each neccesary derivation.

## Step-by-step instructions
### Figure 1

* Figure 1(a-h) consist of a typical timeseries ladder plot. For generating the pitch angle distribution we used the [mms_feeps_pad](https://github.com/spedas/pyspedas/blob/master/pyspedas/mms/feeps/mms_feeps_pad.py) function from [Pyspedas](https://github.com/spedas/pyspedas/). For the ion differential energy flux spectrum, the irf_spectrogram function of [irfu-matlab](https://github.com/irfu/irfu-matlab) was used. All tha panels and plots were made using irf_plot and irf_panel of [irfu-matlab](https://github.com/irfu/irfu-matlab). Figure 1(i-j) were generated using simple plot function of MATLAB.

### Figure 2

* Figure 2(a-h) were similarly made using irf_plot and irf_panel of [irfu-matlab](https://github.com/irfu/irfu-matlab). To do the wavelet analysis in order to analyze the wave observations, a filtering of the backgroun magnetic field was done using the irf_filt function [irfu-matlab](https://github.com/irfu/irfu-matlab) and the [irf_wavelet](https://github.com/irfu/irfu-matlab/blob/master/irf/irf_wavelet.m) function to generate the power spectra of the electric and magnetic field. To do the polarization analysis and determine the ellipticity and angle of propagation with respect to the magnetic field, [irf_ebsp](https://github.com/irfu/irfu-matlab/blob/master/irf/irf_ebsp.m) function is used. Figure 2 (i) was generated using simple plot function of MATLAB with the errorbars per data point being ploted through the [errorbar Matlab function](https://www.mathworks.com/help/matlab/ref/errorbar.html)

### Figure 3

* Figure 3 is also made in MATLAB, using [errorbar function](https://www.mathworks.com/help/matlab/ref/errorbar.html) along with [scatter](https://au.mathworks.com/help/matlab/ref/scatter.html) and [colormap](https://se.mathworks.com/help/matlab/ref/colormap.html). The function [text](https://www.mathworks.com/help/matlab/ref/text.html) is used to add the FEEPS energy channel for each event, while the second legend (top-right) was made by generating the same markers as in the plot and adding them via illustrator in vector graphic format.


### Figure 4

* Figure 4 was made mainly on Adobe Illustrator. For the embedded data that are shown regarding the upstream discontinuity associated seed population and the foreshock transient electrons, the irf_plot function from [irfu-matlab](https://github.com/irfu/irfu-matlab) was used. Information regarding how to access the background image used for the Sun are given in the caption of the figure.


### Figure 5
* Figure 8 is made using [SPEDAS](http://spedas.org/wiki/index.php?title=Downloads_and_Installation#Download_the_SPEDAS_executables,_Version_6.1_(May_2024)) standlone software. To generate the 2D slices distributions, the function  thm_ui_slice2d was used. Information on how to run it along with examples can be found on SPEDAS [website](http://spedas.org/wiki/index.php?title=THEMIS_Particle_Distribution_Slices).

### Figure 6
* Figure 9 was made in MATLAB using standard plot functions. In particular, to generate the meshgrid for the bow shock model, the function meshgrid from MATLAB is used with a resolution of 0.4 Re. [quiver3](https://www.mathworks.com/help/matlab/ref/quiver3.html) and plot3 were used to [plot](https://www.mathworks.com/help/matlab/ref/plot3.html) the direction of the discontinuities and the location of the ARTEMIS spacecraft respectively. More information regarding the parametrization of the bow shock model used can be found in the methods section.

### Figure S1
* Figure 5 consists of several spectrograms of the FEEPS high-energy electron populations made with the irf_spectrogram function of [irfu-matlab](https://github.com/irfu/irfu-matlab). The left plot (panel A) shows the raw data for all MMS spacecraft while on the right (panel B) one can see the cleaned version in which the removed data are ploted as NaN (Not a Number) values with hite background.

### Figure S2
* Figure 6 is made with the MATLAB [stackedplot function](https://www.mathworks.com/help/matlab/ref/stackedplot.html). Special indication (i.e., vertical lines) are made using the [annotation](https://www.mathworks.com/help/matlab/ref/annotation.html) function.

### Figure S3
* Figure 7 consist of a typical timeseries ladder plot. Similarly to Figures 1 and 2, for the ion and electron differential energy flux spectrum, the irf_spectrogram function of [irfu-matlab](https://github.com/irfu/irfu-matlab) was used. All tha panels and plots were made using irf_plot and irf_panel of [irfu-matlab](https://github.com/irfu/irfu-matlab). To generate the power spectra of the electric and magnetic field, for the polarization analysis and to determine the ellipticity and angle of propagation with respect to the magnetic field, [irf_ebsp](https://github.com/irfu/irfu-matlab/blob/master/irf/irf_ebsp.m) function is used.
* 
If more information are needed, the reader may contact the corresponding author. 
