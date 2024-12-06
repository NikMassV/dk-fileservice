Build image:
- docker build . --tag=dk-fileservice:latest

Run container:
- docker run -p 8070:8080 --rm --name dk-fileservice -e storage.location='/tmp/storage.txt' -v dk-fileservice-storage:/tmp dk-fileservice:latest

Check volumes:
-docker volume ls

Publish to Docker Hub:
- docker tag fileservice:latest nikmassv/fileservice:latest
- docker push nikmassv/fileservice:latest

Apply K8s configuration: 
- kubectl apply -f fileservice-deployment.yaml  -f fileservice-service.yaml
