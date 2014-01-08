# dockerfiles
for various things

## credits
Shamelessly stolen from: https://github.com/cambridge-healthcare/dockerfiles.
I seem to be messing around with a lot of their stuff atm!

MySQL Dockerfile is from the excellent fglio.com blog post on [creating a MySQL
containter](http://txt.fliglio.com/2013/11/creating-a-mysql-docker-container)

## instructions

To build locally:

```sh
docker build -rm -t roovo/ubuntu:12.04            ./ubuntu.12.04
docker build -rm -t roovo/ruby-build:20131225.1   ./ruby_build
docker build -rm -t roovo/ruby:2.0.0-p247         ./ruby.2.0

docker build -rm -t roovo/mysql:5.5               ./mysql.5.5
```

To run the mysql container (persisting data in `/data/mysql` on the host):

```sh
docker run -d -p 3306:3306 -v /data/mysql:/var/lib/mysql roovo/mysql:5.5
```
