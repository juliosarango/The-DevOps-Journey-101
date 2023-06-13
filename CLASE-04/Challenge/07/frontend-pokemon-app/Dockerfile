FROM node
ENV NODE_OPTIONS --openssl-legacy-provider
COPY . .
RUN yarn install
RUN chmod +x ./entrypoint

ENTRYPOINT [ "./entrypoint" ]    