# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

A Django-based  notes app DevOps project on Jenkins declarative groovy pipeline deployed on  AWS ec2 instance. Continuous integration and continuous deployment are done, building a groovy syntax pipeline to automate and release the application. Docker is used to containerize the  app image and docker-compose to isolate the environment as it can be reproduced anywhere. GitHub  is used as source code management to store the code. 
-------------------------------------------
The following are the steps:

	Launch an Ec2 instance of t2.micro type and use the Ubuntu image.

![Django Notes-app-pipeline](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/41f1178f-fedb-436d-9ebd-e7fd1135cfca)

	Connect the server and update and install Docker, Java, and Jenkins.

![Django Notes-app-pipeline (1)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/3ea3d688-3475-4f1b-bf91-98e97edc88ad)

![Django Notes-app-pipeline (2)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/8fb71364-b6df-4c19-9dc6-4c183b26fdcf)

	Add docker to user group, user is ubuntu. 

![Django Notes-app-pipeline (3)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/1590aca4-928c-4658-992e-b3136c45f652)

	Add docker to user group so that Jenkins can use.

![Django Notes-app-pipeline (4)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/c8ec9737-bb3e-4872-b92c-e571c825ad56)

	Add  a new  pipeline item named as note-app-cicd-pipeline
	Hit check on Github project, and enter the URL of the Github repo.

![Django Notes-app-pipeline (5)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/df295ba3-7573-45d3-a8d9-e2654b5f43b0)

	In build trigger hit GitHub hook trigger GitScm polling.
![Django Notes-app-pipeline (6)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/60c4d0c3-7d0d-4f53-a5b5-a50a9c9f43e7)

	In pipeline choose pipeline script from SCM (Git) enter the URL and Brach of the repo and enter  declarative groovy pipeline script file in the Script path

![Django Notes-app-pipeline (7)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/4194b04c-f160-4a64-9eda-a8084692d9bb)

![Django Notes-app-pipeline (8)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/a2be9b4d-c46b-4bd3-be51-1de98e1c211e)

	Save and apply, Build the pipeline.

![Django Notes-app-pipeline (9)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/0d494e16-f607-4dab-9974-166e271076d8)

	You can see in your Docker-Hub account the new image is built.

![Django Notes-app-pipeline (10)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/7a82d251-5872-46cf-8d73-1d3da8e19f78)

	You can also check your terminal to run “Docker images” and “docker ps”
![Django Notes-app-pipeline (11)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/b4704c60-da35-49bf-9275-95ecf93d885e)

	Open the 8000 port of the instance and see the notes app.

![Django Notes-app-pipeline (12)](https://github.com/Tripti-TD/django-notes-app-DevOps/assets/128075759/a3bdf999-bb23-4336-96ea-afe140eefe6e)

Please excuse if something is missed.

------------------------------------------------------------------------
