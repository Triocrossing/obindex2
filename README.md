# OBIndex2 - Online Binary Image Index

OBIndex2 is an open source C++ library for indexing images. It implements a hierarchical indexing scheme to match binary descriptors, which is used as an incremental Bag-Of-Words (BoW) visual vocabulary. This index is combined with an inverted file in order to provide an image database, that can be queried for finding similar images. This online binary visual vocabulary tries to solve the main drawbacks that classical BoW approaches present, avoiding the training step and adapting the visual dictionary to the operating environment.

OBIndex2 is released as a standalone library or ROS package, and relies on OpenCV 3.x and Boost libraries. It can be used with any binary descriptor computed using the OpenCV format.

The library is an evolution of [OBIndex](http://github.com/emiliofidalgo/obindex). The main improvements included are:
* OBIndex2 provides a policy for deleting visual words, which reduces the size of the visual vocabulary with little impact on the performance.

* FLANN library is no longer required. This is an implementation from the scratch of the full approach.

* It is not needed to specify the number of descriptors to index in advance.

* Several modifications have been developed to speed up the approach.

Note that OBIndex2 is research code. The authors are not responsible for any errors it may contain. **Use it at your own risk!**

# Conditions of use

OBindex2 is distributed under the terms of the [GPL3 License](http://github.com/emiliofidalgo/obindex2/blob/master/LICENSE).

# Related publication

The details of the algorithm are explained in the following publication:

**iBoW-LCD: An Appearance-based Loop Closure Detection Approach using Incremental Bags of Binary Words**
Emilio Garcia-Fidalgo and Alberto Ortiz
Submitted to IEEE RA-L and IROS 2018

# Usage

For an example of use, see the demo file (`lib/tests/test_search.cc`).

# Contact

If you have problems or questions using this code, please contact the author (emilio.garcia@uib.es). [Feature requests](http://github.com/emiliofidalgo/obindex2/issues) and [contributions](http://github.com/emiliofidalgo/obindex2/pulls) are totally welcome.
