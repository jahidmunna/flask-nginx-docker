# Load Balancing Using Nginx in Docker and Flask

## Directory Structure
```
.
├── App
│   ├── requirements.txt
│   ├── Dockerfile
│   └── app.py
├── nginx.conf
├── docker-compose.yml
└── README.md
```

## Setup (create network)
```bash
docker network create my_network_v1
```


## Execution Command:
```bash
docker-compose up -d --build --scale app=3
```

*repalce 3 with the desire num of instance of the app service*

## Checking Command:
```bash
http://localhost
```
*You can see that, every time it loads ui from different service, thus load balancing is ensured*

## Shutdown Command:
```bash
docker-compose down
```
