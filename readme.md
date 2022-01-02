# FormaLMS Docker Stack

A docker container for the e-learning platform [Forma LMS](https://www.formalms.org/) based on a centos image, the latest version of Forma LMS (from the [downloads](https://www.formalms.org/download/all-downloads/category/2-releases.html) section-currently 2.4.5) and mariadb.

## Usage

## 1st build latest Forma LMS image
```shell
docker build -t formalms .
```

## 2nd bring up the Forma LMS application and database
```shell
docker-compose up -d
```
This will create both the latest Forma LMS (just built) and Maria DB database stack.

You can change the database credentials used by updating the docker-compose.yml file prior to running the second command. The database is not exposed outside of the stack, but you can always change the database parameters if you so wish.

Likewise, Apache, PHP, and FormaLMS config options can be preset by updating the appropriate config and ini files in this directory prior to initial docker build command.


## 3rd configure the application

Once started the application runs on the default http port 80

Go to `http://{{server-ip}}/formalms/install` to complete the installation.

## Built With

* Forma LMS v2.4.5
* PHP v5.4.16
* MariaDB v10.6.5

## Acknowledgments

* [The Forma LMS project](https://www.formalms.org/)

