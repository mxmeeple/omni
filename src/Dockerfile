FROM python:3.9-slim-buster

# Dependencies for psutil lib to work
RUN apt update && apt upgrade -y && apt install -y gcc && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY ./requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY ./main.py ./stats.py ./

CMD [ "python3" , "main.py"]
