## KNN:
KNN normally finds the nearest data points to a given observation.
1. Select one observation.
2. Find the K nearest neighbor based on their distance.
3. Calculate the average distance to those neighbors.
4. Repeat for every observation.
5. Students with unusually large average distances become potential anomalies.
Important: KNN does not automatically know what an abnormal score is. It measures how isolated a record is compared with other records.


the correct order: (to make best use of anomaly detection algo)

1. split the data into training and testing
2. Detect anomalies in training data
3. Investigate flagged records
4. Clean or retain
5. Train your ML model