# Simultaneous Localization and Mapping (SLAM)- Part I

## Paper 

- Title: Simultaneous Localization and Mapping
- Authors: Hugh Durrant-Whyte and Tim Bailey
- Link:
- Tags:
- Year: 2006



## Summary/Notes

- At a theoretical and conceptual level, SLAM can now be considered a solved problem
- History of SLAM problem
  - genisis of the probabilistic SLAM problem occurred at the 1986 IEEE Robotics and Automation Conference
  - want to add estimation-theoretic methods to mapping and localization problems
    - Peter Cheeseman, Jim Crowley, and Hugh Durrant-Whyte
  - consistant probabilistic mapping was a fundamental problem in robotics with major conceptual and computational issues
  - there must be a high degree of correlation between estimates of the location of different landmarks in a map and that these correlations would grow with successive observations
  - taking relative observations of landmarks, the estimates of these landmarks are all necessarily correlated with each other because of the common error in estimated vehicle location
  - a consistent full solution to the combined localization and mapping problem would require a join state composed of the vehicle pose and every landmark position, to be updated following each landmark observation 
    - This would require large state vector (on the order of the number of landmarks maintained in the map) with computation scaling as the square of the number of landmarks
  - instead focused on a series of approximations to the consistent mapping problem