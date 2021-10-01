# conversao-peso

# Criar imagem com Dockerfile
docker build -t conversao-peso -f Dockerfile .

# Ver imagem criada
docker images
ou
docker image ls

# Criar container com a imagem criada
docker create --name conversao-peso-kubedev conversao-peso
# Rodar container
docker start conversao-peso-kubedev


ou

# Criar e rodar container
docker run -d -p 5000:80 --name conversao-peso-kubedev conversao-peso


# Passos de criar imagem, dar push e criar cluster e kubernetes
1) docker build -t elainecro/conversao-peso:v1 .
2) docker push elainecro/conversao-peso:v1
3) docker tag elainecro/conversao-peso:v1 elainecro/conversao-peso:latest
4) docker push elainecro/conversao-peso:latest
5) kind create cluster --name clusterconversao --config cluster.yaml
6) kubectl apply -f deployment.yaml
7) acessar localhost:8080 :)