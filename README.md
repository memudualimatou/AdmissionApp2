## DEEPSTACK-UI

DeepStack-UI is a UI web application powered by Deepstack. It is designed to run on docker container and uses the user-friendly designed web application for object detection or
face detection from uploaded images.
This web app provides the advantages to manipulate the images as the user wishes by providing the 
necessity to do so, it allows the user to select a specific section of the image on which his/her desired objects will be extracted, filter
the object detected by their confidence and provides the power to select the object the user desired to detect.



## TECHONLOGY USED

* [DeepStack](https://docs.deepstack.cc/)

* [Streamlit](https://docs.streamlit.io/en/stable/)

* [DeepStack-UI](https://github.com/robmarkcole/deepstack-ui)


## INSTALLATION

To run Deepstack-ui for object detection, two major steps must be followed accordingly:


### 1-Deepstack Installation on Docker
To install Deeptsack you need to run the command below 
```
docker run -e VISION-DETECTION=True -p 80:5000 deepquestai/deepstack:latest
```

### 2-DeepStack-UI Installation
Deepstack-ui can be run through two ways:

#### Solution1:
From the root dir, build the deepstack-ui container from source and then run the UI, passing the DEEPSTACK_IP environment variable:

     docker pull robmarkcole/deepstack-ui:latest

     docker run -p 8501:8501 -e DEEPSTACK_IP='192.168.1.133' deepstack-ui

- DEEPSTACK_IP : the IP address of your deepstack instance, default "localhost"

To check this IP address:
- Open PowerShell and run the command below
```
Get-NetIPAddress -AddressFamily IPV4
```
- Then copy the first IP Address in the result
- Use the IP address to replace “localhost” in your DeepStack UI command

The UI is now viewable at http://localhost:8501

#### Solution2:

   * Clone the deepstack_ui repository
	
   * Open Powershell or CMD in the repository folder and run pip install -r requirements.txt

   * Go to this folder on your laptop
 		``` C:\Users\<your-laptop-username>\.streamlit and delete the file config.toml ```
	
   * Run the command streamlit run app/deepstack-ui.py to start the deepsack-ui application


Now, the UI is available at http://localhost:8501


## HOW THE DEEPSTACK-UI WORKS?

This system accepts an image as input and outputs a couple of elements xplained below:


1. **IMAGE INSERTION**:
<br>

![capture1](https://github.com/memudualimatou/STUDENT-ATTENDANCE-USING-FACIAL-RECOGNITION-SYSTEM-OPENCV/blob/master/Docs/Images/Capture12.PNG)

![capture](https://github.com/memudualimatou/STUDENT-ATTENDANCE-USING-FACIAL-RECOGNITION-SYSTEM-OPENCV/blob/master/Docs/Images/Capture12.PNG)











