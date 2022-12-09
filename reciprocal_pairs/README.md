# Reciprocal Pairs
Analysis of pairs of neurons (or partial neurons) that synapse onto one another

***

![a reciprocal pair of neurons that synapse onto one another](reciprocal_pair_top.png "reciprocal pair of neurons that synapse onto one another")

***

# Summary Presentation

### View the [Reciprocal Pairs](https://github.com/shandran/layer23-volume/blob/main/reciprocal_pairs/reciprocal_pairs_summary_presentation.pdf) summary presentation.

***

# Contents

## Notebooks and datatables

Use the [`list_of_all_reciprocal_pairs.ipynb` notebook]() to list and analyze all the reciprocal synapses in the volume. A special thank you to [Wanwen Zeng](https://github.com/wanwenzeng) at Stanford for generating the dictionary code to generate the reciprocal synapse list.  

Use the [`reciprocal_pairs_neurons_with_soma_in_volume.ipynb` notebook]() to list and analyze all the reciprocal pairs of neurons that have an identified soma within the Layer 2/3 volume.  

Use the [`reciprocal_pairs_synapse_visualizer.ipynb` notebook]() to generate 2D and 3D visualizations (using matplotlib, meshparty and vtk) of synapses for a desired set of reciprocal pairs. Includes over a dozen example pairs.  

The [`paired.csv` datatable](https://github.com/shandran/layer23-volume/blob/main/reciprocal_pairs/paired.csv) contains all the reciprocal pairs (n = 1998/2 = 999) in the entire volume, including all the partial processes as well.  

The [`pairs_rm_v_g_na.csv` datatable](https://github.com/shandran/layer23-volume/blob/main/reciprocal_pairs/pairs_rm_v_g_na.csv) contains the reciprocal pairs where both pairs have an identified soma in the volume, filtering out vascular and glial (because these are mis-segmented synapses anyway!), as well as filtering out the partial proceses. This was generated using the [`220309_cell_type_classification.csv` datatable](https://github.com/shandran/layer23-volume/blob/main/data/220309_cell_type_classification.csv). *Confession: due to my novice pandas skills, I found it more expedient to create the datatable in Excel using a simple vlookup function.*

## Visualization examples
