# CDLE_Capstone_Project
Car Brand Detection for CAIP
A simple deep learning car brand identifier using Yolov4

Project name: CAR BRAND DETECTION (MALAYSIAN BRAND)

Problem statement: Are the latest Malaysian brand cars being bought and used in Malaysia? 
Objective: To identify the car brand and the new type of car on the road 

Classes: 
          Perodua_Ativa_H
          Proton_X50
          Proton_X70
          Perodua_Aruz_1.5AV
          
          
Need to install/implement opencv to use

Methodology: Used Darknet Yolov4 on seperate file on colab to create training weights for detection, then use python OpenCV library to run object detection.

Input: Images and video car Output: The car brand detection 

Data Set Sources: Google, Car Brand Websites,Youtube video; Labelled according to yolov4 specification

Network Description: YOLOv4 is a one-stage object detection model that improves on YOLOv3, its widely used and still recives updates to its databases.
                      
                      Input → CSPDarknet53 → [SPP Block + PANet] → YOLOv3
                      (Backbone)          (Neck)          (Head)
                      
                      
Model Traning : Trained for 8000 epochs but the accuracy began to waver and to avoid overfitting, the most optimal weight is 3000, with 4000 included for reference.

average loss 0.235939, 0.219559, 0.001300 rate at 4000 epochs

161 conv layers 		16 batches 		iou threshold = 50%

mean average precision @ 0.50 = 0.920798	          for conf_thresh = 0.25

precision = 0.77	          recall = 0.86		f1 score = 0.81

detection count = 58, unique truth count = 35 

Perodua_Ativa_H     = 90.00%(ap)        tp =8 fp  =0

Proton_X50	= 93.04%(ap)	tp = 9 fp =8

proton_x70	= 85.28%(ap)	tp = 6 fp =0

perodua_Aruz_1.5AV  =100%(ap)	          tp = 7 fp =1

Future development: More Dataset for further accuracy and training

Group members: Rose Neezam bin Rose Zaidi, Robinson Loh Ying Sheng ,Nor Sakinah binti Mohd Yusoff ,Nur Farah Syakila binti Selamat

References: https://medium.com/nerd-for-tech/yolov4-paper-summary-analysis-602dd584fa86

            https://github.com/AlexeyAB/darknet/ -for darknet
            
            https://github.com/theAIGuysCode/YOLOv4-Cloud-Tutorial -yolov4 on colab
