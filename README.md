# chat-app
The Chat Application with Automated CI/CD enables real-time messaging between users while ensuring smooth, automated development and deployment workflows. The project includes:  Core Features: User authentication, messaging, notifications, and media sharing. 
Configuring the repo for the first time and running the application
Docker
To be able to run this project you will need Docker Desktop installed on your computer. Docker installation instructions: https://www.docker.com/products/docker-desktop/

The instructions below will allow you to run this project on your local computer using docker-compose

Run the following command in the terminal to download a copy of the repo to your local machine
  git clone https://github.com/adrianhuber17/chat-app.git
Navigate into the new sub-folder created called chat-app.
After the project repo is downloaded navigate into the project directory
  cd chat-app
Manually open Docker desktop or run the command below to open Docker
 open -a Docker
Once the Docker desktop is runnning, type the command below to create and start the container in detached mode and build the image
  docker-compose up -d --build
At this point the container with the app should be running in your local computer

Services are running on Port 3000 (front-end React), Port 5001 (back-end REST), Port 5004 (back-end WebSocket). Please make sure you have no other app running on these ports

Run the following command to create and reset the Messages table in the database.
This command can be used any time you want to delete and reset all the data in the database
docker-compose exec backend python manage.py reset_db
Open a browser to the local host http://localhost:3000/ and start enjoying the app
