# Face Recognition.  

IBM Watson Visual Recognition understands the contents of images. Analyze images for scenes, objects, faces, colors, food, text, explicit content and other subjects that can give you insights into your visual content.  

We use PIR Sensor for detection and recognition is carried out by IBM Watson, which can be embedded in Node Red. The Node Red configuration is shown below:  

![1](https://user-images.githubusercontent.com/39903083/41078737-261f8c84-6a3c-11e8-9a19-c611f5b1bd9e.png)  
 
Refer: http://www.instructables.com/id/Face-Detection-Security-System-Using-Pi-Node-red-I/.  

As the primary step check if all the necessary nodes, including Node-watson is installed.  

According to the algorithm, corresponding to every image, identification is done to check whether it contains a person among the classified objects. In any case, a snapshot is taken. Whenever a face is detected, an email is sent with the subject “Someone has arrived”. Whenever a moving object other than a face is detected, an email is sent with the subject “Activity is detected”. In both cases an audio is played with the corresponding content, for this text to speech conversion is used. 

After the configuration is done, choose “**deploy**”.  

The email received is shown below:  

![2](https://user-images.githubusercontent.com/39903083/41078756-4a205000-6a3c-11e8-8f10-0038a18f61e8.png)  

The specifications of detected face are:  


![1](https://user-images.githubusercontent.com/39903083/41078788-6f12c53c-6a3c-11e8-8ceb-ae847cbbaf8b.png)

A welcome note can be played based on time. The node red flow is as follows:  

![screenshot 35](https://user-images.githubusercontent.com/39903083/41078807-83e5fb5a-6a3c-11e8-8578-2fb68a53f654.png)  
 
The information obtained after analyzing (or classifying) the detected images can be stored into cloudant NoSQL database in IBM Watson.  

![1](https://user-images.githubusercontent.com/39903083/41078828-a3433f58-6a3c-11e8-8eb6-2dda2062edaf.png)  
 
Here, create a new database “**faces**” to store the information after analysis.  

![2](https://user-images.githubusercontent.com/39903083/41078829-a37829ac-6a3c-11e8-9b5d-4b2cb5494977.png)  


![1](https://user-images.githubusercontent.com/39903083/41078871-d9bcba64-6a3c-11e8-94c8-377d76b16ddb.png)  

The email sent also contains the snapshot captured by the IP Webcam. The project can be further extended by storing the faces detected into a database. Matching with the database can be done, to identify a visitor who visits repeatedly.  

## Flow clipboard is given in this repository.
