# Project S.A.F.E.

![Project Image](https://github.com/sarthakpurohit/Project-SAFE/blob/alpha/home_page.png)
---

### Table of Contents

- [Description](#description)
- [Details](#details)
- [License](#license)
- [Contributors](#contributors)


### Description

> During emergencies, when stranded in a traffic jam, what's the best possible help one can provide to those in dire need of help? There comes the situation where people can not be extricated from problematic situations as the emergency vehicles can not reach there on time.

> We have created a web portal where users signup and provide their vehicle and contact details. Our Project S.A.F.E is aimed at providing the best and nearest possible help to the stranded emergency vehicles by detecting through cameras installed on roads, the traffic and emergency vehicles. If the image captured  is classified as being in an emergency, the camera captures a picture of the number plate. The text is extracted and sent to the nearest possible help. At the time of the disaster our drones and cameras will capture pics of the vehicles on road and send it to our server.

---

## Details
> ### Classifier: 
>   The CNN classifier for classifying Emergency Vehicles and Non-Emergency Vehicles was trained using transfer-learning on pre-trined resnet50. Finally after training, the model attained almost 94% accuracy. Saved model can be found at (https://drive.google.com/drive/folders/1gyJQaO7AUsfyEBrIJ7jd8PQxlCDBEEFp?usp=sharing)
>    For inference, the given image is first converted to 224 * 224 shape and normalized before feeding to model.

>   (a) Why resnet?
>        - Although there were other choices like VGG and Alexnet, resnet takes comparatively less memory space. Inference time of resnet is low. Also, resnet takes lesser number of epochs to attain desirable accuracy.
>     (b) Why resnet-50?
>        - While other options like resnet-34, resnet-101 were available. There is a trade-off between model size and (training time & inference time). So, resnet-50 appeared to be a good choice for our task.

> ### Number Plate Extraction:
> OpenCV and PyTesseract have been used for this purpose.

> The images are fed to the model which converts it to gray scale, blurs it out and eventually, edges are highlighted. Contours are drawn to extract the highlighted features.

> A bounding rectangle is then drawn around the highlighted number plates, subsequently being passed on to another png file.

> Using pytesseract, the text on the number plate is extracted and sent to the database.

> ### Website:

>The website is made using the basic technologies like HTML and CSS being used for the front end section along with JavaScript for certain animations . This site contains a home page which provides the basic knowledge about us and what our project aims at. A login/signup page where the users are supposed to fill their personal and their vehicle's details correctly. Then these details are sent to the backend section of our website where the user collection stores all the data of the user and presents it back when the user logs in into his/her account. The admin page, for now, (as the deployment is not complete) just shows the images of vehicles that are to be classified into emergency/non emergency type.

> ### Technologies

>- PyTorch
>- OpenCV
>- HTML
>- CSS
>- NodeJS
>- Flask
>- MongoDB
---


> ### Contributors

>- Ritvick V. Pandey - (https://github.com/Ritvick-me)
>- Devangi Purkayastha - (https://github.com/devangi2000)
>- Sarthak Purohit - (https://github.com/sarthakpurohit)
>- Shubham Saxena - (https://github.com/shubhamsaxena1810)

---

> ## Contribute 👨‍👨‍👧‍👦
> Thanks for taking the time to contribute!

> The following is a set of guidelines for contributing to Project S.A.F.E. Use your best judgement and feel free to propose changes to this document in a pull request.

> If you have any questions, open an issue.

---

> ### Issue 

> Ensure the bug was not already reported by searching on GitHub under issues. If you're unable to find an open issue addressing the bug, open a new issue.

> Write detailed information. Detailed information is very helpful to understand an issue.

---

> ### Pull Requests

> Pull Requests are always welcome.

---

> ## License

> MIT © HACKOS

> This project is licensed under the MIT License 
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

<p align="center">
	Made with :heart: by <a href="https://github.com/devangi2000">HACKOS</a>
</p>

