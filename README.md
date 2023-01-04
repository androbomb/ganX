# ganX - a python library to generate MA-XRF raw data out of RGB images

ganX (*generate artificially new XRF*) is a small library to generate Macro mapping X-ray fluorescence (MA-XRF) images out of an RGB input image, and a dictionary comprising pigments' RGBs and characteristic XRF signals.

To generate a synthetic MA-XRF data, it performs the following steps: 

1. Use an interative KNN unsupervised clustering on the RGB space to extract a set of RGB clusters, thus replacing the original RGB with a clustered RGB.
2. Starting from the clustered RGB, it associates a pigment (or a list of pigments) to the colour, by computing the distance of the cluster RGB to the pigments RGB in CIELAB colour space.
3. After that, it builds a distribution out of a weighted average of the pigments distribution found; this distribution is used to randomly generate the XRF signal via a Montecarlo simulation.

Additionaly, the library offers other classes and methods to explore the XRF dataset.

--------------

