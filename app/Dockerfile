FROM python:3

RUN useradd -m -d /app backend
RUN apt-get -q update && apt-get -q install -y gettext-base
RUN python3 -m pip install flask

USER backend
WORKDIR /app

COPY --chmod=777 api.py /app
COPY --chmod=777 web.py /app
COPY --chmod=777 app.sh /app

EXPOSE 5000

CMD ["/bin/bash", "app.sh"]
