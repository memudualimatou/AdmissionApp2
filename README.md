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



<br>

![capture1](https://github.com/memudualimatou/AdmissionApp2/blob/main/image1.jpg)

<br>
This is the landing page of deepstqck-ui. It is composed of two sections, the parameter section constructed to manipulate the image as wished and the main page which displayed
the results. 

The parameter is composed of 3 parts:
1. **Confidence**  : this is used to set the treshold of the each object prediction percentage (confidence).
2. **ROI** : the Region of Interest is used to select a specific part of the image on ehich the detection will run
3. **Object Selection** : This is allows the user to choose the type of object to extract in the image.

![capture](https://github.com/memudualimatou/AdmissionApp2/blob/main/Capture002.PNG)

<br>
The main page outputs four elements which are:

1. **Processed Image** : This image is composed of all object detected, bordered with their respective label
2. **All discovered objects** : A list of all object detected
3. **Filtered object count** : A list of the objects and their number of occurance.
4. **All filtered objects** : A list of dictionaries where each dictionary consict of each object's confidence value, name and location details.


![capture](https://github.com/memudualimatou/AdmissionApp2/blob/main/Capture996.PNG)


<br>

After intersing an image:

![capture](https://github.com/memudualimatou/AdmissionApp2/blob/main/Capture777.PNG)



<br>
## DEEPSTACK-UI DEMO

![capture](https://github.com/memudualimatou/AdmissionApp2/blob/main/gif1.gif)







