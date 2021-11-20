FROM node:lts

WORKDIR /opt/next
COPY . .
# COPY ./pages ./pages
# COPY ./public ./public
# COPY ./styles ./styles
# COPY ./next-env.d.ts ./next-env.d.ts
# COPY ./package.json ./package.json
# COPY ./yarn.lock ./yarn.lock
# COPY ./tsconfig.json ./tsconfig.json

RUN yarn install
RUN yarn run build
RUN groupadd -r next && useradd -r -g next next && chown -R next:next .next

USER next
CMD ["yarn", "run", "start"]