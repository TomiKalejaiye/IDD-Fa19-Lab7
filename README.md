# Video Doorbell, Lab 7

*A lab report by Tomi Kalejaiye*

### In This Report

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**

[![HelloYou!](http://img.youtube.com/vi/NgBB2-zPii4/0.jpg)](https://www.youtube.com/watch?v=NgBB2-zPii4)

*Basic HelloYou sketch running.*

## Part B. Web Camera

**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)**

The original server (server.js) didn't make use of a web camera. In order to make use of one in pictureServer.js, an instance of NodeWebcam had to be created. Then, on a particular event, we can have the server capture a picture using the webcam.

**b. Include a video of your working video doorbell**

[![Video Doorbell](http://img.youtube.com/vi/1NpMzfzsZ6g/0.jpg)](https://www.youtube.com/watch?v=1NpMzfzsZ6g)

*Working basic video doorbell.*

## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**

I modified the simple video doorbell to add a ringing sound when the button is pressed. My original idea was a bit more ambitious. First of all, I wanted increase the size and quality of the photos taken on the webcam, and display them fullscreen on the web browser. However I found that changing the size parameters for creating the webcam instance actually had no effect on the size of the images taken. In fact, the values used in the default script are not the dimensions of the photo it actually takes. The default values are 1280x720, but the photos are all 640x480. Secondly, I wanted to use OpenCV to detect faces on the webcam photos, but considering the limited resources of the Pi, I decided against it. Ultimately of my desired features, the one I was able to implement was a ringing sound for the doorbell. I added a doorbell ring mp3 file to the public folder, included it in the html, and had the client play the file when the doorbell button was pushed. 

**b. Upload a video of your working modified project**

[![Video Doorbell](http://img.youtube.com/vi/7t3kQw1YWbQ/0.jpg)](https://www.youtube.com/watch?v=7t3kQw1YWbQ)

*Video doorbell with ring!*
