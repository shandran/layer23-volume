# Decimated meshes in the Layer 2/3 Volume
Using a mesh decimation protocol to significantly reduce mesh sizes of cell body and mitochondria features.

A special thanks to Tyler Sloan for his advice and pyvista [code](https://github.com/Quorumetrix/Blender_scripts/blob/main/Mesh%20Decimation%20Pipeline.ipynb) for mesh decimation. See more of Tyler's work at [Quorumetrix Studio](https://www.quorumetrix.com/). I also thank [Forrest Collman](https://alleninstitute.org/person/forrest-collman/) at Allen Institute for his [tutorial notebooks](https://github.com/AllenInstitute/MicronsBinder/tree/master/notebooks) for reading and generating the trimesh objects and setting up the trimesh_vtk visualization tools and animations.

See the Microns explorer page at the [Allen Brain Institute](https://www.microns-explorer.org/terms-and-conditions) for more details about the Layer 2/3 volume, terms and conditions.

![All astrocyte mitochondria with vasculature](all_astro_mito_with_vasc_2024_08_01_1950_40.png "all astrocyte mitochondria with vasculature")

This view shows all the mitochondria (over 41K meshes) in all 44 astrocytes identified in the Layer 2/3 volume, along with the vasculature. The astrocyte cell bodies are not rendered (although the code allows for this), as the astrocyte cell bodies are so complex (even when decimated) that rendering them only serves to reduce clarity.

***

# Contents

## Jupyter Notebook files

Download the cell type data tables on the [Allen Institute Microns Phase 1](https://www.microns-explorer.org/phase1) page, and the mitochondria info on [Zenodo](https://zenodo.org/record/5579388/files/211019_mitochondria_info.csv).

### Mesh decimation notebooks

Use [`pyvista_decimate_mesh_astro_cell_bodies.ipynb`](https://github.com/shandran/layer23-volume/blob/main/decimated_meshs/pyvista_decimate_mesh_astro_cell_bodies.ipynb) to decimate the cell body meshes for the 44 identified astrocytes in the Layer 2/3 volume. Default decimation of 95%. This will result in some minor loss of distal leaflets of the astrocyte cell body but over all a good balance of decimation and mesh preseveration. The astrocyte meshes take the longest of any cell type (even more than vascular cells) to decimate. The total time to decimate all 44 astrocytes was 20+ hours on a standard laptop.

Use [`pyvista_decimate_mesh_vasc_cell_bodies.ipynb`]() to decimate the cell body meshes for the vascular cells identified in the Layer 2/3 volume. These take an hour or so to process.

Use [`decimated_meshs/pyvist_mesh_decimation_astrocyte_mitochondria_batch_processing.ipynb`](https://github.com/shandran/layer23-volume/blob/main/decimated_meshs/pyvist_mesh_decimation_astrocyte_mitochondria_batch_processing.ipynb) to decimate the mitochondria meshes for the astrocytes identified in the Layer 2/3 volume. This consists of over 41,000 mitochondria meshes, however, the decimation is fast and efficient, taking several minutes (instead of hours) to process.

### vtk visualization notebooks

Use [`decimated_meshs/vtk_decimated_astro_meshes.ipynb`](https://github.com/shandran/layer23-volume/blob/main/decimated_meshs/vtk_decimated_astro_meshes.ipynb) to visualize the astrocyte cell bodies with the decimated meshes.

Use [`vtk_decimated_meshes_astro_mitos_with_vasc.ipynb`](https://github.com/shandran/layer23-volume/blob/main/decimated_meshs/vtk_decimated_meshes_astro_mitos_with_vasc.ipynb) to visualize the astrocyte cell bodies and vascular cells with the decimated meshes.

Use [`vtk_decimated_meshes_by_celltype.ipynb`](https://github.com/shandran/layer23-volume/blob/main/decimated_meshs/vtk_decimated_meshes_by_celltype.ipynb) to visualize the astrocyte cell bodies, all of their respective mitochondria, and the vascular cells with the decimated meshes. Also has options for looking at one astrocyte at a time instead of all astrocytes at once (if you visualize all 41K mito meshes, even with the decimation, it will really bog down a typical laptop).

***

## Visualizations

### An example astrocyte and all of its mitochondria with vasculature

![astrocyte 648518346349490239 and all of its mitochondria located near a blood vessel in the Layer 2/3 volume](astro_648518346349490239_mito_with_vasc_2024_08_02_1025_29.png "astrocyte 648518346349490239 and all of its mitochondria located near a blood vessel in the Layer 2/3 volume")
