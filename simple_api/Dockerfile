# I Use indicated Python image as the base image
FROM python:2.7-stretch

# Maintener of this dockerfile Didier Sabecheun
Maintainer Disabe

# Add the source code of the api to the root directory
ADD student_age.py /

# run some command to update envirronnement
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

# Create a volume to mount data
VOLUME ["/data"]

# Port exposition
EXPOSE 5000

# Run the api inside the container
CMD ["python", "./student_age.py"]
