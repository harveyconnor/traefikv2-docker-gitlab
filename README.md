# Gitlab Trafik v2 Docker Lets Encrypt
This is a repository that allows you to setup gitlab with lets encrypt using Traefik v2 and Docker.

## Installation
1.  Firstly you need to configure the environmental variables found within each sub folders.
    These can be found in `./traefik` and `./gitlab` as .example.env. Please move them to .env
2. Once you have configured the files you can use:
```
docker-compose up -d
```
in each of the sub folders, traefik and gitlab.
3. Use `docker ps` and `docker logs traefik` / `docker logs gitlab` to see if they are functioning correctly.

4. Once gitlab has started running, you'll need to edit the runner key in the script file. If you wish to not use a runner, please remove the runner from the compose file or comment the code out.

Gitlab usually takes a few minutes to start up but the best way to get started is o focus on getting Traefik up and running.

Please note that these compose files are not fully fledged products aimed for production, please use them to your liking and customise each of them to make sure you're happy with their operations.
