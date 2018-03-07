# SLAM for dummies

## Notes:

## Introduction

SLAM is (obviously) the acronym for simultaneous localization and mapping, which was developed by Hugh Durrant-Whyte and John J. Leonard.

SLAM has multiple parts

1. landmark extraction
2. data association
3. state estimation
4. state update
5. landmark update

These parts can be updated for new technologies (**New research topic**).

To understand SLAM, one should know **EKF** (Extended Kalman Filter).

### How Extended Kalman Filter (EKF) is used in SLAM

- Based off of Kalman Filter (non-linear version)
- Heart of SLAM process
- It is responsible for updating where the robot thinks it is based on the 'features' received from the sensor(s) 
  - features == landmarks
- keeps track of an estimate of the uncertainty in the robots **position** and also the uncertainty in these **landmarks**  it has seen in the environment
- when the odometry changes (due to the robot moving) the uncertainty ertaning to the robots new position is updated in the EKF using odometry update
- landmarks are then extracted from the environment from the new position
- the robot then **attempts** to associate these landmarks to observations of landmarks it previously has seen
- re-observed landmarks are then used to update the robots position in the EKF
- landmarks which have not been proviously been seen are added to the EKF as new observations so they can be re-observed later

