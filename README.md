# Raytracer

A program that creates images from scratch using a number of complex lighting and rendering effects.

First objects are defined in a scene. 
Then raytracing is used to produce realistic & lifelike lighting effects.

## Motivation

This project was created as a submission for [CSC418 - Spring, 2018] at the University of Toronto. The final code & project structure has been modified.

The contributors to this submission were myself, Oliver Straszynski, and Jacob Ritchie.

Some of the code was provided to us as setup (`bmp_io` , `scene_object` , `main`, others), and attribution to the original code authors is made on those individual files.

## Usage

- Install g++

- execute `make -f Makefile clean`

- execute `make -f Makefile raytracer`

- execute `./raytracer`

- See output in `/output_images`

---

### Octree Optimization

An Octree is a 3D space partitioning data structure that allows us to dramatically improve the efficiency of raytracing.

By splitting the virtual 3D space into segments, and determine which object lie in which segments.
Then, we calculate which segment a ray is currently traversing, which dramatically reduces the number of objects that the ray may interact with.

<img width=480 height=360 src="https://github.com/broliver12/raytracer/blob/main/images/octree.png?raw=true"/>

### Cube Mapping

Cube mapping allows us to place objects inside a virtual cube. The inside of this cube forms a 3D view of any scene.

<img width=480 height=360 src="https://github.com/broliver12/raytracer/blob/main/images/cube.bmp?raw=true"/>

### Texture Mapping

Map textures onto a virtual 3D object. 

<img width=480 height=360 src="https://github.com/broliver12/raytracer/blob/main/images/globe.bmp?raw=true"/>

### Phong Reflection Model

Each stage of the Phong model is implemented individually.

<img width=480 height=360 src="https://github.com/broliver12/raytracer/blob/main/images/reflect.bmp?raw=true"/>

### Anti Aliasing

Uses multiple pixels around a ray's intersection point to calculate colour. Result is a smoother, more realistic final image.

---

## License

![UNLICENSED](https://github.com/broliver12/raytracer/blob/main/LICENSE.txt)
