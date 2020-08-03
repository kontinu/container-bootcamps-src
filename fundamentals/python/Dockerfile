# For more information, please refer to https://aka.ms/vscode-docker-python
FROM python:3.8


EXPOSE 5000

# Keeps Python from generating .pyc files in the container
ENV PYTHONDONTWRITEBYTECODE 1

# Turns off buffering for easier container logging
ENV PYTHONUNBUFFERED 1

ENV APP_HOME=/app/
# Install pip requirements

ADD requirements.txt /tmp/
RUN python -m pip install -r /tmp/requirements.txt

RUN echo "date"


WORKDIR ${APP_HOME}
COPY . ${APP_HOME}


RUN whoami


#ENTRYPOINT [ "python","app.py" ]
CMD [ "python","/app/app.py" ]


