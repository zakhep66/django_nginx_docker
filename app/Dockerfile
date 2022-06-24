FROM python:3.8-alpine

RUN pip install --upgrade pip

RUN pip install --upgrade pip wheel
COPY ./req.txt .
RUN pip install -r ./req.txt

COPY ./django_app /app

WORKDIR /app

COPY ./entrypoint.sh /
ENTRYPOINT ["sh", "/entrypoint.sh"]