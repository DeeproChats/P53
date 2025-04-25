FROM node:20-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci
COPY . .
ENV PORT=5000
EXPOSE 5000
CMD ["node","src/index.js"]
HEALTHCHECK CMD wget -qO- http://localhost:5000/healthz || exit 1
