

# Install PostgreSql and pgAdmin 4

	sudo apt update
	sudo apt install postgresql postgresql-contrib

# Verify installation

	`sudo -u postgres psql -c "SELECT version();"`

We should see below output:   
	
 ```
	version   ----------------------------------------------------------------------------------------------------------------------------------------
	 PostgreSQL 10.10 (Ubuntu 10.10-0ubuntu0.18.04.1) on x86_64-pc-linux-gnu, compiled by gcc 	   (Ubuntu 7.4.0-1ubuntu1~18.04.1) 7.4.0, 64-bit
	 (1 row)
```

## The postgres user is created automatically when you install PostgreSQL. 
   This user is the superuser for the PostgreSQL instance and it is equivalent to 
   the MySQL root user.

# Login to PostgreSql as admin user: 

	sudo su - postgres (using dash "-" to switch to the target user home directory)

# Start PostgreSql command line tool: 

	psql 

# Set a password for default admin user: 
	psql
	\password postgres
	(at the prompt, enter admin password twice)
	("admin" is my pwd set for "postgres" user)

# Create db for our application, 'cross-post'
	sudo su - postgres -c "createdb cross_post_db"

# Create New Role for our Application/Database

	(login as my default account, "lei")	
	sudo su - postgres -c "createuser cross_post"
	sudo -u postgres psql
	grant all privileges on database cross_post_db to cross_post;

	Use previous \password command to set a password for "cross_post" user: "admin"


# By default, PostgreSql server listens to local interface only: 127.0.0.1. 
  Perform further configuration as needed. 


