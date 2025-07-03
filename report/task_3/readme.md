#  Vulnerability Scan – Summary

##  Tool Used
- Greenbone Vulnerability Manager (OpenVAS)
 - Downloaded official Greenbone Docker Compose file
 
 ```bash
 mkdir ~/greenbone && cd ~/greenbone
 curl -s -L https://greenbone.github.io/docs/latest/_static/docker-compose-22.4.yml -o docker-compose.yml
 ```
 - Launched GVM stack containers(Deployed via Docker)
 ```bash
 docker compose -f docker-compose.yml -p greenbone-community-edition up -d
 ```
 - Monitored logs during feed sync and initialization
 ```bash
 docker compose -f docker-compose.yml logs -f
 ```

### Accessed web UI at https://localhost:9392 with default credentials (admin / admin).

## Target
- Localhost: 127.0.0.1

## Report File
- Full analysis is in analysis.md

## Screenshots 
- Located in screenshots/ 

---