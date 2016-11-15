^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package orb_slam
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* Update System.cc
* SaveTrajectory functions retrieve full frame trajectory using relative rigid body transformations between each frame and its reference keyframe. This relative transform is computed when the frame was tracked. This is inaccurate in the monocular case, as each relative transformation is computed at the particular scale when each frame was tracked. A global scale change will make all relative transformations invalid, and this can happen in two cases:
  1) At loop closure
  2) When the map is small and all keyframes are optimized in the Local BA. In that case the scale is not fixed and can change.
* Make clearer that SaveTrajectoryKITTI and SaveTrajectoryTUM do not work for monocular.
* Update Dependencies.md
* How to run EuRoC Dataset (mono and stereo)
* Simpler keyframe insertion policy regarding stereo points.\n Added EuRoC mono and stereo examples. \n Some bug fixes.
* Added documentation for stereo ROS node and EuRoC dataset example.
* Stereo ROS node
* Update README.md
* Add include: Some OpenCV versions seem to complain
* Update System.cc
* Adding missing include for setprecision()
* Update ORBextractor.cc
* Update LICENSE.txt
* Update ros_rgbd.cc
* Update stereo_kitti.cc
* Update mono_kitti.cc
* Update mono_tum.cc
* Update Tracking.h
* Fix bug: Local Mapping got stucked at System::Shutdown() if it was already stopped (e.g. if Localization Mode is active)
* Fix bug in Pangolin producing a segfault when the program ends.
* Update System.h
* Update README.md
* Add Files
* Initial commit
* Contributors: Raul Mur-Artal
