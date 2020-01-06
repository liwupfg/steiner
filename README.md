# steiner
obstruction aware steiner tree with source-to-sink control

This is an alpha release for a future python module steinerpy. The executable steiner-A binary can be found in the release package, steiner-A is compiled from C++ source.

please report all bugs and enhancement suggestion to

fe2o3@mit.edu

Thanks.

=== how to run the steiner-A executable ===
0. provided file,
 steiner-A : the executable
 in.dat : a sample input file (documentation at top of the file as comments)
 h.dat : a sample file that contains all the horizonatlly blocked rectangles
 v.dat : a sample file that contains all the vertically blocked rectangles
 f.dat : a sample file that contains all the fully blocked rectangles
 
1. run steiner-A without any argument to show the suggested run command
 steiner-A
 gives 
 Usage :  steiner-A input=in.dat output=out.dat hblock=h.dat vblock=v.dat fblock=f.dat dump=1

or ( steiner-A input=<in.dat> output=<out.dat> [hblock=<h.dat>] [vblock=<v.dat>] [fblock=<f.dat>] [dump=1] )

2. if dump=1 is specified, each tree will have a corresponding python file created.
   type python3 tree1_*.py& to view tree1 (the gui is very primitive, based on tkinter)

3. the output of each tree will be reported in the out.dat that you specified in the run command
   each tree is reported by 2 lines, the first line gives each node of the tree, and a node number.
   (it starts with all the original input nodes followed by newly added steiner points)
   Second line begins with a space followed by whether the tree in build with violation or not, and child->parent edges
   (if you choose dump=1 the GUI display will have a cross mark at the root/source of the tree
   for trees with violation, i.e. there are forced connection inside blockages)

4. you can also examine the created log file for the run time of each tree.
