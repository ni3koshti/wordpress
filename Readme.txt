
THis file provide information create wordpress setup using mysql from docker compose

Created docker-compose file that include
- mysql container details with require password and version
- wordpress container details with require password
- volume information
- port details that use to browse


execute 

1. create docker-compose.yml
2. check syntax using docker-compose config
3. if everything fine execute "docker-compose up -d" 
4. "docker ps" to check created containers
5. "docker-compose logs" to check logs
6. use browser http://localhost:<port>

how to stop

1. 'docker-compose down'
2. 'docker ps' to confirm 
