# Setting up Immich in Docker
1. Create the folder path for Immich and fetch the official `docker-compose.yml` and default `.env` files:
```
mkdir -p ~/immich-app && cd ~/immich-app
wget -O docker-compose.yml https://github.com/immich-app/immich/releases/latest/download/docker-compose.yml
wget -O .env https://github.com/immich-app/immich/releases/latest/download/example.env
```

2. Open the `.env` file with preferred editor.
```
nano ~/immich-app/.env
```

3. Replace `DB_PASSWORD` and `DB_USERNAME` with preferred credentials, proceed to quit and save.

4. Open the 'docker-compose.yml' file with the preferred editor.
```
nano ~/immich-app/docker-compose.yml
```

5. Set every `restart: always` to `restart: unless-stopped`, proceed to quit and save.

6. Run Docker Compose in detached mode: 
```
docker compose up -d
```

7. Click [here](http://localhost:2283) and follow the on-screen prompts to register the Admin Account.