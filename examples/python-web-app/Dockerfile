FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN yum update -y && \
    yum install -y python3 python3-pip && \
    pip3 install --no-cache-dir -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




