FROM python:3.8

COPY . /web
WORKDIR /web

RUN pip install --upgrade pip
RUN pip install -r ./requirements.txt

CMD ["python3", "app.py"]
