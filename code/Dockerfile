FROM python:3.8

COPY . /web
WORKDIR /web

RUN pip install --upgrade pip
RUN pip install -r ./requirements.txt
EXPOSE 5000
ENTRYPOINT ["python"]
CMD ["web/app.py"]
