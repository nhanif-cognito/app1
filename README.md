To deploy a basic hello world application on HTTP server follow steps below 1.Create a simple python file index.py using flask and also specify HTTP server ip and port init. 2.Create a Dockerfile containing

python base image source
COPY all files from base image to new folder
set path to WORKDIR
invoke PyPi on build to produce a container image that has all of the dependencies and the application using these dependencies.
EXPOSE port for HTTP server
RUN python code
