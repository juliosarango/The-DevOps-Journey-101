FROM node
ENV NODE_OPTIONS --openssl-legacy-provider
COPY src /src
COPY ./entrypoint /src
WORKDIR /src/
RUN chmod +x ./entrypoint
RUN yarn install

ENTRYPOINT [ "./entrypoint" ]    