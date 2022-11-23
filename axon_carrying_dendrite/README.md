# Axon-Carrying Dendrite (possibly!)
Visualization of a partial dendrite and axon (soma not in volume) with a possible axon-carrying dendrite for cell id 648518346349536971

***

## Neuroglancer
View the partial processes in [neuroglancer](https://neuromancer-seung-import.appspot.com/#!%7B%22layers%22:%5B%7B%22source%22:%22precomputed://gs://microns_public_datasets/pinky100_v0/son_of_alignment_v15_rechunked%22%2C%22type%22:%22image%22%2C%22blend%22:%22default%22%2C%22shaderControls%22:%7B%7D%2C%22name%22:%22EM%22%7D%2C%7B%22source%22:%22precomputed://gs://microns_public_datasets/pinky100_v185/seg%22%2C%22type%22:%22segmentation%22%2C%22selectedAlpha%22:0.51%2C%22segments%22:%5B%22648518346349536971%22%5D%2C%22skeletonRendering%22:%7B%22mode2d%22:%22lines_and_points%22%2C%22mode3d%22:%22lines%22%7D%2C%22name%22:%22cell_segmentation_v185%22%7D%2C%7B%22source%22:%22precomputed://matrix://sseung-archive/pinky100-clefts/mip1_d2_1175k%22%2C%22type%22:%22segmentation%22%2C%22skeletonRendering%22:%7B%22mode2d%22:%22lines_and_points%22%2C%22mode3d%22:%22lines%22%7D%2C%22name%22:%22synapses%22%7D%2C%7B%22source%22:%22precomputed://matrix://sseung-archive/pinky100-mito/seg_191220%22%2C%22type%22:%22segmentation%22%2C%22skeletonRendering%22:%7B%22mode2d%22:%22lines_and_points%22%2C%22mode3d%22:%22lines%22%7D%2C%22name%22:%22mitochondria%22%7D%2C%7B%22source%22:%22precomputed://matrix://sseung-archive/pinky100-nuclei/seg%22%2C%22type%22:%22segmentation%22%2C%22skeletonRendering%22:%7B%22mode2d%22:%22lines_and_points%22%2C%22mode3d%22:%22lines%22%7D%2C%22name%22:%22nuclei%22%7D%5D%2C%22navigation%22:%7B%22pose%22:%7B%22position%22:%7B%22voxelSize%22:%5B4%2C4%2C40%5D%2C%22voxelCoordinates%22:%5B74731.5546875%2C54819.9609375%2C1025.518310546875%5D%7D%7D%2C%22zoomFactor%22:383.0066650796121%7D%2C%22perspectiveOrientation%22:%5B-0.20825789868831635%2C-0.3129841387271881%2C0.4062955677509308%2C0.8328226208686829%5D%2C%22perspectiveZoom%22:871.3464965180995%2C%22showSlices%22:false%2C%22selectedLayer%22:%7B%22layer%22:%22cell_segmentation_v185%22%7D%2C%22layout%22:%7B%22type%22:%223d%22%2C%22orthographicProjection%22:true%7D%7D).


## Summary Presentation
View the summary presentation file: [`axon_carrying_dendrite_presentation.pdf`](https://github.com/shandran/layer23-volume/blob/main/axon_carrying_dendrite/axon_carrying_dendrite_presentation.pdf)

## Synapse visualization
This reconstruction was made using the [`synapse_visualizer.ipynb` notebook](https://github.com/shandran/layer23-volume/blob/main/synapse_visualizer.ipynb). The post-synaptic sites (on the dendrites) are shown in red and the pre-synaptic sites (on the presumtive axon) are shown in green.

![Pre- and post-synaptic sites on the axonal and dendritic processes](axon-carrying-dendrite-synapse_sites.png "Pre- and post-synaptic sites on the axonal and dendritic processes")

## Raw Electron Micrographs show it is likely not a segmentation error
Review of the raw EM images, the presumptive axonal process is continuous with the dendrite and does not appear to be a segmentation error.

![EM view of axon-carrying dendrite](axon_carrying_dendrite_em.png "EM view of axon-carrying dendrite")

***

# Wahle et al, ELife 2002
Axon-carrying dendrites (AcD) are not uncommon in rodents, with estimated 10-21% of pyramidal neurons have AcDs. See their [paper in eLife](https://elifesciences.org/articles/76101) entitle *Neocortical pyramidal neurons with axons emerging from dendrites are frequent in non-primates, but rare in monkey and human*.
