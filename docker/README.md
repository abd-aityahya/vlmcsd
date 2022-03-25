# VLMCSD for Docker

Deploy vlmcsd service on Docker container

```bash
git clone https://github.com/abd-aityahya/vlmcsd.git vlmcsd
cd vlmcsd
cd docker

# Use docker-compose service
docker-compose up -d

# or docker build image
docker build -t vlmcsd .
docker run -idt -p 1700:1700 vlmcsd
```
