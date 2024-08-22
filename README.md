# robintptsai / ravenclw_restreamer

## How to install and run Restreamer app on a local environment


### Preparation

1.Environment
- Mac OS 13.6.7 or newer
- CPU: Intel Core i5 or higher
- Memory: 16G (for app consume))
- Disk: 10G or higher (for app consume)

2.Tools
- Docker: 4.16.2 or higher
- iTerm (recommend)

### Deploy/Install

Steps to install app: Restreamer

1.create file directory for app
```
mkdir /tmp/data
mkdir /tmp/config
```

2.download app image
```
docker pull datarhei/restreamer:latest
```

3.install app
```
sudo docker run  --rm --name restreamer \
  -v /tmp/config:/opt/restreamer/config \
  -v /tmp/data:/opt/restreamer/data \
  -p 8080:8080 -p 8181:8181 \
  -p 1935:1935 -p 1936:1936 \
  -p 6000:6000/udp \
  datarhei/restreamer:latest
```

### Run and Use

1.Open http://localhost:8080/ui/ from browser
2.Create a user account (at the first time login)
3.Login to Restreamer
4.Use


# Reference
https://docs.datarhei.com/restreamer/getting-started/quick-start


