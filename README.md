## OVERVIEW:

This program loads a character skin from a .skin file (described below) and attach it to a skeleton (loaded from a .skel file).

The skin should be rendered with shading using at least two different colored lights.

The program should allow some way to adjust DOF values in the skeleton. At a minimum, it could have keys for next/last DOF and increase/decrease value. Optionally, it could use widgets in a GUI to adjust the values or allow the user to interactively pick a joint and adjust it with the mouse.

The program should be able to load any .skin and .skel file given to it, and should accept .skin and .skel file name as a command line argument. For example:

project2 monster.skel monster.skin
If no file name is given, it should default to 'wasp.skel' and 'wasp.skin'.

## .skin FILE DESCRIPTION:

The .skin file contains arrays of vertex data, an array of triangle data, and an array of binding matrices. For a sample .skin file, see tube_smooth.skin and its corresponding .skel file tube.skel. For a very simple example, see triangle.skin.

positions [numverts] {
    [x] [y] [z]
    ...
}

normals [numverts] {
    [x] [y] [z]
    ...
}

skinweights [numverts]
    [numattachments] [joint0] [weight0] ... [jointN] [weightN]
    ...
}

triangles [numtriangles] {
    [vertex0] [vertex1] [vertex2]
    ...
}

bindings [numjoints]
    matrix {
        [ax] [ay] [az]
        [bx] [by] [bz]
        [cx] [cy] [cz]
        [dx] [dy] [dz]
    }
    ...
}

## PROGRAM OBJECTIVES:

- Skin attached to skeleton properly
- Lighting & normals working properly
- Interactive control working
