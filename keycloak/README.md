## Postgres / pgAdmin
### PgAdmin
http://localhost:5050

- Login: admin@admin.com:ASDqwe123!@#
- add server:
  - Host: postgres_container
  - Port: 5432 
  - Credentials: postgres:ASDqwe123!@#


## Keycloak / Postgres / Redis
http://localhost:8180
- Login (as keycloak administrator): user:bitnami

realm: rpg-services
- client: rpg-ui
    - Valid Redirect URIs: http://localhost:3000/*
    - Web Origins: *

- client: rpg-api
  - Access Type: bearer-only
  
- roles:
    - ADMIN
    - USER
- users: (Temporary: OFF )
    - admin1: ASDqwe123!@#
        - roles: USER, MANAGER
    - user1: ASDqwe123!@#
        - roles: USER