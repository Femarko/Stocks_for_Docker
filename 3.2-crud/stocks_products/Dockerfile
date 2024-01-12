FROM python:3.9-alpine
RUN apk add --no-cache gcc musl-dev linux-headers

WORKDIR stocks_products
COPY ./requirements.txt .
RUN pip3 install --no-cahe-dir --upgrade -r requirements.txt

COPY . /stocks_products
EXPOSE 80

CMD python manage.py migrate & python manage.py runserver
