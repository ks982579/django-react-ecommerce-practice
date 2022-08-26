FROM node

WORKDIR /app 
COPY package.json .
RUN npm install

# Copy in remaining code
COPY . . 

EXPOSE 3000

CMD [ "npm", "start" ]