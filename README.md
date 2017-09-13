# simpleDockerElm
DockerFile with sample elm file


Steps to build and run this docker image:

1. Install Docker for your operating system in use: https://docs.docker.com/engine/installation/
2. Test docker installation on your terminal/CMD with the following command: docker --version
3. Once docker is validated, go to your directory of choice and run this: 
git clone https://github.com/binyata/simpleDockerElm.git
4. Change directory into this newly created directory:
cd simpleDockerElm
5. Your DockerFile will build your image, you can change whatever you need in that file if you want to modify your image. Run the following command to build your docker image:
docker build -t <name of your image> .
6. This will go through a step list of commands that is contained within the DockerFile.
7. Validate that the image was correctly made:
docker images
8. Your image name should bbe on the list of images.
9. Now that your image is up, now build a container out of the image:
docker run -d -p 8000:8000 <name of your image>
10. The -d argument will run as a background process and -p will forward your port from your docker container to your host machine.
11. Validate that the container is up and running:
docker container ls
12. Under name should be your image name and the container ID.
13. Go to your browser and enter http://localhost:8000
14. This should display your elm homepage and a Hello.elm file.
15. Click the Hello.elm file
16. You will see a simple text appear on the page