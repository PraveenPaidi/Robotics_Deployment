# Robotics_Deployment

1.We made our own Neural Network for the feature generation by taking training data of images from OAK-D camera.

2.From the custom NN model, We deployed model to ROS node which does face mask recognition in real time by subscribing to real time data current_frame.

3.We used inbuilt software called MTCNN face detection algorithm for creation of the bounding box for faces which is also subscribing to real time data current_frame.

4.We published a custom topic /go/image from face mask recognition ROS node to MTCNN_vel_pub(fcae tracking) node which is subscriber to /go/image and publishes /cmd/vel.

5.If the MTCNN_vel_det(face tracking) is being sent face without mask, it publishes velocity to move towards that face by using Face bounding box coordinates.



<img width="565" alt="Screenshot 2023-08-18 013756" src="https://github.com/PraveenPaidi/Robotics_Deployment/assets/120610889/b45b8859-44b1-45e4-a1ce-098902f589a3">


<img width="546" alt="Screenshot 2023-08-18 013848" src="https://github.com/PraveenPaidi/Robotics_Deployment/assets/120610889/69ed51c0-91ed-44b7-8f52-912b9eb43f9d">


<img width="430" alt="Screenshot 2023-08-18 013809" src="https://github.com/PraveenPaidi/Robotics_Deployment/assets/120610889/81311f20-ce5f-4d20-b719-ea3038fa857e">


<img width="498" alt="Screenshot 2023-08-18 013827" src="https://github.com/PraveenPaidi/Robotics_Deployment/assets/120610889/a8c8e178-d48d-4c47-8c36-58bc109b7bb2">


