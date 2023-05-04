# Documentation to setup Jenkins CICD pipeline for this Application

## Clone the repository

- Run the following command to clone the repository:

```sh
git clone https://github.com/HelloRitul/node-todo-cicd.git
```
## Setting up webhooks

- Go to your GitHub repository and click on the "Settings" tab.


![Screenshot 2023-05-04 133256](https://user-images.githubusercontent.com/69754757/236193552-dd431a97-e736-4d84-b8fe-b1717bcd58ba.png)


- Click on the "Webhooks" option in the left sidebar.

![Screenshot 2023-05-04 171354](https://user-images.githubusercontent.com/69754757/236194424-a2703eec-955e-4c26-aa6c-6fa798796429.png)

- Click on the "Add webhook" button to save the webhook.

![Screenshot 2023-05-04 171538](https://user-images.githubusercontent.com/69754757/236194597-6fa8d2d0-87f8-41f0-8190-73c686e9021c.png)

- Download and install Jenkins on your server or local machine.

[Read my blog >>](https://ritul.hashnode.dev/day-24-task-complete-jenkins-cicd-project)

- Setup jenkins server by installing dependencies
```sh
sudo apt  install docker.io
```
```sh
sudo apt  install docker-compose
```
```sh
sudo usermod -aG docker $USER
```
```sh
sudo usermod -aG docker jenkins
```
```sh
sudo reboot
```

- Open Jenkins in your web browser and create a new pipeline job.
