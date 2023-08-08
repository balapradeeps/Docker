FROM nginx
RUN apt-get update && apt-get upgrade -y
COPY devops_countdown /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
