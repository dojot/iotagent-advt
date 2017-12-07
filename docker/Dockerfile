FROM node:8

COPY . /opt/iotagent-advt/
WORKDIR /opt/iotagent-advt

RUN apt-get update \
    && apt-get install -y python-pip \
    &&  pip install pyopenssl

RUN npm install && npm run-script build

RUN chmod +x /opt/iotagent-advt/entrypoint.sh \
    && mkdir /opt/iotagent-advt/certs

CMD ["/opt/iotagent-advt/entrypoint.sh"]
