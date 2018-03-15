# docker

Some base-images for running python3 and Flask

## build:
docker run -ti -v /c/Users/git/wx-admin:/code -p 5000:5000 flask:v0 bash

pip install -r requirements.txt
docker commit <hash> wxadmin:v0
docker run -ti -v /c/Users/git/wx-admin:/code -p 5000:5000 flask:v0 bash
gunicorn manage:app -b 0.0.0.0:5000
> or python3 manage.py runserver -h 0.0.0.0
  
> if using minikube:
minikube.exe ip
> will show like: http://192.168.99.100

Then in host, open Web browser: http://192.168.99.100:5000/ 

> save env.
docker commit <hash> wxadmin:v0
docker run -ti -v /c/Users/git/wx-admin:/code -p 5000:5000 wxadmin:v0 python3 manage.py runserver -h 0.0.0.0  
