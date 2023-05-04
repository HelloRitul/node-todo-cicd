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

[Read my blog >>](https://ritul.hashnode.dev/day-22-getting-started-with-jenkins)

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

- Open Jenkins in your web browser and create a new freestyle project.

![Screenshot 2023-05-04 172324](https://user-images.githubusercontent.com/69754757/236196317-8f95aec6-574e-40f6-86f3-956842268ca3.png)

![Screenshot 2023-05-04 172427](https://user-images.githubusercontent.com/69754757/236196469-4bb6d97e-3024-42bf-a810-144df5f6b350.png)

- Configure the pipeline job to use the GitHub repository that you cloned earlier.

![Screenshot 2023-05-04 172633](https://user-images.githubusercontent.com/69754757/236196895-3b47b412-6a09-4cd3-9762-1b08f19c8fb3.png)

![Screenshot 2023-05-04 172722](https://user-images.githubusercontent.com/69754757/236197058-2e4050fd-efc1-4d03-98e8-421cd26d7bb2.png)

- Configure and select “GitHub hook trigger”

![Screenshot 2023-05-04 172859](https://user-images.githubusercontent.com/69754757/236197414-0c74d541-18d0-4e88-bebc-8217808139d7.png)

- Build Code through docker

![Screenshot 2023-05-04 174602](https://user-images.githubusercontent.com/69754757/236201122-9863a3fa-1010-4478-8b0c-b0b1bb830348.png)

- Make any changes in the GitHub repo and edit any header file. The job will run automatically and changes will be made.

![Screenshot 2023-05-04 174751](https://user-images.githubusercontent.com/69754757/236201495-5d411572-e9ee-4f9a-89f6-f79f6a9de2ca.png)

## Deploying the application

![Screenshot 2023-05-04 174831](https://user-images.githubusercontent.com/69754757/236201669-923fc662-730f-41d5-bf2c-1b4062c9b4c5.png)

## Open the particular IP on which it is hosted. It will be up and running.

![Screenshot 2023-05-04 175124](https://user-images.githubusercontent.com/69754757/236202417-5858ebd1-bc7f-487b-b7b6-c307cb9fc0f3.png)

## That's it! You now have a fully automated CI/CD pipeline that deploys your application whenever there is a new commit to your repository.
