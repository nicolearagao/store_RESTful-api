FROM python:3.8

COPY . /web
WORKDIR /web

RUN pip install --upgrade pip
RUN pip install -r ./requirements.txt
ENTRYPOINT ["python3"]
CMD ["app.py"]
