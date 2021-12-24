# Writeup: 3D Object Detection

## Visualizing the Point Cloud

After visualizing the point cloud for a dataset and exploring them in Open3D, we can see a number of examples of vehicles of varying degrees of visibility.

![Point Cloud Visualizations](./img/pcl.png)

Among these examples, we see vehicles in the path of motion, in front of and behind the lidar sensor.
We also see vehicles parked along the roadway and in parking lots adjacent to the road.
In many of these examples, we can see common features that standout as identifying a vehicle, including their general outline, windows, wheels, and side mirrors.
In some cases, we can see elements as small as radio antennae or interior seats and headrests.
From head-on or behind, it is often easy to identify the side mirrors for vehicles, though in some cases those mirrors amount to only a handful of pixels in resolution.
From closer up or side profile, we can see much more detail, like roof bars or lights.

We can also see some of these same features when inspecting the range image.
Viewing these images with range and intensity shown in different outputs can make elements that are very reflective, like tail light reflectors and license places, very obvious.

![Range Image](./img/ri.png)
