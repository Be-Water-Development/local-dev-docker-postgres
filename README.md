# Local Dev

This project is the template for Docker + Postgres local dev enviorment for all clients and apps.

### Prerequisite Steps

Install Docker from: 
https://docs.docker.com/desktop/install/mac-install/

TablePlus download from:
https://tableplus.com/download

### Spin Up Enviorment

From within the root dir, run `docker compose up`\
Terminal should log `database system is ready to accept connections` as final output

### Connect TablePlus (postgres client) to docker image running postgres

Use port: `5432`\
Username: `postgres`\
Password: `postgres`

Hit button `Connect`

### Seeding Data

In dir `db` there are two SQL files; init and seed \
In the SQL tab of TablePlus, run `init.sql` -- you should see a Quote table created \
Next, run the contents of the Quote seed file in TablePlus client -- the table should be populated with data.
... this is all unnecessary though as you can just run mirations from the BE repo to set up this same db with zero data.

#### Thats it, you now have docker running a local image of postgres whose volume contains one table and seed rows and TablePlus is wired up for easy interaction.