cristinel.ababei@ndsu.edu
December 2008, Fargo ND


This is the parallel VPR place project. 
It implements the parallel VPR, WL driven only. 
The top level placement is 4-way partitioned, using hMetis. 
Then subchips are placed using 4 worker threads. 
Post placement refinement using ultra fast SA placement 
is done at the end.


Benchmarks
==========

TESTS/
Contains all 20 benchmarks of original VPR.

TESTS2/
Contains 12 largest benchmarks that come with latest VPR 5.0.


Parallel VPR
============
To run the parallel version you have to use the new option "-mt_place".
If you use the gui/display option, the parallel VPR will not display
intermediate steps; however, the final placement can be viewed.


Examples
========
Run sequential VPR:
vpr TESTS/misex3.net TESTS/4lut.arch misex3.p misex3.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp
vpr TESTS/e64-4lut.net TESTS/4lut.arch e64.p e64.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp
vpr TESTS/clma.net TESTS/4lut.arch clma.p clma.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp

Run parallel VPR:
vpr TESTS/misex3.net TESTS/4lut.arch misex3.p misex3.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp -mt_place
vpr TESTS/e64-4lut.net TESTS/4lut.arch e64.p e64.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp -mt_place
vpr TESTS/clma.net TESTS/4lut.arch clma.p clma.r -place_only -place_algorithm bounding_box -fix_pins random -nodisp -mt_place


Copyright
=========
Copyright 2008 by Cristinel Ababei, cristinel.ababei@ndsu.edu
This Copyright notice applies to all files, called hereafter 
"The Software".
Permission to use, copy, and modify this software and its 
documentation is hereby granted only under the following 
terms and conditions.  Both the above copyright notice and 
this permission notice must appear in all copies of the 
software, derivative works or modified versions, and any 
portions thereof, and both notices must appear in supporting 
documentation.  Permission is granted only for non-commercial 
use.  For commercial use, please contact the authors.
This software may be distributed (but not offered for sale 
or transferred for compensation) to third parties, provided 
such third parties agree to abide by the terms and conditions
of this notice.
The Software is provided "as is", and the authors, the 
North Dakota State University (NDSU), the University of Toronto, 
as well as any and all previous authors (of portions or modified 
portions of the software) disclaim all warranties with regard to 
this software, including all implied warranties of merchantability
and fitness.  In no event shall the authors or NDSU or any and
all previous authors be liable for any special, direct, 
indirect, or consequential damages or any damages whatsoever
resulting from loss of use, data or profits, whether in an
action of contract, negligence or other tortious action,
arising out of or in connection with the use or performance
of this software.
