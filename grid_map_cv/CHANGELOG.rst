^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package grid_map_cv
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.0.1 (2025-01-18)
------------------
* Merge pull request `#447 <https://github.com/Ryanf55/grid_map/issues/447>`_ from ANYbotics/mergify/bp/humble/pr-442
  Bugfix use old style include directories for filters (backport `#442 <https://github.com/Ryanf55/grid_map/issues/442>`_)
* Add link to upstream ticket
  (cherry picked from commit b18744764cec4bd165f0f7486f37282bafb79861)
* Use old-style variables for filter include directories
  (cherry picked from commit 66a07d8656dfb91bbb39b3ca45378d7f51d44414)
* Merge pull request `#445 <https://github.com/Ryanf55/grid_map/issues/445>`_ from ANYbotics/mergify/bp/humble/pr-443
  Add Ryan as maintainer, remove Steve (backport `#443 <https://github.com/Ryanf55/grid_map/issues/443>`_)
* Add Ryan as maintainer, remove Steve
  (cherry picked from commit 852f67694637612e624e4c683a01ab589408b8e7)
* Merge pull request `#434 <https://github.com/Ryanf55/grid_map/issues/434>`_ from ANYbotics/mergify/bp/humble/pr-404
  grid_map_core: Use ament_export_targets and improve eigen linkage (backport `#404 <https://github.com/Ryanf55/grid_map/issues/404>`_)
* fix: use target link libraries instead of ament target deps
  (cherry picked from commit 89ead0384524c728d86e17e227cb0d1ad470ea6e)
* Update ament to latest recommendations
  * Fixes include errors in grid_map_geo ros2 port
  (cherry picked from commit 4f32682271add9477a4566596c1997053d59f345)
* Contributors: Ryan, Ryan Friedman, wep21

2.0.0 (2022-09-13)
------------------
* fix: mark Eigen library as SYSTEM
* fix: build error on jammy
* Initial ROS2 port
* Contributors: Maximilian Wulf, Steve Macenski

1.6.2 (2019-10-14)
------------------

1.6.1 (2019-02-27)
------------------
* Updated host changes.
* Updated author e-mail address.
* Contributors: Peter Fankhauser, Péter Fankhauser

1.6.0 (2017-11-24)
------------------
* Fixed compatibility issue with OpenCV 3 (`#140 <https://github.com/anybotics/grid_map/issues/140>`_).
* Makes the OpenCV include a bit more specific and adds in a dependency into the catkin_package call.
* Moved inpaint filter to grid_map_cv, extended filter demo, cleanups.
* Fixed problem where clamp changes were disregarded (`#115 <https://github.com/anybotics/grid_map/issues/115>`_ from Le-Fix/fix/toImageClamp).
* Contributors: Péter Fankhauser, Perry Franklin, Le-Fix

1.5.2 (2017-07-25)
------------------

1.5.1 (2017-07-25)
------------------

1.5.0 (2017-07-18)
------------------
* Fixed bug for change resolution function in OpenCV processing class (including unit tests). (`#91 <https://github.com/anybotics/grid_map/issues/91>`_).
* Extend grid_map_cv unit test for transparent pixels/nan-values.
* Remove constructor and destructor declaration in GridMapCvConverter.
* Contributors: Peter Fankhauser, Marco Camurri, Sascha

1.4.2 (2017-01-24)
------------------
* Fixed conversion to/from images in float&double format.
* Contributors: Peter Fankhauser

1.4.1 (2016-10-23)
------------------
* Improved transformation of images to color grid map layers.
* Contributors: Peter Fankhauser

1.4.0 (2016-08-22)
------------------

1.3.3 (2016-05-10)
------------------
* Release for ROS Kinetic.
* Contributors: Peter Fankhauser

1.3.2 (2016-05-10)
------------------
* Updated dependency to OpenCV for compatibility with ROS Kinetic and OpenCV 2/3.
* Contributors: Peter Fankhauser

1.3.1 (2016-05-10)
------------------

1.3.0 (2016-04-26)
------------------
* Separated OpenCV to grid map conversions to grid_map_cv package. The new methods
  are more generalized, faster, and can be used without ROS message types.
* Added new convenience function to change the resolution of grid maps with help of the OpenCV interpolation methods.
* Added `initializeFromImage()` to GridMapCvConverter.
* Added unit tests for grid_map_cv. Updated documentation.
* Resolving build errors for OpenCV.
* Fixed typo and added documentation.
* Contributors: Peter Fankhauser, Dominic Jud,
