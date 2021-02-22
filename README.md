

 # Simple Flask App - Docker 

 Simple app build on Python Flask. 

 
 ## Aplication Structure 

 ```
 .
├── app
│   ├── requirements.txt
│   └── src
│       ├── server.py
│       └── templates
│           └── index.html
├── docker-compose
│   ├── docker-compose-dev.yml
│   └── docker-compose.yml
├── Dockerfile
├── dockerfile-dev
├── files
│   └── index.html
└── README.md

``` 

## Folders

| Folder  | Description |
| ------------- | ------------- |
| [app](app) | Flask Application Code. |
| [docker-compose](docker-compose)  | docker-compose files  |
| [files](files)  | contains static files for test purposes |





## Prerequisites 

* Linux Server 

* Python3.8

* Python pip


## Usage

Clone Repository:

```bash 
git clone https://github.com/betulakman/docker_app.git
```

Change working directory:
``` bash
cd docker_app
```

Install requirements

```bash
pip3 install -r app/requirements.txt
```

Run Application:

```bash
python3.8 app/src/server.py
```


## Docker Image Build

Build Image
```bash
docker image build -t <your-tag>  . 
```

Push Image 
```bash 
docker image push <your-tag>
```

## Run Docker Container

Run Container
```bash
docker container run -d --name sampleapp  -p <hostport>:5000  <docker-image>
```

## Docker-Compose

Change Directory
```
cd docker-compose
```

* Note:  Modify docker-compose.yml file(optional)

Build image and Run Container
```
docker-compose up -d --build
```

