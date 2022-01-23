# MagicaVoxel Improved Obj

A script that improves `.obj` and `.mtl` files exported from MagicaVoxel.

Specifically, it does the following:
    - makes each colour a separate material
    - creates new UV values (based on global coordinates) that make it easier to apply textures in a game engine, modeling software, etc.

# More Details

This works best if you use relatively few colours, with each colour
representing a different texture that you plan to apply later in
other software.

Note that while this script creates multiple materials and new texture vertices
(so the `.mtl` and `.obj` files may get *slightly* bigger), the 3D geometry
is not modified at all. Thus, there shouldn't be any serious efficiency
concerns.

# Dependencies

Requires `numpy` and `pillow`.

# Instructions:

Modify a file in place:
`python mvio.py input.obj`

Output to a separate file:
`python mvio.py input.obj output.obj`

Modify all files in a directory:
`python mvio.py input_dir`

Output in separate directory:
`python mvio.py input_dir output_dir`

For help:
`python mvio.py`

