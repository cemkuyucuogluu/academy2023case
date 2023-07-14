
## Python Application with Docker

Running app.py using docker container technology

## Usage/Examples

```shell
git clone https://github.com/cemkuyucuogluu/academy2023case.git
cd academy2023case
```
## Run Locally

#For Dockerfile on the Vscode
```shell
FROM python:alpine 
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt 
EXPOSE 5000
CMD python ./app.py
```

## Build for Image

```shell
docker image build -t cemkuyucuoglu/akademi2023 .
docker image ls 
docker container run --rm -d -p 80:5000 cemkuyucuoglu/akademi2023
```

## Push to Files for Github

```shell
git init
git add .
git commit -m 'first commit'
git branch -M master
git remote add origin https://github.com/cemkuyucuogluu/academy2023case.git
git push -u origin master 
```

## Push to Image for Docker Hub

```shell
docker login
docker image tag cemkuyucuoglu/akademi2023:latest cemkuyucuogluu/akademi2023:latest
docker image ls 
docker image push cemkuyucuogluu/akademi2023:latest
docker image ls
```
## Check 

```shell
docker container run --name deneme -d -p 80:5000 cemkuyucuogluu/akademi2023:latest
docker container ps 
```
```
http://127.0.0.1/
```

## Resources

[Docker] (https://www.docker.com/)

[Docker Hub] (https://hub.docker.com/)

[Git] (https://git-scm.com/downloads)

[Github] (https://github.com/)

[Best Cloud For Me] (https://academy2023.bestcloudfor.me/)