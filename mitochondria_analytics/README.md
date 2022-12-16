# Mitochondria analytics
Visualization and analysis tools for analyzing mitochondria in the Layer 2/3 EM volume

![visualize all mitochondria in a cell of interest](ng_linkgenerator_astrocyte.png "visualize all mitochondria in a cell of interest")

***

# Contents

## Visualization tools

### Visualize a single mitochondrion of interest

[`neuroglancer_link_generator_mitochondria_visualization_version.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/neuroglancer_link_generator_mitochondria_visualization_version.ipynb): generate a Neuroglancer link for a single cellid and single mitochondrion from the `pni_mito_cellswskel_v185_fullstats.csv` datatable. The view will be centered at the centroid of the mitochondrion in the volume.

![neuroglancer link to a single mitochondrion with crosshair at the mito centroid](ng_linkgenerator_centroid.png "neuroglancer link to a single mitochondrion with crosshair at the mito centroid")

***

### Visualize all the mitochondria in a cell of interest

[`neuroglancer_link_generator_all_mitochondria.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/neuroglancer_link_generator_all_mitochondria.ipynb): generate a Neuroglancer link for all the mitochondria in a single cellid of interest pulling the mito ids from the `211019_mitochondria_info.csv` datatable.

![neuroglancer link generator for all mitochondria in a cell](ng_linkgenerator_jupyter.png "neuroglancer link generator for all mitochondria in a cell")

***

