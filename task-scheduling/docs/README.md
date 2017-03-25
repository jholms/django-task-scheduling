# Task Scheduling with Redis + Celery

This is a sample project that is built on Django(1.10). It is setup to schedule and automate tasks.
Redis is also included to queue tasks. This is meant to be a project that focuses on celery and redis, it is not included with views/templates. I ahve included some celery tasks that can be ran once redis and celery are running. 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

1. Make sure you have python 3.4 installed

2. Create Virtual Environment
    ```
    cd ~/Dev
    mkdir redhome && cd redhome
    virtualenv -p python3.4 redvirtenv.
    ```
3. Create a directory for project 

### Installing

1. Git clone from Github repository

2. Download Redis and Mysql
    - Using [Homebrew](http://brew.sh):
        ```
        brew install mysql

        brew install redis
        ```

3. Run Requirements.txt

4. 4 Processes running:
    ```
    # django
    $ python manage.py runserver
    
    # celery worker
    $ celery -A redhome worker -l info
    
    # celery beat
    $ celery -A redhome beat -l info -S django
    
    # redis server
    $ redis-server
    ```

### Questions?
	Happy Coding!
	Send me a message if you have any issues.
