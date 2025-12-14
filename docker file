FROM python:3.11-slim

WORKDIR /app
COPY . /app

RUN pip install --no-cache-dir \
    flask==3.0.1 \
    pandas==2.1.4 \
    numpy==1.26.4 \
    scikit-learn==1.4.2 \
    gunicorn==22.0.0

EXPOSE $PORT
CMD ["gunicorn", "--bind", "0.0.0.0:$PORT", "main:app"]
