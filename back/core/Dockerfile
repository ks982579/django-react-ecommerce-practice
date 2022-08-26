FROM python

# set up working directory
WORKDIR /usr/src/core

# Setting Environment Variables
## prevent python writing pyc files to disc
ENV PYTHONDONTWRITEBYTECODE 1
## prevent python from buffering stdout and stderr
ENV PYTHONUNBUFFERED 1

# Install psycopg2 dependencies
# RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev

RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/core
RUN pip install -r requirements.txt

# Copy in rest of project
COPY . /usr/src/core

EXPOSE 8000

CMD [ "python", "./manage.py", "runserver", "0.0.0.0:8000" ]

# core/core/...
# core/manage.py

# docker build --help
# docker build -t django-core:1.1
# docker run --name django-backend --rm -d -p 8000:8000 django-core:1.1