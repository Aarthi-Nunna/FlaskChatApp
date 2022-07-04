# FlaskChatApp

To do:

1. Work on localhost aspect of the chat application  
   Problem:  Since we are using localhost in our python chat app, there is some error in the mapping of that port with that of the docker container's port.
             Have to look into it further.
   
   
2. Download DockerHub on the desktop
3. Create an image and run it as a contatiner using Docker ( If 1 is figured out 2 is pretty much done)
   Create image using: docker build -t "name of image" .         => Run this inside the directory in which there is the Dockerfile and app.y
   To run the container: docker run "name of image"              => Additional port mapping if required (depends on 1 again)
4. Create a pipeline in Jenkins and use webhooks
5. Prepare the presentation 
6. Follow up on the date, time slot etc
July 8th ruled out for sure, 9th and 10th are weekends, 11th?
12th -> SSN has exam
CEG dates for Adithya?

From the Neueda Ppt they uploaded:
1. Set up a Jenkins project to build a Docker Image, run a container based on the image
2. Set up a pipeline to automate the build / test / deploy process 

