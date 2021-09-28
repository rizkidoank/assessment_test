# assessment_test 

#prerequisites
- Docker (x86_64, arm64 not supported) 
- Docker Compose

# How to use
1. Export required environment variables
2. run `docker-compose up -d` in root dir

# scalability design
1. Wordpress could be scaled out by configure the value, i.e `docker-compose up -d --scale wordpress=<NUM_OF_INSTANCE>
2. In order to enable the load balancing, we could use load balancer in front of the wordpress, i.e using HAProxy 
3. For database, we could use cluster. In example using MariaDB cluster / galera. But in the docker-compose, haven't implemented yet.
4. Storage stored in persistent volume so stateful data will retained.

# environment variables

- WP_DB (database name)
- WP_DB_USER (database username)
- WP_DB_PASS (database user password)
- WP_DB_ROOT_PASS (database root password)
