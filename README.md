# ChallengesDE
Create the execution environment with docker-compose

``` bash
$ docker-compose build
$ docker-compose run --name task-etl  etl
```

This will open a shell inside the container:

``` bash
root@task-pyspark:~#
```

You can quit from this shell using command: `exit`.

#### Running routines inside container

Run the routines that simulate the Data Enginering process by executing the python programs.
They require no command line paramaters and the result is presented in console.

``` bash
$ python3 ingestion.py # For ingesting the provided data in trips.csv
$ pytho3 reports.py # For obtaining the result from the Database
```

For changing the parameter for the reports, edit the reports.py file inside the container, or rebuild the containers if edited outside.
