# Mitochondria Inclusions in Astrocytes
Visualization tools for mitochondria inclusions in astrocytes in the Layer 2/3 EM volume

![inclusion in mitochondria 2528399 of astrocyte 648518346349538089 of the Layer 2/3 EM volume](cid_648518346349538089_mid_2528399_100dpi_mitoseg_slice_13_512.jpg "inclusion in mitochondria 2528399 of astrocyte 648518346349538089 of the Layer 2/3 EM volume")

***

# Summary Presentation

### View the [**Astrocyte Mitochondria Inclusions**](https://github.com/shandran/layer23-volume/blob/main/astrocyte_mitochondria_inclusions/Mitochondria_Inclusions_in_Astrocytes.pdf) summary presentation file, with visualization examples of mitchondria inclusions in astrocytes.

***

# Contents

***

## Visualization tools

[`EM_image_generator_master_astrocyte_inclusions.ipynb` notebook](https://github.com/shandran/layer23-volume/blob/main/astrocyte_mitochondria_inclusions/EM_image_generator_master_astrocyte_inclusions.ipynb): Uses cloudvolume and imageryclient libraries to create electron micrograph (EM) images from the Layer 2/3 volume. From Neuroglancer, grab the cellid and mitoid of interest, along with coordinates of the bottom and top slices. The notebook will create cell and mito segmentations, as well as options for creating single images, image stacks and image montages.

[`vtk_astrocyte_mitochondria_visualizer_using_threshold_with_neuroglancer_all_mitos.ipynb` notebook](vtk_astrocyte_mitochondria_visualizer_using_threshold_with_neuroglancer_all_mitos.ipynb): Uses meshparty, vtk, and OpenGL to create an interactive 3D visualization of astrocyte mitochondria. A threshold variable colors mitochondria by number of voxels (default value used in these visualization was 2 million voxels); mitochondria above the threshold are colored blue and red for mitochondria below the threshold. Includes an option to save a high resolution png file. This version also adds a neuroglancer link generator and a vtk visualizer that places the center of view on the mitoid centroid of interest.

***

## A selection of interesting visualizations

### EM cell segmentation using imageryclient

#### Astrocyte 648518346349527319 mito 980814 
EM of inclusion in mitochondria 980814 in astrocyte 648518346349527319 using cell segmentation for colorization.

![EM of inclusion in mitochondria 980814 in astrocyte 648518346349527319 using cell segmentation for colorization](cid_648518346349527319_mid_980814_100dpi_slice_13.jpg "inclusion in mitochondria 980814 in astrocyte 648518346349527319 using cell segmentation for colorization")

### EM mitochondria segmentation using imageryclient

#### Astrocyte 648518346349538089 mito 2528399
EM of inclusion in mitochondria 2528399 of astrocyte 648518346349538089 using the mitochondria segmentation for coloring.

![EM of inclusion in mitochondria 2528399 of astrocyte 648518346349538089 using the mitochondria segmentation for coloring](cid_648518346349538089_mid_2528399_100dpi_mitoseg_slice_13_512.jpg "inclusion in mitochondria 2528399 of astrocyte 648518346349538089 using the mitochondria segmentation for coloring")

### 3D visualization using vtk and OpenGL

#### Astrocyte 648518346341354380 mitos 2643929 and 2643903 
3D vtk visualization of mitochondria 2643929 in astrocyte 648518346341354380. Upon manual inspection, this mitochondria is continous with mito 2643903 and the segmentation is interupted by the inclusion (see summary presentation for additional details). There are several other mitochondria inclusions in this view as well, which can be seen as fragments or holes in the view. 

![3D vtk visualization of mitochondria 2643929 in astrocyte 648518346341354380](648518346341354380_2643929-512_512.png "3D vtk visualization of mitochondria 2643929 in astrocyte 648518346341354380")

### Image montage generator

#### Astrocyte 648518346341354380 mitos 2643929 and 2643903 
Same example as above demonstrating the image montage generator function from the `EM_image_generator_master_astrocyte_inclusions.ipynb` notebook. Twenty-four EM slices were arranged in a 3x8 image montage. Colorization is by cell segmentation for astrocyte 648518346341354380. These two mitochondria are continuous, but electron-bright inclusion causes the segmentation algorithm to separate the mitochondria into two separate ids.  

![EM image montage of two continuous mitos 2643929 and 2643903 in astrocyte 648518346341354380 separated by a mitochondria inclusion, colored by cell segmentation](cid_648518346341354380_mid_2643929_zmontage_100dpi-512.png "EM image montage of two continuous mitos 2643929 and 2643903 in astrocyte 648518346341354380 separated by a mitochondria inclusion, colored by cell segmentation")
