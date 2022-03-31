# People-counter
The idea behind this project is to create a People counting system that aims at automatically estimating the number of people indoor and outdoor places. A video is captured and will be given as input to the system. This People Counter will then process the video and count the number that have entered and exited the video frame with the help of OpenCV. In order to track and count an object in a video stream, the detected object is registered by assigning object ID and their centroids are saved. For effective counting of objects, centroid object tracking algorithm is implemented. The centroid tracking algorithm makes the assumption that pairs of centroids with minimum Euclidean distance between them must be the same object ID.![image](https://user-images.githubusercontent.com/67202732/161114132-34b995e8-03e0-42f0-b35a-3f5acca29b08.png)
Module 1: Person Detection
Get the camera / Video Feed
Detect people in the frame using the cafe pre-trained model
Localize the pedestrians in the frame
use the detected person bounding box coordinates to track them
Module 2:  Tracking Phase:
create an object tracker for each detected object to track the object as it moves around the frame
continue tracking until  the N-th frame is reached  and then re-run our object detector
Module-3: Real-Time alert
If selected, we send an email alert in real-time. Use case: If the total number of people (say 10 or 30) exceeded in a store/building, we simply alert the staff.
You can set the max. people limit in config. (Threshold = 10).
This is pretty useful considering the COVID-19 scenario.
Module- 4: Simple log
Logs all data at end of the day.
Useful for footfall analysis.

