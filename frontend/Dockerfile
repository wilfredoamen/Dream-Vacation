FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install react-scripts@latest


ENV REACT_APP_API_URL=http://3.80.107.219:3001

COPY . .

RUN npm run build
RUN npm install -g serve

EXPOSE 3000

CMD ["serve", "-s", "build"]
