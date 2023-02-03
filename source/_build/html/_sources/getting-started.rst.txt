
Getting started
=================================

This tutorial will guide you through the analyses, visualization and interpretation of metabarcoding data.
Once you have finished this tutorial and have met the objectives, you are ready for the module assignment. 
During the assignment, you will work in teams of two to analyze the composition and diversity of environmental microbiomes and present your results in a report.
More information on the assignments can be found `on canvas <https://canvas.uva.nl/courses/35953>`_.


Objectives
--------------------------------


By the end of this practical you should be able to:

- Describe the scientific context and experimental design of a metabarcoding study.

- Formulate metabarcoding research questions and hypotheses.

- Apply data filtering and normalization and justify the choice of methods.

- Characterize and interpret microbial community composition and justify the choice of methods.

- Compare the microbial diversity within and between samples and justify the choice of methods.

- Conduct metabarcoding analyses in a way that results are reproducible.
 
- Evaluate how metabarcoding results relate to the research questions and hypotheses.

- Discuss metabarcoding results in a scientific context.



Experimental design
----------------------------------

All analyses are performed in `MicrobiomeAnalyst <https://www.microbiomeanalyst.ca>`_ (group A)
or `MicrobiomeAnalyst mirror <https://dev.microbiomeanalyst.ca>`_ (group B).

When you navigate to MicrobiomeAnalyst you have a choice of six different modules.

.. figure:: images/MA-startscreen.png
   :width: 600

   Six options on the start page of MicrobiomeAnalyst

.. admonition:: Question 1.

   Judging by their brief description in the colored boxes, which module would you use for metabarcoding analyses?
   Discuss the differences in the experimental design and sequencing strategy of Marker Data Profiling and Shotgun Data Profiling.

Select the appropriate module.

Explore what the three mandatory data files should look like by hoovering over the ``?``.
You will notice that none of these files contain actual sequencing data, because the conversion of raw sequencing data into abundance tables and taxonomic classifications was already done for you.

.. figure:: images/MA-dataupload.png
   :width: 400

   Data upload page of microbiome analyst. The three mandatory files are the OTU/ASV table, the metadata file and the taxonomy table.
   For the assignment you will upload your data here. For the tutorial, you will use the example data in the ``Try our examples`` tab.

.. admonition:: Question 2.

   | Discuss the content of these files based on what you learned in the lecture. 
   | How is the OTU/ASV table generated from amplicon sequences?
   | How are these sequences taxonomically classified?
   | Which treatment or conditions can be compared for this example?

During the assignments you will upload your own data here, but for the tutorial we will use the example data sets.
Under ``Try our examples``, select ``Mammalian Gut``.

.. figure:: images/MA-mammaliangut.png

   Example data of the mammalian gut microbiome in MicrobiomeAnalyst, including a brief description.

.. admonition:: Question 3.

   | Based on the brief description, what is the sampling design of this study?
   | What could be your research questions on the community composition and diversity within and between diet groups?  
   | Discuss potential hypotheses with respect to the differences between the three groups.


.. important:: 

   Make sure you record all methodological details needed to reproduce your results. 
   This is good scientific practice and a therefore a grading criteria in the assessment of your report.
   In addition, MicrobiomeAnalyst can time out, which requires that you restart the session and thus replicate exactly what you did before. 

.. note::

   In this tutorial, options you can select in MicrobiomeAnalyst are indicated in ``this`` type set.

