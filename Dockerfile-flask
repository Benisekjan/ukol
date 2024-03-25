FROM python:3.10.13-bookworm
RUN mkdir /app
COPY . /app
WORKDIR /app
RUN pip install --upgrade pip
RUN apt update
RUN apt install -y build-essential
RUN pip install -r requirements.txt
CMD ["gunicorn", "-w", "3", "-b", "0.0.0.0:5000", "run:app"]
