Exercise2_6# docker-compose up
Starting exercise2-6-postgres_server ... done
Starting exercise2-3-frontend        ... done
Starting exercise2-4-redis           ... done
Starting exercise2-3-backend         ... done
Attaching to exercise2-6-postgres_server, exercise2-3-frontend, exercise2-4-redis, exercise2-3-backend
exercise2-3-frontend           | INFO: Accepting connections at http://localhost:5000
exercise2-4-redis              | 1:C 21 Sep 2021 13:33:51.936 # oO0OoO0OoO0Oo Redis is starting oO0OoO0OoO0Oo
exercise2-4-redis              | 1:C 21 Sep 2021 13:33:51.940 # Redis version=6.2.5, bits=64, commit=00000000, modified=0, pid=1, just started
exercise2-4-redis              | 1:C 21 Sep 2021 13:33:51.940 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.941 * monotonic clock: POSIX clock_gettime
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * Running mode=standalone, port=6379.
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 # Server initialized
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * Loading RDB produced by version 6.2.5
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * RDB age 1792 seconds
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * RDB memory usage when created 0.77 Mb
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * DB loaded from disk: 0.000 seconds
exercise2-4-redis              | 1:M 21 Sep 2021 13:33:51.942 * Ready to accept connections
exercise2-6-postgres_server    | The files belonging to this database system will be owned by user "postgres".
exercise2-6-postgres_server    | This user must also own the server process.
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | The database cluster will be initialized with locale "en_US.utf8".
exercise2-6-postgres_server    | The default database encoding has accordingly been set to "UTF8".
exercise2-6-postgres_server    | The default text search configuration will be set to "english".
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | Data page checksums are disabled.
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | fixing permissions on existing directory /var/lib/postgresql/data ... ok
exercise2-6-postgres_server    | creating subdirectories ... ok
exercise2-6-postgres_server    | selecting dynamic shared memory implementation ... posix
exercise2-6-postgres_server    | selecting default max_connections ... 100
exercise2-6-postgres_server    | selecting default shared_buffers ... 128MB
exercise2-6-postgres_server    | selecting default time zone ... UTC
exercise2-6-postgres_server    | creating configuration files ... ok
exercise2-6-postgres_server    | running bootstrap script ... ok
exercise2-3-backend            | [Ex 2.4+] Initializing redis client
exercise2-3-backend            | [Ex 2.4+] Connection to redis initialized, ready to ping pong.
exercise2-3-backend            | [Ex 2.6+] Initializing postgres connection with envs
exercise2-3-backend            | 		POSTGRES_HOST      postgres_server,
exercise2-3-backend            | 		POSTGRES_USER:     postgres,
exercise2-3-backend            | 		POSTGRES_PASSWORD: postgres,
exercise2-3-backend            | 		POSTGRES_DATABASE: postgres
exercise2-3-backend            | 		to postgres_server:5432
exercise2-3-backend            | [Ex 2.6+] Connection to postgres failed! Retrying...
exercise2-6-postgres_server    | performing post-bootstrap initialization ... sh: locale: not found
exercise2-6-postgres_server    | 2021-09-21 13:33:52.851 UTC [31] WARNING:  no usable system locales were found
exercise2-6-postgres_server    | ok
exercise2-6-postgres_server    | syncing data to disk ... initdb: warning: enabling "trust" authentication for local connections
exercise2-6-postgres_server    | You can change this by editing pg_hba.conf or using the option -A, or
exercise2-6-postgres_server    | --auth-local and --auth-host, the next time you run initdb.
exercise2-6-postgres_server    | ok
exercise2-6-postgres_server    |
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | Success. You can now start the database server using:
exercise2-6-postgres_server    |
exercise2-6-postgres_server    |     pg_ctl -D /var/lib/postgresql/data -l logfile start
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | waiting for server to start....2021-09-21 13:33:54.962 UTC [36] LOG:  starting PostgreSQL 13.2 on x86_64-pc-linux-musl, compiled by gcc (Alpine 10.2.1_pre1) 10.2.1 20201203, 64-bit
exercise2-6-postgres_server    | 2021-09-21 13:33:54.974 UTC [36] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
exercise2-6-postgres_server    | 2021-09-21 13:33:55.029 UTC [37] LOG:  database system was shut down at 2021-09-21 13:33:53 UTC
exercise2-6-postgres_server    | 2021-09-21 13:33:55.063 UTC [36] LOG:  database system is ready to accept connections
exercise2-6-postgres_server    |  done
exercise2-6-postgres_server    | server started
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | /usr/local/bin/docker-entrypoint.sh: ignoring /docker-entrypoint-initdb.d/*
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | waiting for server to shut down....2021-09-21 13:33:55.142 UTC [36] LOG:  received fast shutdown request
exercise2-6-postgres_server    | 2021-09-21 13:33:55.164 UTC [36] LOG:  aborting any active transactions
exercise2-6-postgres_server    | 2021-09-21 13:33:55.166 UTC [36] LOG:  background worker "logical replication launcher" (PID 43) exited with exit code 1
exercise2-6-postgres_server    | 2021-09-21 13:33:55.166 UTC [38] LOG:  shutting down
exercise2-6-postgres_server    | 2021-09-21 13:33:55.243 UTC [36] LOG:  database system is shut down
exercise2-6-postgres_server    |  done
exercise2-6-postgres_server    | server stopped
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | PostgreSQL init process complete; ready for start up.
exercise2-6-postgres_server    |
exercise2-6-postgres_server    | 2021-09-21 13:33:55.383 UTC [1] LOG:  starting PostgreSQL 13.2 on x86_64-pc-linux-musl, compiled by gcc (Alpine 10.2.1_pre1) 10.2.1 20201203, 64-bit
exercise2-6-postgres_server    | 2021-09-21 13:33:55.383 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
exercise2-6-postgres_server    | 2021-09-21 13:33:55.383 UTC [1] LOG:  listening on IPv6 address "::", port 5432
exercise2-6-postgres_server    | 2021-09-21 13:33:55.405 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
exercise2-6-postgres_server    | 2021-09-21 13:33:55.428 UTC [48] LOG:  database system was shut down at 2021-09-21 13:33:55 UTC
exercise2-6-postgres_server    | 2021-09-21 13:33:55.441 UTC [1] LOG:  database system is ready to accept connections
exercise2-3-backend            | [Ex 2.6+] Connection to postgres initialized, ready to ping pong.
exercise2-3-backend            | [GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.
exercise2-3-backend            |
exercise2-3-backend            | [GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
exercise2-3-backend            |  - using env:	export GIN_MODE=release
exercise2-3-backend            |  - using code:	gin.SetMode(gin.ReleaseMode)
exercise2-3-backend            |
exercise2-3-backend            | [GIN-debug] GET    /ping                     --> server/router.pingpong (4 handlers)
exercise2-3-backend            | [GIN-debug] GET    /messages                 --> server/controller.GetMessages (4 handlers)
exercise2-3-backend            | [GIN-debug] POST   /messages                 --> server/controller.CreateMessage (4 handlers)
exercise2-3-backend            | [GIN-debug] Listening and serving HTTP on :8080
exercise2-3-backend            | &{1 pong}
exercise2-3-backend            | [GIN] 2021/09/21 - 13:34:24 | 200 |    1.168411ms |      172.27.0.1 | GET      "/ping?postgres=true"

