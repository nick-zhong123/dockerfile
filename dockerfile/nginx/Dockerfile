# docker run -d -p 80:80 --name webserver nginx
# docker run -d -p 80:80 --name nginx-container -v index.html:/usr/share/nginx/html:ro -d nginx
# docker build -t my-nginx
FROM nginx
COPY ./www/index.html /usr/share/nginx/html