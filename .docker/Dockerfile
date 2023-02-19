FROM python:3.10-slim
ENV APP_DIR "/opt/app/"

ENTRYPOINT [ "waitress-serve" ]
CMD [ "--port=8080", "--call", "app:create_app" ]

RUN mkdir -pv "${APP_DIR}"
WORKDIR "${APP_DIR}"

COPY requirements.txt "${APP_DIR}"/requirements.txt
RUN pip install -r requirements.txt
COPY ./src/ ${APP_DIR}

