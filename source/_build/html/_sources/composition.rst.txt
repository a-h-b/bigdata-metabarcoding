Community composition
================================

The next step in the analyses of microbial communities is to visualize the community composition.
In this part of the tutorial you will learn how to plot and interpret microbiome data - it is still based on the ``Try our examples``: ``Mammalian gut`` data set.

If the following are not current settings, select the data, disable data filtering and normalization. Then ``>> Proceed`` to ``Stacked bar/area plot``.


Absolute abundances
--------------------------------

Plot the absolute abundances of the phyla present in the mammalian gut samples.

.. figure:: images/MA-barplot-aa.png
   :width: 800

   Absolute abundances of the phyla present in the mammalian gut samples grouped by diet type.

.. admonition:: Question 13.

   | Apart from the differences between the three diet groups, what are the most striking differences between samples?
   | Discuss what, if any, is your biological interpretation of these differences.
   | Hint: Discuss which sample contains most Firmicutes bacteria, `BighornW3` or `Saki`?
   | Hint: Discuss which gut microbiome probably contains more Firmucutes bacteria, `BighornW3` or `Saki`?

Relative abundances
--------------------------------

Now plot the relative abundances of the phyla present in the mammalian gut samples and compare the barplots of the absolute and relative abundances.

.. admonition:: Question 14.

   | Given what you learned in the lecture about the differences of library size / sequencing depth in metabarcoding data, which plot gives a better representation of the community composition of the mammalian gut?
   | Can you think of another way to normalize the abundances across samples? Hint: see question 10 and 11.

Apply this normalization and compare the three diet groups.

.. admonition:: Question 15.

   | What are the most striking differences in the community composition between the diet groups? (just highlight a few).
   | Discuss which diet group probably has the highest evenness at phylum level? (we will come back to this later this later)

Compare the View options ``Organize samples by Diet`` and ``Merge samples to groups Diet``.

.. figure:: images/MA-rabund-unstacked.png
   :width: 800

   Relative abundances of the phyla present in the mammalian gut samples organized by diet type.

.. figure:: images/MA-rabund-stacked.png
   :width: 800

   Relative abundances of the phyla present in the mammalian gut samples merged by diet type.

.. admonition:: Question 16.

   | Which plot more clearly demonstrates the differences between diet groups?
   | Do you think this plot is a fair representation of the true variation between samples? Hint: discuss whether Tenericutes bacteria are generally more abundant in omnivores than in the other diet groups? 
   | Which of these two plots is most essential to include in your report / a scientific publication?
   


