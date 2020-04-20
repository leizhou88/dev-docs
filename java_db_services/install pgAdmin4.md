
# Install pgAdmin4 on Unbuntu 18

## import postgresql repo key

	sudo apt-get install curl ca-certificates gnupg
	curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

	sudo apt update -y && sudo apt upgrade -y

## create /etc/apt/sources.list.d/pgdg.list

	sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ bionic-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

## Update local repo

	sudo apt-get update

## Install

	sudo apt install pgadmin4
	sudo apt-get install pgadmin4-apache2
	(when prompted, enter "lei@ips" as user name, and "admin" as password)

## Launch pgAdmin4: 

	in browser, enter http://localhost/pgadmin4
	in login boxes, enter lei@ips and admin


