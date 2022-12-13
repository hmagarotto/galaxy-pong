FROM node

WORKDIR /opt/app

ADD app/package* ./
RUN npm ci --omit=dev && \
    npm cache clean --force

COPY app/index.js .

EXPOSE 8112
CMD [ "node", "index.js" ]
