FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt /app/
COPY test-app.py /app/
RUN pip install --trusted-host pypi.python.org -r requirements.txt
CMD ["python", "test-app.py"]