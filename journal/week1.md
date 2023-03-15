# Week 1 — App Containerization
This week we're going to talk about App Containerization. But before that, I want to discuss about Docker Containers and their best practices.

A container is a lightweight, standalone, and executable package of software that includes everything needed to run an application, including the code, runtime, system tools, libraries, and settings. Containers are designed to be portable, scalable, and easily deployable, and are commonly used in cloud computing environments and DevOps workflows.

Docker containers are a popular technology used for deploying and managing applications in a portable and efficient manner. Here are some best practices for working with Docker containers:

-> Keep your containers lightweight: Try to keep your containers as lightweight as possible by only including the necessary components and dependencies.

-> Use official images: Use official images from Docker Hub or other reputable sources to ensure that the images are well-maintained and secure.

-> Use a single process per container: Each container should only run a single process or service to ensure that it is easy to manage and scale.

-> Use environment variables: Use environment variables to store configuration settings and secrets rather than hard-coding them in your Dockerfile or container.

-> Use volumes to store data: Use Docker volumes to store data that needs to persist between container restarts or that needs to be shared between containers.

-> Use Docker Compose for multi-container applications: Use Docker Compose to manage multi-container applications and simplify the deployment and management of interconnected services.

-> Regularly update your containers: Regularly update your containers and base images to ensure that they are running the latest security patches and bug fixes.

-> Monitor your containers: Set up monitoring and logging for your containers to help identify and troubleshoot issues quickly.

By following these best practices, you can ensure that your Docker containers are efficient, secure, and easy to manage.


Now, let's go to the homework to be completed for week-1

## Homework Required

## Attended Live Session 

Here we got to know about the working of **Guest OS, Host OS and the Containers**. We also **created a Docker file** in this instructional live video. Also ran some of the **Python scripts**. Experienced the guidance from the Docker experts : ***James Spurin*** and ***Edith Puclla***. Installed the Docker Extension in Gitpod, and understood the working of code in Dockerfile. And the entire playlist is here : https://www.youtube.com/watch?v=8b8SvQHc4Pk&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&ab_channel=ExamPro

### Video Review

* Watched [How to Ask for Technical Help](https://youtu.be/tDPqmwKMP7Y) video.
* Watched [Grading Homework Summaries](https://youtu.be/FKAScachFgk) video.
* Watched [Week 1 Live Streamed Video](https://www.youtube.com/live/zJnNe5Nv4tE?feature=share) during the livestream and followed along with the tasks.
* Watched [Commit Your Code](https://youtu.be/b-idMgFFcpg) video.
* Watched [Chirag's Week 1 Spend Consideration](https://youtu.be/OAMHu1NiYoI) video.
* Watched [Ashish's Week 1 Security Consideration](https://youtu.be/OjZz4D0B-cA) video.
* Watched [Week 1 - Create the notification feature (Backend and Front)](https://youtu.be/k-_o0cCpksk) video.
  * The hardcoded confirmation code when registering an account with Cruddur is '1234'.
  * [OpenAPI Specification v3.1.0](https://spec.openapis.org/oas/v3.1.0)

## Tasks Completed
## #1 Launched Gitpod and Implemented Notifications.

We built an image via Gitpod. **Launched the micro blogging app - Cruddur on a localhost**. For this we created `frontend-react-js` file and a `backend-flask` file which were connected. There was a `docker-compose.yml` file which included both frontend and backend file's links. We need to **compose up** to activate the ports that helped us to run the Cruddur app. The `port 4567` was for the backend and the `port 3000` was for the frontend.

Then, we set the notifications feature in this cruddur app.

 ## #2 Installed DynamoDB on Gitpod

 Installed and ran DynamoDB via Gitpod and **created a table "Music"**. 

Went through [video](https://youtu.be/CbQNMaa6zTg) steps to set up PostgreSQL and DynamoDB Local

  * Ran DynamoDB Local container to ensure it worked
  * Ran Postgres container to ensure it worked  
  * [AWS Documentation - DynamoDB Local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.DownloadingAndRunning.html)

  * Tested connecting to DynamoDB Local using ```aws dynamodb list-tables --endpoint-url http://localhost:8000``` which returned empty table info successfully.

 ## #3 Installed Postgres

  * Added steps to install PostgreSQL Client into [.gitpod.Dockerfile](../.gitpod.Dockerfile) and tested using ```psql -h localhost -p 5432 -U postgres -d postgres```

 ## #4 Spending Considerations for week-1
 
 It was good and helped to know that this Gitpod charges you on an horuly basis per month. If your workspace is open more than 50 hours in a month it will charge you. As 50 hours/month is in the free-teir. To avoid unwanted use we can also **stop the gitod workspace** when not in use. **Attended the Pricing Quiz** which was damn easy as I already had watched Chirag's video that covered all of the conent. 
  
**Watch this video by Chirag for more details  :** https://www.youtube.com/watch?v=OAMHu1NiYoI&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=24 
 
 
 ## #5 Security Considerations for week-1
In this lecture he taught about Snyk, Clair, AWS Secrete manager that helps in managing the security and detecting the vulnerabilities in are conatiner/code. 
Also helped me to solve the Security Quiz.

**Watch this video by Ashish for more details :** https://www.youtube.com/watch?v=OjZz4D0B-cA&list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv&index=25



## Summary

| Homework      | Completed     | Not Completed  |
| ------------- |:-------------:| -----:|
| Watched Week 1 - Live Streamed Video   | ✔ |  |
|Watched Chirag's Week 1 - Spend Considerations   | ✔     |    |
| Watched Ashish's Week 1 - Security Considerations | ✔      |   
|Containerize Application (Dockerfiles, Docker Compose)|✔      |   |
|Document the Notification Endpoint for the OpenAI Document| ✔      |   |
|Write a Flask Backend Endpoint for Notifications | ✔   |   |
|Write a React Page for Notifications |✔      |   |
|Run DynamoDB Local Container and ensure it works	| ✔   |   |
|Run Postgres Container and ensure it works | ✔      |   |