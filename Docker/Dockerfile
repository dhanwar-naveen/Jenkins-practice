FROM python:3.9-alpine

COPY . /app

WORKDIR /app

RUN apk add --no-cache --virtual .build-deps gcc musl-dev \
    && pip install --upgrade pip \
    && pip install -r requirements.txt \
    && apk del .build-deps

EXPOSE 8000

CMD ["python", "main.py"]
