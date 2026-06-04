FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /app

RUN groupadd -r main_group && useradd -r -g main_group user

COPY . .

RUN chown -R user:main_group /app

USER user

EXPOSE 8080

CMD ["python", "app.py"]