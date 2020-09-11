# ghost env.list

- A small file with env configuration variables used to pass into ghost when started as a docker file. 
- place this file in: /srv/ghost/
- This example enables Amazon SES as an email send service. Have your IAM credentials at hand and check the location of the service you are using. The example shows Ireland


## to start docker ghost without env.list variables
```
docker run -dit --name ghost_3.31.5 -p 2368:2368 -v ghost-content:/var/lib/ghost/content ghost:latest
```

 
## Start Docker Ghost with en.list variable
```
docker run -dit --name ghost_3.31.5 -p 2368:2368 -v ghost-content:/var/lib/ghost/content --env-file /srv/ghost/env.list ghost:latest
```

