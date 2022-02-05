Biodiversity
======================

When analyzing metabarcoding data we are typically interested in the diversity within samples as well as the diversity between samples.

.. figure:: images/MA-tree.png

   Analyses methods you can choose from in MicrobiomeAnalyst.

.. admonition:: Question 17.

   | Based on what you learned in the lecture, discuss which method is appropriate to analyze the diversity within samples. 
   | And which one to compare the biodiversity between samples?

The following questions can be answered using the ``Try our examples``:``Mammalian gut`` data set.


:math:`\alpha`-diversity analysis
----------------------------------

Lets proceed with the ``Alpha diversity analyses``. 
Familiarize yourself with the different ``diversity measures`` by hoovering over the ``?``.
Apply the alpha diversity analyses at the species level using those measures that were also introduced in the lecture.

.. warning::

   MicrobiomeAnalyst does not have an option to test whether data is normally distributed.
   As you know from the course `Data verzamelen en analyseren`, using a parametric test, like an ANOVA, requires that your data (technically the residuals) are normally distributed. 
   Non-parametric tests like the Kruskall-Wallis test can also be used if the data is not normally distributed.
   Make sure you apply an appropriate test for all analyses.

.. figure:: images/MA-alpha-observed-diet.png
   :width: 400

   The observed species richness in the mamalian gut samples from the different diet groups. 
   Boxes represent the interquartile range (IQR) and the median. Whiskers represent 1.5x the IQR. Diamonds represent the mean. Kruskal-Wallis test: stat = 13.10, n = 36, p = 0.0014.

.. figure:: images/MA-alpha-shannon-diet.png
   :width: 400

   The species-level shannon diversity of the mamalian gut samples from the different diet groups.
   Boxes represent the interquartile range (IQR) and the median. Whiskers represent 1.5x the IQR. Diamonds represent the mean. Kruskal-Wallis test: stat = 3.81, n = 36, p = 0.1487.


.. admonition:: Question 18.

   | Discuss which ``statistical method`` to apply and why.
   | Comparing the observed richness and the Shannon index, discuss why their results differ with respect to the difference between omnivores and carnivores.
   | What other :math:`\alpha`-diversity measure, not implemented in MicrobiomeAnalyst, could provide further information?

Recall your hypotheses from question 3.

.. admonition:: Question 20.

   | How do your results relate to your hypotheses?
   | Discuss potential explanations why your results are different than expected.
   | Which of the two figures (sample-level or group-level) best demonstrated the differences between diets? Which figure would be most appropriate to include in your report/a scientific publication?


   
:math:`\beta`-diversity analysis
----------------------------------

Lets proceed with the ``Beta diversity analyses`` and perform the Principle Coordinate Analysis (PCoA).
Start with the Bray-Curtis index of the species abundances and the (non-parametric) PERMANOVA statistical test.

.. figure:: images/MA-beta-braycurtis.png
   :width: 600

   Principle coordinate plot of the differences in mammalian gut community composition between diet groups.
   Bray-Curtis distances based on the species abundances. PERMANOVA: F = 5.11, n = 36, p < 0.001.


Recall your hypotheses from question 3.

.. admonition:: Question 21.

   | Which Diet groups differ most strongly from each other?
   | Which Diet group is most variable across different samples?
   | How do your results relate to your hypotheses?
   | Discuss potential explanations why your results are different than expected.

Repeat the analyses but now using the Jaccard index.

.. figure:: images/MA-beta-jaccard.png
   :width: 600

   Principle coordinate plot of the differences in mammalian gut community composition between diet groups.
   Jaccard distances based on the species occurrences. PERMANOVA: F = 3.50, n = 36, p < 0.001.


.. admonition:: Question 22.

   | Based on what you learned in the lecture, discuss what the difference is between the Bray-Curtis distance and the Jaccard distance.
   | Does the PCoA plot based on the Jaccard index differ from the PCoA plot based on the Bray-Curtis index?
   | What biological interpretation can you draw based on this distinction or the lack thereof? 
   | Which of these two analyses better explains the variation in the data? Hint: note the PCoA axes.


      
