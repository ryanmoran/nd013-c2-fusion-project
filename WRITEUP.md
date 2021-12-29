# Writeup: Track 3D-Objects Over Time

## 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

### Step 1: Tracking

In the first step of the project, we implemented the Extended Kalman Filter.
This allowed us to track the single vehicle using only the lidar measurements.
As can be seen below, the mean RMSE result is below the expected 0.35 threshold.
While the tracking was reasonably good, we can improve on this by including measurements from the camera and tuning the parameters.

![Step 1 RMSE](./img/step-1-rmse.png)

### Step 2: Track Management

### Step 3: Data Association

### Step 4: Sensor Fusion


### 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?


### 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?


### 4. Can you think of ways to improve your tracking results in the future?
