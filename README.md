# Api-platform
Using Symfony CLI:

# setup
# After cloning the repo, run the following commands.
composer install

# Database and Elasticsearch must be running
# Change DATABASE_URL and ELASTICSEARCH_HOST in .env.local, if needed

bin/console doctrine:database:create --if-not-exists
bin/console doctrine:schema:update --force
bin/console doctrine:fixtures:load -n

bin/console projection:synchronize

symfony server:start
symfony open:local
