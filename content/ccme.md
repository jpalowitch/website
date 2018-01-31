---
title: Continuous Configuration Model Extraction (CCME)
---

<img src="http://stats.johnpalowitch.com/wp-content/uploads/2016/01/output_ccme_may2.png" style="max-width:50%;min-width:40px;float:right;" alt="Github repo" />

Here's a brief description of the community detection method CCME, introduced in [Significance-based community detection in weighted networks](https://arxiv.org/abs/1601.05630v4). The method identifies and refines communities in weighted networks using tests of statistical significance with respect to a null model. These significance tests are performed in iterative batches, with a multiple testing correction to ensure Type-I error control. The batches correspond to refinements of single communities, and refinements are performed independently so that each node has the potential to belong to multiple communities. Due to the significance tests, each node also has the potential to belong no communities. So, CCME will return “background” nodes along with communities, and sometimes no communities when no significant node subgroups exist.

The image above plots the results of applying CCME to the U.S. airport network. Airports covered by identical symbol-colors are in the same community. Some airports belong to multiple communities, and most belong to no communities (those are not given a symbol). Code for the method is [here](https://github.com/jpalowitch/CCME), and code for the analyses in the paper is [here](https://github.com/jpalowitch/CCME_analyses).