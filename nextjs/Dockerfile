FROM node:20-alpine3.16

ARG NEXT_PUBLIC_BACKEND_ENDPOINT

ENV NEXT_PUBLIC_BACKEND_ENDPOINT=${NEXT_PUBLIC_BACKEND_ENDPOINT}

RUN mkdir -p /var/app/current

WORKDIR /var/app/current

COPY . .

RUN npm ci

RUN npm run build

CMD [ "npm", "run", "start" ]
