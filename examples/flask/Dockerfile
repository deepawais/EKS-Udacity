FROM python:3.7.2-slim
COPY . /app
WORKDIR /app
RUN pip install --upgrade pip
RUN pip install -r requirements.txt
RUN pip install flask
RUN pip install gunicorn
RUN pip install pytest
RUN pip install jwt
ENTRYPOINT [ "gunicorn","--preload",  "-b", ":5000", "main:app" ]

