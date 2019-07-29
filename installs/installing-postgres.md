External resources:

- https://dev.to/nabbisen/installing-postgresql-11-2-server-on-openbsd-6-5-4oh9
- https://wiki.archlinux.org/index.php/Gitea#PostgreSQL

```sh
# Install postgres
pkg_add postgresql-server

# Init database
cd /var/postgresql/
doas su _postgresql
initdb -D /var/postgresql/data/ -U postgres --auth=scram-sha-256 --pwprompt --encoding=UTF-8 --no-locale

# Start database
pg_ctl -D /var/postgresql/data/ -l logfile start
```

Creating a database for a given user.

```sh
createuser -P $USER
createdb -O $USER $USER
```
