FROM node:lts

WORKDIR /opt/next
COPY . .

RUN yarn install
RUN yarn run build
RUN groupadd -r next && useradd -r -g next next && chown -R next:next .next

USER next
CMD ["yarn", "run", "start"]