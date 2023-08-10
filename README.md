# Docker_Containers_with_command:

-docker ps <container_id> (to list all running containers):

#output:

CONTAINER ID   IMAGE       COMMAND             CREATED             STATUS          PORTS      NAMES
9ea4eaeef1b5   hello-app   "python hello.py"   About an hour ago   Up 28 minutes   8080/tcp   new-name

-docker stop <container_id> (to stop the running container):

#output:

9ea4eaeef1b5

-docker rm <container_id> (to remove the stopped container):

#output:

e7243e2033f8

-docker logs <container_id> (to see the logs of container):

#output:

Traceback (most recent call last):
  File "/part_one/hello.py", line 10, in <module>
    httpd.serve_forever()
    ^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.11/socketserver.py", line 233, in serve_forever
    ready = selector.select(poll_interval)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.11/selectors.py", line 415, in select
    fd_event_list = self._selector.poll(timeout)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

 -docker inspect <container_id> (to view the detail of a container):

 #output:
 
 [
    {
        "Id": "9ea4eaeef1b5a9e768563667db6b275e2c15aefdb4b23d353ba7d2b26e7589b3",
        "Created": "2023-08-09T21:16:35.448246112Z",
        "Path": "python",
        "Args": [
            "hello.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 15930,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-08-09T21:53:48.475371887Z",
            "FinishedAt": "2023-08-09T21:47:08.498685336Z"
        },
        .
        .
        .
        to be continue

-docker exec <container_id> ls (to execute the command inside the container):

#output:

hello.py

-docker attach <container_id> (to attach to running container):

-docker commit <container_id> new_image_name (to create a image from container):

#output:

sha256:5dd4c4299d2b87ee6d51c76928e96deeeb6c9cde773bb06e3a527e97a59c5fc6

-docker cp /path/to/local/file.txt <container_id>/path/in/container/ (to copy files between container and host):

-docker stats <container_id> (to view the resource usage of container):

#output:

CONTAINER ID   NAME       CPU %     MEM USAGE / LIMIT   MEM %     NET I/O   BLOCK I/O   PIDS
9ea4eaeef1b5   new-name   0.00%     0B / 0B             0.00%     0B / 0B   0B / 0B     0

-docker top <container_id> (to view the running processes inside container):

#output:

UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                21176               21155               1                   22:39               ?                   00:00:00            python hello.py

-docker start <container_id> (to start the stopped container):

#output:

9ea4eaeef1b5

-docker pause <container_id> (to pause the running container):

#output:

9ea4eaeef1b5

-docker unpause <container_id> (to unpause the paused container):

#output:

9ea4eaeef1b5

-docker rename <container_id> new_name (to rename the current container):

#output:

check the docker desktop after running this command, name will be changed

-docker wait <container_id> (to wait for a container to exit)

-docker attach <container_id> (to attach the local input/output to a running container)

-docker port <container_id> (to view public facing port that container uses)

-docker update <container_id> flag (to update the resource of container)

-docker restart <container_id> (to restart a running container):

#output:

9ea4eaeef1b5
