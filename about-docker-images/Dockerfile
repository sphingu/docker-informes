FROM node:16.9.1-alpine3.14

WORKDIR /app

COPY ./my-svelte-app .

RUN npm i -g pnpm
RUN pnpm install

# ENV API_URL=http://api.myapp.com/

EXPOSE 5000

# RUN mkdir data 

# RUN addgroup app && adduser -S -G app app

# RUN chown app:app data

# USER app

ENTRYPOINT ["npm", "run", "dev"]