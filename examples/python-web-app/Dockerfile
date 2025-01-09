# Use a Red Hat-compatible base image
FROM registry.access.redhat.com/ubi8/ubi:latest

# Set the working directory
WORKDIR /app

# Copy application files
COPY requirements.txt /app
COPY devops /app

# Install Python and pip
RUN yum update -y && \
    yum install -y python3 python3-pip && \
    pip3 install --no-cache-dir -r requirements.txt

# Expose the required port
EXPOSE 8000

# Define the entry point and command
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]

CMD ["manage.py", "runserver", "0.0.0.0:8000"]




