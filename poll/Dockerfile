FROM python:3.10-rc-slim

WORKDIR /app/poll

COPY requirements.txt ./

RUN pip3 install -r requirements.txt

COPY . .

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]

EXPOSE 80