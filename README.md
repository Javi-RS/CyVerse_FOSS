# CyVerse_FOSS 2021 Capstone Project
____
Team F (Wednesday) components:

  - Charlie Li
  - Chai-Shian Kua
  - Kyle Johnsen
  - Julia Piaskowski
  - Farah Saeed
  - Ferris Saad
  - Javier Rodriguez Sanchez
____

This repository contains the files used to containerize a web app developed as the capstone project for the 
CyVerse Foundations of Open Science Skills 2021 workshop. 
(https://learning.cyverse.org/projects/cyverse-foss/en/latest/index.html)

This web app uses Flask and gunicorn to run a SVM pixel classifier to estimate cotton yield from 2D images.
The image uses the Docker image taxfix/opencv-python (https://hub.docker.com/r/taxfix/opencv-python) as the 
base image. The additional required libraries to run the web app are installed automatically.

## Running the container

The Docker image is stored in the repository javirodsan/foss21_team_f_wed on Docker Hub. After logging into 
CyVerse Atmosphere and installing Docker (Instructions on how to install Docker in Atmosphere can be found here: 
https://learning.cyverse.org/projects/foss-2020/en/latest/Containers/dockerintro.html), you can download the 
image to your local machine by pulling it from the remote repository:

```
docker pull javirodsan/foss21_team_f_wed:1.0
```

Or you can run it directly from the remote repository:

```
docker run -ti -p 8080:8080 javirodsan/foss21_team_f_wed:1.0
```
Note that this command also does a docker pull behind the scenes to download the image with latest tag. 

## Using the web app
You should be able to see the Flask application running on http://localhost:8080 or 127.0.0.1:8080

Select image analysis from the drop down menu and upload an image to analyze. Finally, click proess image to start the estimation of yield. Please be patient, the analysis can take a while.

____
# Find Us

* [GitHub](https://github.com/Javi-RS)

# Authors

* **Javier Rodriguez** - *Graduate Research Assistant* - [BSAIL Lab (The University of Georgia)](https://bsail.engr.uga.edu/)

See also the list of [contributors](https://github.com/your/repository/contributors) who 
participated in this project.

# License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
