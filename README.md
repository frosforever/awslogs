awslogs
=======

Docker image for [awslogs](https://github.com/jorgebastida/awslogs), a simple command line tool for querying groups, streams and events from [Amazon CloudWatch](http://aws.amazon.com/cloudwatch/) logs.

Attempts to track the repo itself rather than install from pip. May lag behind as a result.

To build the image:
```
  $ docker build -t awslogs .
```
To run, provide environment variables to the container via:
```
  $ docker run -it --rm -e AWS_ACCESS_KEY_ID=<key> -e AWS_SECRET_ACCESS_KEY=<secret> -e AWS_REGION=<region> awslogs
```
Or by mounting a local .aws configuration directory:
```
  $ docker run -it --rm -v path/to/.aws/:/root/.aws:ro awslogs
```
See [awslogs README](https://github.com/jorgebastida/awslogs/blob/master/README.rst) for more details.
