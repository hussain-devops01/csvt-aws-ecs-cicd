FROM node:18

WORKDIR /app

COPY . .
EXPOSE 3000

RUN npx prisma generate
RUN npm install
RUN npm run build
CMD [ "npm", "start" ]