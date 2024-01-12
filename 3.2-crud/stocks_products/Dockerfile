#FROM python:3.9-alpine
FROM python:3.13.0a2-bookworm
#RUN apk add --no-cache gcc musl-dev linux-headers

#WORKDIR stocks_products
WORKDIR .
COPY ./requirements.txt .
#RUN pip install --no-cahe-dir --upgrade -r requirements.txt
RUN pip install -r requirements.txt

#COPY . /stocks_products
COPY . .
EXPOSE 5040

CMD python manage.py migrate & python manage.py runserver
