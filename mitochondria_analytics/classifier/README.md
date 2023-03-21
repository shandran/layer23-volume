# Mitochondria Classifier for Pyramidal Neuron Compartment

# Summary Presentation
#### View a [summary presentation](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/Mitochondria_Classifier_by_Pyramidal_Neuron_Compartment.pdf) using mitochondria spatial metrics and machine learning classifiers to assign mitochondria by  compartment in pyramidal neurons. 

# Contents

---

## Random Forest Classifier 

[`Round1_analysis_of_unknown_dendritic_rfc_prediction_results.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/Round1_analysis_of_unknown_dendritic_rfc_prediction_results.ipynb): manually-verified performance of a random forest classifier. Does not include "with45cone" metric. Accuracy is 65%  

[`Round1_analysis_of_CLEAN125_WITHINCONE_unknown_dendritic_rfc_prediction_results.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/Round1_analysis_of_CLEAN125_WITHINCONE_unknown_dendritic_rfc_prediction_results.ipynb): manually-verified performance of a random forest classifier. Test the "clean125" set of pyramidal neurons (which does not alter accuracy), and does include classifier using the "with45cone" metric, which substantially improves the classifier accuracy to 71%.

[`Round1d_replicate_best_performing_rfc_from_scratch.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/Round1d_replicate_best_performing_rfc_from_scratch.ipynb): minimal code to create the best performing random forest classifier.

[`Round1d_replicate_best_performing_rfc_from_scratch_results.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/Round1d_replicate_best_performing_rfc_from_scratch_results.ipynb): calculating best-performance accuracy using the human-curated dataframe as "ground truth"" (see below) instead of train-test-split dataframe.

---

## Human-curated assignments for 'Unknown dendritic' compartment

[`human_curated_compare.csv`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/human_curated_compare.csv): dataframe with human-curated manual assignments for the Unknown dendritic assignment as reported in the Turner *et. al.,* Cell 2022 paper. Includes curator notes and Neuroglancer link for each entry. Compiled in Microsoft Excel and exported to csv format. This is used as the "ground truth" dataframe mentioned above.

[`unknown_dendritic_human_curated.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/classifier/unknown_dendritic_human_curated.ipynb): Jupyter notebook allowing you to explore the human-curated dataframe. Code is included that allows you to easily view these mitochondria in Neuroglancer.

---
