# Oil_Spill_Detection

# Problem Statement-:
Among the different types of marine pollution, oil spill is a major threat to the sea ecosystems. The sources of these spills can be traced back to the ships and mainland. Fuel oil sludge’s, engine room waste and foul bilge water produced by all type of ships, also end up in the sea.
Satellites equipped with SAR, can provide information on the presence of oil at sea. The presence of oil film on the sea surface damps the small capillary and short gravity waves and drastically reduces the Bragg scattering and therefore the measured backscattering energy, resulting in darker areas in SAR images. However, dark areas may be also caused by other phenomena, called ‘look-alikes’, such as organic film, grease ice, wind front areas, areas sheltered by land, rain cells, currents hear, internal waves and up-welling zones.
In this project our task will be to identify these dark regions and classify them as oil slicks or lookalikes, Image Processing is used to gather useful information from the image and then use this information as a input to either to a Neural Network or with an efficient Machine Learning algorithm to Study the oil spill.

# Methodology
a)The first step is to blur the image in order to reduce the noise (since SAR images are noisy). Toidentify the potential oil spill which is done by thresholding the image (may be with a fix value or via it’s mean & mode), this process clearly separates dark objects and whitens out the rest of the background. Finally contouring is applied and very small areas are removed, area and perimeter of the significant region is calculated.

b)These image based parameters along with shape based (yet to be evaluated) parameters make the   input parameters for the Neural Network. The ANN then trains itself for the given data via stochastic gradient descent (updates weights at every epoch). Finally training the dataset and analyzing the accuracy of the result.
