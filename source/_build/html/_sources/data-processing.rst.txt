Data filtering and normalization
=================================

The first step in metabarcoding (or any other kind of) analyses is to check your data.
The ``Text Summary`` and ``Library Size Overview`` tabs of the `Data Integrity Check` page give some important summary statistics.
These can help you decide on how to proceed with the analyses.

.. figure:: images/MA-libsize.png
   :width: 600

   Library size overview for the mammalian gut example data in MicrobiomeAnalyst. The library size is the number of reads per sample.

.. admonition:: Question 4.

   | Based on what you learned in the lecture about undersampling / sequencing depth, how do you evaluate these first results?
   | Discuss which summary statistics give information about undersampling.
   | Discuss what causes undersampling in metabarcoding data and why it could be a problem.
   | How can you deal with undersampling in metabarcoding analyses?

.. admonition:: Question 5.

   | Based on what you learned in the lecture about unequal sampling depth, how do you evaluate these first results?
   | Discuss which of these results give information about unequal sampling depth.
   | Discuss what causes unequal sampling depth in metabarcoding data and why it could be a problem. 
   | How can you deal with unequal sampling depth in metabarcoding analyses?

Lets ``>> Proceed``



Data Filtering
---------------------------------

Data filtering aims to remove low quality or uninformative features to improve downstream statistical analysis.
Features with very small counts in very few samples are more likely due to sequencing errors or low-level contaminations. Even if they are real, they carry little information compared to other features and the analysis will be more efficient without them, but the results will not be drastically different. Their removal is advised.

Let's look at the effect of removing rare features. 

First, use unfiltered data: Disable data filtering and ``Submit``.

.. figure:: images/MA-filter.png
   :width: 400

   Feature filtering settings to disable filtering in MicrobiomeAnalyst.

.. admonition:: Question 6.

   | How many features remain according to the results in the blue pop-up box?
   | Is this what you expect based on the results in the Data Integrity Check? Discuss why / why not.

Systematically change the ``minimum count`` filtering option (keep low variance filtering disabled, we will not focus on that in this course).

.. admonition:: Question 7.

   | What happens if you set the value too high?

Choose a data filtering setting and ``>> Proceed``. (The tutorial's figures are based on no filtering.)



Data Normalization
---------------------------------

The second important step in data preparation for metabarcoding analyses is data normalization.
Normalization removes biases due to, for instance, unequal sampling depth and thus allows us to directly compare the community composition of different samples.

Lets first disable data normalization, ``Submit``, ``>> Proceed`` and select ``Rarefaction Curve``.
This gives a set of rarefaction curves, where each curve represents a sample of the gut microbiome of one of the mammalian species.

.. figure:: images/MA-rarefactioncurve.png

   Rarefaction curves for the mammalian gut samples in MicrobiomeAnalyst (parameter settings: data source = filtered, steps = 20, group by = None).
 
The saturation (leveling off) of the rarefaction curve gives information on how well the species richness estimate based on the sample reflects the true species richness in the environment (here: the mammalian gut).
 
.. admonition:: Question 8.

   | Given the shape of the curves, do you think these samples captured the complete microbial community in the gut of each of these species? Why / Why not?

Especially when the rarefaction curves are not saturated, the sampling depth (sequence sample size) can have a major impact on the species richness estimate.

.. admonition:: Question 9.

   | Based on what you learned in the lecture, discuss what can cause unequal sampling depth.
   | Which sample has the higher species richness estimate, `Horse1` or `Chimp1`?
   | Which gut community is probably more species rich, that of `Horse1` or `Chimp1`?
   | What do you conclude about the comparability of these original samples?

One data normalization method that can remove biases due to unequal sampling depth is to rarefy upto the smallest sampling depth (i.e. the rarefaction depth).
For samples with a higher sampling depth, this means taking a random subsample of the reads (without replacement) up to the rarefaction depth.
 
Using the results of the ``Library Size Overview`` on the `Data Integrity Check` page and the rarefaction curve, mentally draw a line at the rarefaction depth.

.. admonition:: Question 10.

   | Discuss whether rarefying improves the comparability of the samples.
   | How does rarefying affect the accuracy of the species richness estimates? 

Because rarefying often results in the loss of a lot of data, it may be worth to consider excluding certain samples from the analyses rather than accepting a very low rarefaction depth.

.. admonition:: Question 11.

   | Given the ``Library Size Overview`` on the `Data Integrity Check` page, decide on the best strategy for sample filtering and normalization.

Now implement this strategy on 1) the ``sample filtering`` tab of the `Data filtering page` and 2) the `Data normalization` page.
``>> Proceed`` again to the ``Rarefaction curve``.

.. admonition:: Question 12.

   | Are you satisfied with the results?


