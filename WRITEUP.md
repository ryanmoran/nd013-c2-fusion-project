# Writeup: Track 3D-Objects Over Time

## 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

### Step 1: Tracking

In the first step of the project, we implemented the Extended Kalman Filter.
This allowed us to track the single vehicle using only the lidar measurements.
As can be seen below, the mean RMSE result is below the expected 0.35 threshold.
While the tracking was reasonably good, we can improve on this by including measurements from the camera and tuning the parameters.

![Step 1 RMSE](./img/step-1-rmse.png)

### Step 2: Track Management

In the second step of the project, we implemented track management.
For each track, we initialized and updated a score and state.
When then kept track of those values over time to decide if and when to delete the track.
As can be seen below, the mean RMSE is high, but still below the expected 0.8 threshold for this step.

![Step 2 RMSE](./img/step-2-rmse.png)

### Step 3: Data Association

In the third step of the project, we implemented data association.
For each track and measurement, we associated them by calculating their Mahalanobis distance and associating the nearest measures to their track.
As can be seen in the RMSE plot, we track 3 objects in the scene with a relatively low error.

![Step 3 RMSE](./img/step-3-rmse.png)

### Step 4: Sensor Fusion


### 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?


### 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?


### 4. Can you think of ways to improve your tracking results in the future?
