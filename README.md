# flask-on-docker3

This repo enables you to create a web service where you can upload a static or media(e.g. image or gif) and open it in another link. This repo contains the relevant folders and files relating to Flask, Docker, and Postgres that enable the aforementioned web service to function. Below is a gif showing the final process of uploading:  

![alt text](https://github.com/Bazzer218/flask-on-docker3/blob/master/video2.gif)

In order to bring the services up, do the following:

1. SSH into your remote server and enable port forwarding 

2. Clone this repo onto the server you are using

3. Follow the docker commands below:

```
$docker-compose down -v
```
```
$docker-compose -f docker-compose.prod.yml up -d --build
```
```
$docker-compose -f docker-compose.prod.yml exec web python manage.py create_db
```

4. Go to a web browser and upload an image at http://localhost:7676/upload

5. View the image at http://localhost:7676/media/IMAGE_NAME
