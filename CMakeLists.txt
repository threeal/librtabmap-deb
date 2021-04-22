cmake_minimum_required(VERSION 3.16)

add_subdirectory("rtabmap")

set(CPACK_GENERATOR "DEB")
set(CPACK_DEBIAN_FILE_NAME DEB-DEFAULT)

set(CPACK_DEBIAN_PACKAGE_NAME "librtabmap-dev")

set(CPACK_DEBIAN_PACKAGE_VERSION 0.20.10)
set(CPACK_DEBIAN_PACKAGE_RELEASE 1)

set(CPACK_DEBIAN_PACKAGE_DESCRIPTION
  "RTAB-Map library and standalone application
 RTAB-Map (Real-Time Appearance-Based Mapping) is a RGB-D, Stereo and Lidar
 Graph-Based SLAM approach based on an incremental appearance-based loop
 closure detector. The loop closure detector uses a bag-of-words approach to
 determinate how likely a new image comes from a previous location or a new
 location. When a loop closure hypothesis is accepted, a new constraint is
 added to the map’s graph, then a graph optimizer minimizes the errors in the
 map. A memory management approach is used to limit the number of locations
 used for loop closure detection and graph optimization, so that real-time
 constraints on large-scale environnements are always respected. RTAB-Map can
 be used alone with a handheld Kinect, a stereo camera or a 3D lidar for 6DoF
 mapping, or on a robot equipped with a laser rangefinder for 3DoF mapping.")

set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Alfi Maulana <alfi.maulana.f@gmail.com>")
set(CPACK_DEBIAN_PACKAGE_HOMEPAGE "http://introlab.github.io/rtabmap")

set(CPACK_DEBIAN_PACKAGE_DEPENDS
  "libceres-dev, libdc1394-dev, libeigen3-dev, libflann-dev, libfreenect-dev, libgflags-dev, liboctomap-dev, libomp-dev, libopencv-dev, libopenni-dev, libpcl-dev, libsqlite3-dev, libsuitesparse-dev, libqhull-dev, libusb-dev, zlib1g-dev")

include(CPack)
