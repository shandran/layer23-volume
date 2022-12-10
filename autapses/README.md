# Autapses in the Layer 2/3 volume
Analysis and visualization of neurons that form a synapse onto itself

***

# Contents

## Notebooks and datatables

[`autapse_checker_entire_synapse_table.ipynb` notebook](https://github.com/shandran/layer23-volume/blob/main/autapses/autapse_checker_entire_synapse_table.ipynb): a simple method to identify potential autapses from the Layer 2/3 synapse table (pni_synapses_v185.csv).  

[`autapses_rm_nonneuronal.csv` datatable](https://github.com/shandran/layer23-volume/blob/main/autapses/autapses_rm_nonneuronal.csv): a human-curated (by me) data table that removed the vascular and glial cell ids. This resulted in a list of 27 potential neuronal autapses. The electron micrographs for each of these were manually checked in neuroglancer and 3 of the 24 were determined to be true autapses. The remaining 24 were due to segmentation errors or edge artifacts.  

[`` notebook](): analysis and visualization of the three true autapses as well as some example segmentation errors from the `autapses_rm_nonneuronal.csv` datatable.

***

## Visualization examples

### Autapse 3623767
In an inhibitory basket neuron (cell id 648518346349528994)

![inhibitory basket neuron autapse](autapse_cellid_648518346349528994.png "inhibitory basket neuron autapse")  

### Autapse 3966225
In an excitatory pyramidal neuron (cell id 648518346349538718)

![pyramidal neuron autapse](autapse_cellid_648518346349538718.png "pyramidal neuron autapse")  

### Autapse 5423743
In an excitatory pyramidal neuron (cell id 648518346349539853)

![pyramidal neuron autapse](autapse_cellid_648518346349539853.png "pyramidal neuron autapse")  

### Segmentation error examples


