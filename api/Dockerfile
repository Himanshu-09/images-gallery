FROM python:3.10

WORKDIR /app

EXPOSE 5050

COPY Pipfile Pipfile.lock ./

RUN pip install --upgrade pip
RUN pip install pipenv
RUN pipenv requirements > requirements.txt
RUN pip install -r requirements.txt

COPY . ./

# Use pipenv to run the application
CMD ["python", "main.py"]
