---
author:
- Rutuj Gavankar
date: 11 December 2017
title: |
    Computational Chemistry - 
    3D Modeling and Bond Geometry
---

Project Summary
===============

This project uses an open-source file format called '.xyz', which is
essentially a text file with the names and coordinates of atoms of a
compound.

The program reads this text file, coverts it into a multidimensional
array, imports a CVS file that contains the periodic table and converts
it into an array. It calculates the bond lengths, bond angles, molecular
mass, and plots it in 3D space. It also generates a unique colour for
each of the atoms.

Use Case Analysis
=================

This project is for people who would like to visualize chemical bonds.
Covalent compounds have specific geometries depending on the number of
lone pairs and the bonds. The bond length, bond angle, both depend on
the electrostatic forces of attraction and repulsion.

XYZ is an open source file format. Downloading a .xyz file of the desired
compound and loading it in the program, the molecule can be graphed in
3d space and the molecular mass, atomic radii, bond length and bond
angles can be calculated.

Data Design
===========

am using arrays for everything. The xyz text file is stored in a 2D
array. The CVS file is stored in a 2D array as well. The program is
divided into functions. Each function does one job and returns a value.
There are also functions that show the values of other functions.

I did not choose object oriented programming because it had no
significant advantage over this approach. Infact, it would be twice as
much tedious. All functions more or less depend on matrix manipulation.

There is also a function to save the output as a .txt file

UI Design
=========

I am using a Jupyter Notebook. The module I am using, VPython, doesn't
work outside Jupyter. The first cell is just the code for people to view
The second cell executes the 3D plot The third cell executes the math
outputs The fourth cell asks for a save file prompt

Algorithm
=========

The XYZ file is imported into python using file functions. It is stored
in a multidimensional array (2x2).The same is done to a CVS file with
the periodic table.

1.  Atomic Mass is calculated by adding up all the masses of individual
    atoms. The masses of atoms are found by comparing the periodic table
    cvs and the xyz file.
    
2.  Covalent Radius of an atom is displayed by using a similar method

3.  Bond length is calculated by calculating the distance between all
    the atoms, and then comparing each of them for finding the ones that
    bond.

4.  Bond Angles are found by converting each of the coordinates to a
    position vector. The difference between 3 position vectors gives 2
    vectors with 1 common point. Angle between these vectors is arc
    cosine of the dot product of them divided by product of their
    lengths. It is then converted to degrees.

Acknowledgment
==============

Modules:

-   SciPy : https://www.scipy.org/

-   Visual Python (VPython): http://www.vpython.org/

-   NumPy : http://www.numpy.org/

-   Jupyter : http://jupyter.org/

Files

-   periodicTable.cvs :
    https://github.com/andrejewski/periodic-table/blob/master/data.csv

-   XYZ files :
    https://github.com/tmpchem/computational\_chemistry/tree/master/geom/xyz

Other Resources:

-   https://cs.iupui.edu/~aharris/230/

-   Stewart, James. Calculus. Cengage Learning, 2016.
