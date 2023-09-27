ARG PY_VER=3.10.9-slim
ARG PORT=8080
FROM python:${PY_VER}

COPY requirements.txt /
RUN pip3 install -r requirements.txt

COPY ./ /workshop01
ENV PORT=${PORT}
EXPOSE ${PORT}

WORKDIR /workshop01
ENTRYPOINT bash run.sh
