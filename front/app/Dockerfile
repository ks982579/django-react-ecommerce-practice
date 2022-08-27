FROM node

WORKDIR /app 
COPY package.json .
RUN npm install

# Copy in remaining code
COPY . . 

EXPOSE 3000

CMD [ "npm", "start" ]

# docker build --help
# docker build -t react-emporium:1.0 .
# docker run --name emporium-frontend --rm -d -p 3000:3000 react-emporium:1.0

## Does not appear to require the need of being ran in -it mode. 