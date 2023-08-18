# Robotics_Deployment

We made our own Neural Network for the feature generation by taking training data of images from OAK-D camera.
From the custom NN model, We deployed model to ROS node which does face mask recognition in real time by subscribing to real time data current_frame.
We used inbuilt software called MTCNN face detection algorithm for creation of the bounding box for faces which is also subscribing to real time data current_frame.
We published a custom topic /go/image from face mask recognition ROS node to MTCNN_vel_pub(fcae tracking) node which is subscriber to /go/image and publishes /cmd/vel.
If the MTCNN_vel_det(face tracking) is being sent face without mask, it publishes velocity to move towards that face by using Face bounding box coordinates.

