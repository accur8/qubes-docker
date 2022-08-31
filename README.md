# Configuration
- db.env
    - Set database user and password
- qubes.env
    - Set locus repository user and password
- volumes/config/config.json
    - Set base database user and password
    - Set hardcoded admin user's password

# Install in docker
- Run `docker compose up`
- Once qubes is running, press `Ctrl-C` to stop them
- Run `docker compose start` to run them in the background

# Dump Database
- If updates are made to the database, you can re-dump it, replacing qubes.sql.gz
- Run `pg_dump --host=localhost --port=5432 --username=qubes --no-privileges --no-owner --compress=9 --file qubes.sql.gz qubes`
