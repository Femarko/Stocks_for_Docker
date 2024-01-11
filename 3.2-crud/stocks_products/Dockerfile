FROM python:3.9-alpine
RUN apk add --no-cache gcc musl-dev linux-headers

WORKDIR src
COPY ./requirements.txt .
RUN pip3 install --no-cahe-dir --upgrade -r requirements.txt

ENV

COPY . /src
EXPOSE 80

CMD ["python", "manage.py", "migrate", "runserver"]