Build image:
- docker build . --tag=dk-fileservice:latest

Run container:
- docker run -p 8070:8080 --rm --name dk-fileservice -e storage.location='/tmp/storage.txt' -v dk-fileservice-storage:/tmp dk-fileservice:latest

Check volumes:
-docker volume ls
