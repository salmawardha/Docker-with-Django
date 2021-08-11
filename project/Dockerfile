#FROM django
FROM python:3.8.3-alpine

WORKDIR /usr/src/app

RUN pip install --upgrade pip
COPY requirements.txt ./
RUN pip install virtualenv2
ENV source env/bin/activate && pip install -r requirements.txt
#RUN pip install -r requirements.txt
#COPY . .
#ENTRYPOINT gc_app=project/gc_app/views.py django run --host=0.0.0.0 --port=8000
EXPOSE 8000
CMD ["django", "manage.py", "runserver", "0.0.0.0:8000"]