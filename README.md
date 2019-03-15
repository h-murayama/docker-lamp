# docker-lamp

## How to use

```bash
git clone https://github.com/h-murayama/docker-lamp.git
cd docker-lamp/
docker-compose up -d
```
After, please access to 127.0.0.1 from browser.

## Access to Container MySQL from host machine
```mysql
mysql -u root -p -h 127.0.0.1 --port 3333
```

## Command collection

Image confirmation
```
sudo docker images
```


Container's ID confirmation
```
sudo docker ps
```


First start 
```
# foreground
docker-compose up

# background
docker-compose up -d
```

Stop
```
# foreground
##Ctr + C

# background
docker-compose stop
```

Restart or Reflection of Dockerfile
```
#foreground
docker-compose up

#background
docker-compose restart
```

Container rebuild　（Reflection of docker-compose.yml）
```
#foreground
docker-compose up

#background
docker-compose up -d
```


Dockerfile or Build reflection
```
# foreground
docker-compose up --build

# background
docker-compose up -d --build
```

Look of logs.
Output of background building logs.
```
# Last 5 line
docker-compose logs -f --tail="5"

# Last 5 line with timestamp
docker-compose logs -f --tail="5" -t
```

Stop container
```
docker stop <containerID or name>
```

Cleaning
```
# stop and remove （container, network）
docker-compose down

# stop and remove （container, network, image）
docker-compose down --rmi all

# stop and remove （container, network, volume）
docker-compose down -v
```
