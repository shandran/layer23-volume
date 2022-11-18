# layer23-volume
Reconstructions and analyses of mouse cortex Layer 2/3 serial EM volume

Attribution: https://www.microns-explorer.org/terms-and-conditions<br>
Citation: https://www.microns-explorer.org/citation-policy<br>

***

### Over a century ago, Golgi and Cajal revolutionized the field of neuroscience

For an interesting summary of this revolution, read Mitch Glickstein's essay on Golgi and Cajal in <em>Cell</em>: https://www.cell.com/current-biology/pdf/S0960-9822(06)01203-6.pdf

![Pyramidal neuron of the mouse cortex stained using the Golgi method](img/golgistain.png "Serial LM reconstruction of Golgi stained neuron")  

<em>Image credit: by author, using a Zeiss Photomicroscope II at 40x oil. Reconstruction using Smart Objects in Photoshop.</em>

### Once again neuroscience is undergoing another revolution with the serial electron microscope brain reconstructions

![Pyramdial neuron from the Layer 2/3 serial EM volume](img/layer23pyr.png "Serial EM reconstruction using Neuroglancer")  

<em>Image credit, by author, using Neuroglancer of pyramidal neuron with cellid 648518346349538440.</em> 

***

## Contents

### Look up tools

Use `lookup_cellid_in_layer23_volume.ipynb` to identify the cell subtype for a given cellid in the Layer 2/3 volume. This is a human-curated list for cells that contain all (or most) of the cell soma within the volume.

Use `lookup_mitochondria_ids.ipynb` to look up mitochondria ids by cellid. Useful for creating a list of mito ids for visualization in neuroglancer and for analyzing voxel data.

Use `lookup_synapse_ids.ipynb` to look up synapse ids by pre- and post-synaptic cell ids. Also contains voxel data.

### Visualization and analyses of interesting features

`most_synapses` folder: reconstructions and synaptic analysis of an excitatory pyramidal neuron with the most synapses in the volume, along with an inhibitory basket neuron with making the most synapses onto other processes within the volume. 

`oligodendrocyte_648518346349508279` folder: a beautiful example of an oligocyte in the layer 2/3 volume. 
