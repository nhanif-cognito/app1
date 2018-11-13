To deploy a basic hello world application on HTTP server follow steps below

1.Create a simple python file index.py using flask and also specify HTTP server ip and port init.
2.Create a Dockerfile containing 
  1. python base image source
  2. COPY all files from base image to new folder
  3. set path to WORKDIR
  4. invoke PyPi on build to produce a container image that has all of the dependencies and the application using these             dependencies.
  5. EXPOSE port for HTTP server
  6. RUN python code 
