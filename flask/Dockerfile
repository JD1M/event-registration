FROM python:3

COPY . /web
WORKDIR /web

RUN pip install --no-cache-dir -r requirements.txt
RUN pip install gunicorn

EXPOSE 5000

CMD [ "gunicorn", "-w", "4", "--bind", "0.0.0.0:5000", "app:app"]
# CMD ["python", "app.py"]
