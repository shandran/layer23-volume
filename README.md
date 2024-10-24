# layer23-volume
Reconstructions and analyses from the IARPA [MICrONS consortium](https://www.iarpa.gov/research-programs/microns) mouse cortex Layer 2/3 serial EM volume.

**Attribution:** https://www.microns-explorer.org/terms-and-conditions<br>
**Citation:** https://www.microns-explorer.org/citation-policy<br>

***

### Over a century ago, Golgi and Cajal revolutionized the field of neuroscience

For an intriguing summary of this revolution, read Mitch Glickstein's [**essay**](https://www.cell.com/current-biology/pdf/S0960-9822(06)01203-6.pdf) on Golgi and Cajal in <em>Current Biology</em>.

![Pyramidal neuron of the mouse cortex stained using the Golgi method](img/golgistain.png "Serial LM reconstruction of Golgi stained neuron")


<em>Image credit: I created this serial LM reconstruction of a Golgi-stained mouse pyramidal neuron using a Zeiss Photomicroscope II at 40x oil and Smart Objects in Photoshop.</em>

### Once again neuroscience is undergoing another revolution with the serial electron microscope brain reconstructions

Petabytes of data have been generated for small volumes (1 cubic mm or less) of human, mouse, songbird, and fly brain volumes. This gargantuan task has been spearheaded by investigators from a variety of entities, including Allen Institute, Baylor, Columbia, Google Research, Harvard, IARPA, Janelia/HHMI, Johns Hopkins, Max Planck Institute, Princeton, Rice, and the University of Cambridge, among others.  

![Pyramdial neuron from the Layer 2/3 serial EM volume](img/layer23pyr.png "Serial EM reconstruction using Neuroglancer")


<em>Image credit, I created this reconstruction using Neuroglancer of pyramidal neuron with cellid 648518346349538440 in the Layer 2/3 volume.</em>  

***

# Contents
This github repo focuses on visualization and analyses of the Layer 2/3 EM volume data generated in the IARPA Microns consortium (Allen Institute, Baylor, Princeton). The volume can be viewed in Neuroglancer (developed at Google Research). Allen Institute and the Seung lab at Princeton have posted datasets, resources, analysis tools, and more on their respective github repos, and also at the Allen Brain Map website. 

## Look up and visualization tools

Use [`lookup_cellid_in_layer23_volume_neuroglancer.ipynb`](https://github.com/shandran/layer23-volume/blob/main/lookup_cellid_in_layer23_volume_neuroglancer.ipynb) to identify the cell subtype for a given cellid in the Layer 2/3 volume. This is a human-curated list for cells that contain all (or most) of the cell soma within the volume. Includes a Neuroglancer link generator. See also a version that adds the Neuroglancer nucleus id (for cells with a nucleus in the volume): [`lookup_cellid_in_layer23_volume_neuroglancer_with_nucleus_id.ipynb`](https://github.com/shandran/layer23-volume/blob/main/lookup_cellid_in_layer23_volume_neuroglancer_with_nucleus_id.ipynb).

Use [`list_of_cell_subtypes_in_layer23_volume.ipynb`](https://github.com/shandran/layer23-volume/blob/main/list_of_cell_subtypes_in_layer23_volume.ipynb) to view the cellids categorized by cell subtype, from a curated list of 619 cellids.

Use [`lookup_mitochondria_ids.ipynb`](https://github.com/shandran/layer23-volume/blob/main/lookup_mitochondria_ids.ipynb) to look up mitochondria ids by cellid. Useful for creating a list of mito ids for visualization in neuroglancer and for analyzing voxel data.

Use [`neuroglancer_link_generator_mitochondria_visualization_version.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/neuroglancer_link_generator_mitochondria_visualization_version.ipynb) to generate a Neuroglancer link for a single cellid and single mitochondrion from the `pni_mito_cellswskel_v185_fullstats.csv` datatable.

Use [`neuroglancer_link_generator_all_mitochondria.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/neuroglancer_link_generator_all_mitochondria.ipynb) to generate a Neuroglancer link for all the mitochondria in a single cellid of interest pulling the mito ids from the `211019_mitochondria_info.csv` datatable.

Use [`vtk_mitochondria_visualizer.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/vtk_mitochondria_visualizer.ipynb) to generate a 3D interactive view of all mitochondria in a cell of interest. Note this method has significant file download and space requirements compared to using the Neuroglancer viewer. Use [`vtk_mitochondria_visualizer_with_synapses.ipynb`](https://github.com/shandran/layer23-volume/blob/main/mitochondria_analytics/vtk_mitochondria_visualizer_with_synapses.ipynb) to add the pre- and post-synaptic sites to the visualization as well. 

Use [`lookup_synapse_ids.ipynb`](https://github.com/shandran/layer23-volume/blob/main/lookup_synapse_ids.ipynb) to look up synapse ids by pre- and post-synaptic cell ids. Also contains voxel data.

Use [`synapse_visualizer.ipynb`](https://github.com/shandran/layer23-volume/blob/main/synapse_visualizer.ipynb) to create a 2D and 3D visualization of all pre- and post-synaptic sites on a cell of interest.

[`synapse_visualizer_plotly.ipynb`](https://github.com/shandran/layer23-volume/blob/main/synapse_visualizer_plotly.ipynb) is an updated synapse visualizer with interactive 2d and 3d plotly scatterplots added.

Use [`vtk_nuclei_visualizer_with_vasculature.ipynb`](https://github.com/shandran/layer23-volume/blob/main/vtk_nuclei_visualizer_with_vasculature.ipynb) to create an interactive 3D visualize the cell nuclei in the volume using vtk and OpenGL. Includes a visualization option to include all vasculature in the volume. 

Use [`layer23_cell_proximity_calculator.ipynb`](https://github.com/shandran/layer23-volume/blob/main/layer23_cell_proximity_calculator.ipynb) to enter a cell id of interest and make of list of nearest cells, using a simple centroid-to-centroid Euclidean distance calculation.

## Interesting features in the Layer 2/3 volume

### Axon-carrying dendrite
[`axon_carrying_dendrite` folder](https://github.com/shandran/layer23-volume/tree/main/axon_carrying_dendrite): a partial neuron (soma is not in the volume) with a possible axon-carrying dendrite.

![axon-carrying dendrite](axon_carrying_dendrite/axon-carrying-dendrite-synapse_sites.png "axon-carrying dendrite")

### Autapses
[`autapses` folder](https://github.com/shandran/layer23-volume/tree/main/autapses): there are three autapses in the Layer 2/3 volume and many (24) cases of segmenation errors that are not true autapses.

![inhibitory basket neuron autapse](autapses/autapse_cellid_648518346349528994.png "inhibitory basket neuron autapse") 

### Mitocondria visualizations
[`mitochondria` folder](https://github.com/shandran/layer23-volume/tree/main/mitochondria): analysis of interesting mitochondrial features in the layer 2/3 volume, including the largest contiguous mitochondrion in an astrocyte, and the largest number of mitochondria by count in an inhibitory basket neuron.

[`decimated meshes` folder](https://github.com/shandran/layer23-volume/tree/main/decimated_meshs): notebooks and vtk visualizations using pyvista mesh decimation to reduce the size of the cell body and mitochondria mesh files.Modified from Tyler Sloan's() [mesh decimation pipeline](https://github.com/Quorumetrix/Blender_scripts/blob/main/Mesh%20Decimation%20Pipeline.ipynb). 

![All astrocyte mitochondria with vasculature](decimated_meshs/all_astro_mito_with_vasc_2024_08_01_1950_40.png "all astrocyte mitochondria with vasculature")

![large contiguous mitochondria in an astrocyte](mitochondria/astrocyte_mitos.png "large contiguous mitochondria in an astrocyte")

[`astrocyte mitochondria` folder](https://github.com/shandran/layer23-volume/tree/main/astrocyte_mitochondria): analytical and visualization notebooks and high resolution 3D renderings of astrocyte mitochondria.

![3D rendering of astrocyte mitochondria colored with a voxel size threshold](astrocyte_mitochondria/648518346349527319_web.png "3D rendering of astrocyte mitochondria colored with a voxel size threshold")

[`astrocyte mitochondria inclusions` folder](https://github.com/shandran/layer23-volume/tree/main/astrocyte_mitochondria_inclusions): visualization notebooks for generating electron micrograph (EM) images and high resolution 3D renderings of mitochondria inclusions in astrocytes of the Layer 2/3 volume.

![inclusion in mitochondria 2528399 of astrocyte 648518346349538089 of the Layer 2/3 EM volume](astrocyte_mitochondria_inclusions/cid_648518346349538089_mid_2528399_100dpi_mitoseg_slice_13_512.jpg "inclusion in mitochondria 2528399 of astrocyte 648518346349538089 of the Layer 2/3 EM volume")

### Mitochondria analysis and classification
[`mitochondria analytics` folder](https://github.com/shandran/layer23-volume/tree/main/mitochondria_analytics): more in-depth analysis of the structural, spatial, and positional characteristics of mitochondria in the Layer 2/3 volume.

![3D interactive visualization of all mitochondria and synapses in a neuron](mitochondria_analytics/3dvtk_mito_synapses.png "3D interactive visualization of all mitochondria and synapses in a neuron")

### Two neurons with the most synapses in the Layer 2/3 volume
[`most_synapses` folder](https://github.com/shandran/layer23-volume/tree/main/most_synapses): reconstructions and synaptic analyses of an excitatory pyramidal neuron with the most synapses in the volume, along with an inhibitory basket neuron making the most synapses onto other processes within the volume. 

![neuron with the most synpases in the layer 2/3 volume](most_synapses/pyramidal_neuron.png "neuron with the most synpases in the layer 2/3 volume")

### Reciprocal pairs
Pairs of neurons in the Layer 2/3 volume that synapse onto one another

[`reciprocal_pairs` folder](https://github.com/shandran/layer23-volume/tree/main/reciprocal_pairs): Martinotti-bipolar reciprocal pair (cell ids 648518346349538179 and 648518346349515986, respectively).  

![Martinotti-bipolar reciprocal pair](reciprocal_pairs/martinotti_bipolar_reciprocal_pairs.png "Martinotti-bipolar reciprocal pair")


### An exceptional oligodendrocyte
[`oligodendrocyte_648518346349508279` folder](https://github.com/shandran/layer23-volume/tree/main/oligodendrocyte_648518346349508279): a beautiful example of an oligocyte in the layer 2/3 volume. Images of myelination as well as an example of mis-segmentation where a synaptic bouton from a nearby axon was incorrectly segmented to the oligodendrocyte cell.

![oligodendrocyte myelinating a neuronal process](oligodendrocyte_648518346349508279/oligo_neurite_vtk.png "oligodendrocyte myelinating a neuronal process")

### 3D nuclei visualizer with vasculature
[`vtk_nuclei_visualizer_with_vasculature.ipynb`](https://github.com/shandran/layer23-volume/blob/main/vtk_nuclei_visualizer_with_vasculature.ipynb): notebook to create a 3D visualization of cell nuclei in the Layer 2/3 volume. Uses meshparty, vtk, and OpenGL. Here, nuclei from excitatory neurons is shown in light blue; nuceli from inhibitory neurons in light red, and nuclei from glial cells are shown in olive green. Vasculature in the Layer 2/3 volume is shown in light grey. 

![3D interactive visualization with nuclei colored by cell type and including vasculature](img/vtk_nuclei_visualizer_with_vasculature.png "3D interactive visualization with nuclei colored by cell type and including vasculature")

***

##### Thank you for stopping by!

Drop me an email if you have any questions or would like to collaborate.
Shawn
